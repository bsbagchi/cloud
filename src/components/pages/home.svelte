<script lang="ts">
    import Header from "../organisms/header.svelte";
    import Heading from "../atoms/heading.svelte";
    import one from '../../public/images/img1.jpeg';
    import two from '../../public/images/img2.jpeg';
    import three from '../../public/images/img3.jpeg';
    import Featured from "../molecules/Home/featured.svelte";
    import Livesport from "../molecules/Home/livesport.svelte";
    const imglink=[one,two,three];
</script>
<Header/>
<div>
<div >
    <Heading text='Treading Games'/>
    <div class="overflow-x-scroll snap-x scrollbar-hidden">
    <div class="flex gap-3 w-fit py-3 px-[5%]">
        {#each imglink as path }
        <div class="rounded-lg snap-center max-lg:w-[320px] border-t-4 border-l-[1px] border-r-[1px] border-red-600   shadow-xl hover:shadow-blue-500 overflow-hidden">
        <img class="h-[200px]" 
        src={path} 
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        />
    </div>
        {/each}
        
    </div>
</div>
</div>


<Featured/>
<Livesport/>
</div>