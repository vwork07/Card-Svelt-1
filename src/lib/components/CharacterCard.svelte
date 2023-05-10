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

<div class="bg-white rounded-lg overflow-hidden shadow-md">
  <img class="w-full h-64 object-cover" src="{characterModel}" alt="altCharacterName">
  <div class="p-4">
    <h3 class="text-xl font-medium mb-2">{characterName}</h3>
    <p class="text-gray-700 text-base">{characterDescription}</p>
      <p class="text-gray-700 text-base">HP:{hpStat}</p>
    <p class="text-gray-700 text-base">Atk: {atkStat}</p>
    <p class="text-gray-700 text-base">Def: {defStat}</p>
  </div>
</div>