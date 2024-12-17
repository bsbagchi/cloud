<script lang="ts">
    import Heading from "../../atoms/heading.svelte";
    import one from '../../../public/home/menu/cricket.svg';
    import three from '../../../public/home/menu/soccer.svg';
    import four from '../../../public/home/menu/tennies.svg';
    import five from '../../../public/home/menu/india.svg';

</script>

<Heading text='Live Sports'/>
<div>
<!-- short menu of livesport -->
<div class="px-[5%] flex gap-2 py-5">
    <div class="border-[1px] border-[--Accent] flex shadow-red gap-1 p-2 rounded w-fit text-center">
        <img  class="bg-transparent"
        src={one}
         
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        /><h1 class="text-[--Accent] bg-transparent">In Play</h1></div>

    <div class="border-[1px] border-blue-500 flex shadow-blue gap-1 p-2 rounded w-fit text-center">
        <img  class="bg-transparent"
        src={one}
         
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        /><h1 class="text-white bg-transparent">Cricket</h1>
    </div>
    <div class="border-[1px] border-[--Border-Light]  flex gap-1 p-2 rounded w-fit text-center">
        <img  class="bg-transparent"
        src={three}
         
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        /><h1 class="text-white bg-transparent">Soccer</h1>
    </div>
    <div class="border-[1px] border-[--Border-Light]  flex gap-1 p-2 rounded w-fit text-center">
        <img  class="bg-transparent"
        src={four}
         
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        /><h1 class="text-white bg-transparent">Tennies</h1>
    </div>

    <div class="border-[1px] border-[--Border-Light] flex gap-1 p-2 rounded w-fit text-center">
        <img  class="bg-transparent"
        src={five}
         
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        /><h1 class="text-white bg-transparent">Live Casino</h1>
    </div>
</div>

<div class="px-[5%] ">
    <div class="px-3 flex rounded-lg  border border-[--Border-Light]">
    <div class="w-1/2">
        <div class="h-20 flex items-center overflow-hidden">
            <img class="h-2/3"
            
        src={one} 
        alt="Descriptive text here"
        loading="lazy" 
        decoding="async" 
        style="object-fit: cover;  "
        />
        <h1 class="text-3xl text-white px-2">Cricket</h1>
        </div>
    </div>
    <div class="w-1/2">
        <div class="h-20  items-center grid grid-cols-3 justify-between text-white">
            <div class='text-center  text-[--Accent-Alt]  text-2xl'>1</div>
            <div class='text-center  text-[--Accent-Alt]  text-2xl'>X</div>
            <div class='text-center  text-[--Accent-Alt]  text-2xl'>2</div>
        </div>
    </div>
</div>
</div>
</div>