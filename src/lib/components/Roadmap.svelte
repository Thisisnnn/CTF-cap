<script>
  import RoadmapCard from "./Cards.svelte";

  const roadmapItems = [
    { id: 1, title: "Planning", content: "Define project scope and requirements.", date: "September", icon: "ri-flag-line" },
    { id: 2, title: "LFS", content: "Design the user interface and experience.", date: "October-November", icon: "ri-paint-brush-line" },
    { id: 3, title: "Tools", content: "Implement essential tools and libraries.", date: "Planned", icon: "ri-code-line" },
    { id: 4, title: "KDE", content: "Add an user interface to the project.", date: "Planned", icon: "ri-rocket-line" },
    { id: 5, title: "Design", content: "Add the icons and background to KDE.", date: "Planned", icon: "ri-flag-checkered-line" },
    { id: 6, title: "Launch", content: "Prepare for project launch and marketing.", date: "Planned", icon: "ri-launcher-line" }
  ];
  // index of the last roadmap item — used to hide edge dots on mobile
  const lastIndex = roadmapItems.length - 1;
</script>

<div class="relative w-full min-h-screen py-16">
  <!-- Central vertical line -->
  <div class="absolute w-px h-full bg-slate-200 left-1/2 -translate-x-1/2"></div>

  <div class="flex flex-col space-y-24 lg:space-y-12">
    {#each roadmapItems as item, i}
      <div class="relative flex w-full">
        <!-- Desktop dot (single, centered on the central line) -->
        <div class="hidden lg:block absolute left-1/2 -translate-x-1/2 top-1/2 -translate-y-1/2">
          <div class="w-4 h-4 bg-sky-500 rounded-full"></div>
        </div>

        <!-- Mobile dots (two per card, top and bottom) -->
        {#if i !== 0}
          <!-- top dot: not shown for the first card -->
          <div class="absolute w-4 h-4 bg-sky-500 rounded-full left-1/2 -translate-x-1/2 top-0 z-10 lg:hidden"></div>
        {/if}

        {#if i !== lastIndex}
          <!-- bottom dot: not shown for the last card -->
          <div class="absolute w-4 h-4 bg-sky-500 rounded-full left-1/2 -translate-x-1/2 bottom-0 z-10 lg:hidden"></div>
        {/if}

        <!-- Card -->
        <div class={`relative w-full px-4 mt-2 mb-2 lg:mt-6 lg:mb-0 lg:w-1/2 ${i % 2 === 0 ? 'lg:ml-auto lg:pr-8' : 'lg:mr-auto lg:pl-8'}`}>
          <RoadmapCard
            title={item.title}
            content={item.content}
            date={item.date}
            icon={item.icon}
          />
        </div>
      </div>
    {/each}
  </div>
</div>
