<script>
  export let text = 'English'; // Dynamic text
  export let color = '--Primary-Light'; // Dynamic background color
</script>

<button class="px-3 h-8 w-fit rounded-lg text-white flex items-center justify-center whitespace-nowrap" style={`background-color: var(${color});`}>
  <span class="bg-transparent">{text}</span>
</button>
