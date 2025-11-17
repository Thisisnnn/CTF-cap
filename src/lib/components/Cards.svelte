<script>
  export let title = "";
  export let content = "";
  export let date = "";
  export let icon = "";
  export const id = "";

  const cardClasses = {
    container: "w-full border border-slate-200 rounded-2xl p-6 bg-white hover:shadow-md transition cursor-pointer",
    header: "flex items-center gap-3",
    badge: "w-[40px] h-[40px] bg-sky-50 rounded-full text-sky-500 flex items-center justify-center text-lg",
    title: "font-semibold text-slate-700 text-lg",
    date: "mt-2 text-slate-500 text-sm font-medium border border-slate-200 rounded-md inline-block px-2 py-1 bg-slate-50",
    content: "text-slate-500 text-[14px] mt-4 leading-relaxed",
  };
</script>

<div class={cardClasses.container}>
  <div class={cardClasses.header}>
    <div class={cardClasses.badge}>
      <i class={icon}></i>
    </div>
    <h3 class={cardClasses.title}>{title}</h3>
  </div>

  <div class={cardClasses.date}>{date}</div>
  <p class={cardClasses.content}>{content}</p>
</div>

<style>
  /* Card container */
  :global([data-theme='dark'] .w-full.bg-white) {
    background-color: #2e3250 !important;
    border-color: #444b6b !important;
    transition: box-shadow 0.3s ease !important;
  }

  /* Badge */
  :global([data-theme='dark'] .bg-sky-50.text-sky-500) {
    background-color: #d9b06c !important;
    color: #fff7e6 !important;
  }

  /* Title */
  :global([data-theme='dark'] .text-slate-700) {
    color: #fef6e4 !important;
  }

  /* Date */
  :global([data-theme='dark'] .bg-slate-50.text-slate-500.border-slate-200) {
    background-color: #3a3f65 !important;
    border-color: #565f86 !important;
    color: #f2d9b3 !important;
  }

  /* Content */
  :global([data-theme='dark'] .text-slate-500) {
    color: #f6e9d6 !important;
  }

  /* Hover glow around the card */
  :global([data-theme='dark'] .w-full.bg-white:hover) {
    box-shadow: 0 0 20px 10px rgba(217, 176, 108, 0.35) !important; /* soft golden glow */
  }
</style>
