<script lang="ts">

    // Import images for the teams (you can replace these imports with actual paths)
    import sec from '../../../public/home/Features/Team Logo (1).svg';
    import first from '../../../public/home/Features/Team Logo.svg';
    import md from '../../../public/home/Features/vs.svg';
    import Heading from '../../atoms/heading.svelte';

    // Mock dynamic data (JSON format)
    const jsonData = [
    {
      name: {first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.22, second: 1.72 },
      status: "Live",
      matchTime: "22 Dec 2024 (07:00 PM)",
      logo: "/path/to/team-logo-1.svg",  // Logo image path
    },
    {
      name: {first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.50, second: 2.10 },
      status: "Live",
      matchTime: "23 Dec 2024 (09:00 PM)",
      logo: "/path/to/team-logo-2.svg",  // Logo image path
    },
    {
      name:{first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.35, second: 2.00 },
      status: "Live",
      matchTime: "24 Dec 2024 (10:00 PM)",
      logo: "/path/to/team-logo-3.svg",
    },
    {
      name:{first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.50, second: 1.95 },
      status: "Live",
      matchTime: "25 Dec 2024 (06:00 PM)",
      logo: "/path/to/team-logo-4.svg",
    },
    {
      name:{first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.60, second: 2.40 },
      status: "Live",
      matchTime: "26 Dec 2024 (08:00 PM)",
      logo: "/path/to/team-logo-5.svg",
    },
    {
      name: {first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.40, second: 1.85 },
      status: "Upcoming",
      matchTime: "27 Dec 2024 (07:30 PM)",
      logo: "/path/to/team-logo-6.svg",
    },
    {
      name: {first:"Borcelle",sec:"Rimbero"},
      odds: { first: 1.75, second: 2.30 },
      status: "Live",
      matchTime: "28 Dec 2024 (09:15 PM)",
      logo: "/path/to/team-logo-7.svg",
    }
  ];

  
  </script>

  <Heading text='Featured Matches'/>
  <div class="px-[5%] overflow-hidden">
  <div class="overflow-x-scroll  scrollbar-hidden snap-x ">
  <div class=" flex w-fit gap-2 md:gap-3  py-3">
    {#each jsonData as team}
      <div class="w-[310px] h-[240px] snap-center rounded-lg shadow-box shadow-gray-300 hover:border-2 border-[1px] border-[--purple] overflow-hidden">
        <div class="text-white px-5 py-6 gap-x-11 gap-y-8 bg-transparent justify-between grid grid-cols-3">
          <!-- Odds for the first and second columns -->
          <div class="flex items-center justify-center bg-[--Secondary] rounded w-16 text-center h-10">{team.odds.first}</div>
          <div class="flex items-center justify-center bg-[--Accent] shadow-inner shadow-red-700 rounded-lg w-20 text-center h-10">
            <ul class="list-disc bg-transparent">
              <li class="bg-transparent">{team.status}</li>
            </ul>
          </div>
          <div class="flex items-center justify-center bg-[--Secondary] rounded w-16 text-center h-10">{team.odds.second}</div>
  
          <!-- First Team (Borcelle) -->
          <div>
            <img class="" 
                 src={first} 
                 alt="Borcelle logo" 
                 loading="lazy" 
                 decoding="async" 
                 style="object-fit: cover;" />
            <h1 class="text-xl flex justify-center font-semibold text-white">{team.name.first}</h1>
          </div>
  
          <!-- Empty div (important) -->
          <div class="scale-110">
            <img class="" 
            src={md} 
            alt="Borcelle logo" 
            loading="lazy" 
            decoding="async" 
            style="object-fit: cover;" />
          </div>
  
          <!-- Second Team (Rimbero) -->
          <div class="bg-transparent">
            <img class="" 
                 src={sec} 
                 alt="Rimbero logo" 
                 loading="lazy" 
                 decoding="async" 
                 style="object-fit: cover;" />
            <h1 class="text-xl flex justify-center font-semibold text-white">{team.name.sec}</h1>
          </div>
        </div>
  
        <!-- Match Time -->
        <div class="text-white text-center flex justify-center items-center bg-transparent h-7 -mt-3">
          <p class="h-full flex items-center justify-center text-sm w-2/3 bg-[--Primary-Light] rounded">
            {team.matchTime}
          </p>
        </div>
      </div>
    {/each}
  </div>
</div>
</div>