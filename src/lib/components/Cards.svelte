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
