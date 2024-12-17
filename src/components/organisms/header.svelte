<script lang='ts'>
    import Button from '../atoms/button.svelte';
    import one from '../../public/home/Features/vs.svg';
  
    const menu=[
      {image:'../../public/home/Features/vs.svg',lable:'In Play'}, {image:'',lable:'Multi market'}, {image:'',lable:'Cricket'}, {image:'',lable:'Soccer'}, {image:'',lable:'Tennis'}, {image:'',lable:'Casino Games'},{image:'',lable:'Aviator'},{image:'',lable:'Aura'},{image:'',lable:'Blast'},{image:'',lable:'India'}];
    let isMenuVisible = false;

  // Function to toggle menu visibility
  function Handlemenu() {
    isMenuVisible = !isMenuVisible;
  }
  </script>


<div class="w-full h-10 flex justify-between items-center bg-[--primary] px-[5%] py-8 sticky top-0">
    <!-- This is menu icon -->
<button aria-label="menu" on:click={Handlemenu}>
    <div class="flex ">
        <div class="border-2 h-3 w-3 border-white rounded m-[1px]"></div>
        <div></div>
        <div class=" border-2 h-3 w-3  border-white rounded m-[1px]"></div>
    </div>
    <div class="flex  ">
        <div class=" border-2 h-3 w-3 border-white rounded m-[1px]"></div>
        <div class="border-2 h-3 w-3 border-white rounded-full m-[1px]"></div>
    </div>
</button>


<div class="flex gap-3 bg-transparent">
    <Button text={"English"} color={"--Primary-Light"} />
    <Button text={"Sign In"} color={"--Primary-Light"} />
    <Button text={"Register"} color={"--Accent"} />
</div>
</div>
<!-- Menu items with dynamic buttons -->
 <div class="flex  my-3 px-[5%] bg-[--Primary-Light] ">
<div class="py-3 w-full overflow-x-scroll scrollbar-hidden flex gap-3 bg-transparent">
    {#each menu as item}
      <Button text={item.lable} color="--bg-body" />
    {/each}
  </div>
</div>
