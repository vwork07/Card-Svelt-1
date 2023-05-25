<script>
	import CharacterCard from '$lib/components/CharacterCard.svelte';
  import jsonData from '$lib/data2.json';

  console.log(jsonData);


let temp1characterIndex = 2;
let temp1characterModel = "https://media.tenor.com/aIr8iKZ3UdIAAAAi/hasher-sticker.gif";
let temp1characterName = "Bengali Mali ";
let temp1altCharacterName = "waka man";
let temp1characterDescription = "man the man man";
let temp1atkStat= 30;
let temp1defStat= 50;
let temp1hpStat = 150;

let tempcharacterIndex = 1;
let tempcharacterModel = "https://media.tenor.com/wrMDu29fA-YAAAAi/hasher-happy-sticker.gif";
let tempcharacterName = "Bone Papichu ";
let tempaltCharacterName = "bone boy";
let tempcharacterDescription = "the greatst of bone keepers";
let tempatkStat= 50;
let tempdefStat= 30;
let temphpStat = 150;

function getPercentage(num, percentage) {
  return (num * percentage) / 100;
}

function attack() {
	let health1 = temp1hpStat;
	let health2 = temphpStat;



health1 = (tempatkStat - getPercentage(temp1defStat, 50)) - health1;

if (health1 === 0) {
	temp1hpStat = "x_x UN-ALIVED!!! x_x"
}
else {
temp1hpStat = Math.abs(health1);
}
}
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>


<div class="grid grid-cols-2 gap-4 mt-20 mx-5 justify-items-center items-center">
<div class="">
<CharacterCard 
 characterIndex = {tempcharacterIndex}
 characterName = {tempcharacterName}
 altCharacterName = {tempaltCharacterName}
 characterDescription = {tempcharacterDescription}
 characterModel = {tempcharacterModel}
 atkStat = {tempatkStat}
 defStat = {tempdefStat}
 hpStat = {temphpStat}/>
</div>

<div class="">
<CharacterCard
characterIndex = {temp1characterIndex}
 characterName = {temp1characterName}
 altCharacterName = {temp1altCharacterName}
 characterDescription = {temp1characterDescription}
 characterModel = {temp1characterModel}
 atkStat = {temp1atkStat}
 defStat = {temp1defStat}
 hpStat = {temp1hpStat}/>

</div>

</div>

<h1>{jsonData.title}</h1>

<ul>
  {#each jsonData.items as item}
    <li>{item.name}</li>
  {/each}
</ul>
<style>

</style>
