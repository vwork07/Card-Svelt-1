<script>
export let characterIndex;
export let characterModel;
export let characterName;
export let altCharacterName;
export let characterDescription;
export let atkStat;
export let defStat;
export let hpStat;
</script>



<div class="relative rounded  bg-white shadow-lg">
    <div class="relative w-64 h-64 p-4">
  <img class="absolute inset-0 object-cover w-full h-full" src="{characterModel}" alt="{altCharacterName}">
</div>
  <div class="absolute w-48 bottom-60 right-36">
    <div class="text-center">
      <h1 class="text-lg font-bold text-white bg-blue-400 rounded p-2">{characterName}</h1>
    </div>
  </div>
    <div class="absolute w-24 bottom-5 right-60">
    <div class="text-center">
      <h1 class="text-lg font-bold text-white bg-blue-400 rounded p-2">DEF: {defStat}</h1>
    </div>
  </div>
      <div class="absolute w-24 bottom-20 right-60">
    <div class="text-center">
      <h1 class="text-lg font-bold text-white bg-blue-400 rounded p-2">ATK: {atkStat}</h1>
    </div>
  </div>
      <div class="absolute w-24 bottom-36 right-60">
    <div class="text-center bg-blue-400 rounded p-2">
      <h1 class="text-lg font-bold text-white "><span class="text-sm"> Health </span></h1>
      <p class="text-white text-4xl">{hpStat}</p>
    </div>
  </div>
</div>

