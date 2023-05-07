
<script>
import FighterCard from '$lib/components/FighterCard.svelte';
  import { Footer, FooterCopyright, FooterLinkGroup, FooterLink, Card, Button, Toggle  } from 'flowbite-svelte';
  let vCard = false;

  let health1 = 15;
  let health2 = 20;

  function attack(){
    if (health1 > health2) {
      health1 = health1 - health2;
    }
    else health1 = health2 - health1;


       if (health2 > health1) {
      health2 = health2 - health1;
    }
    else health2 = health1 - health2;

 if (health1 === 0){
   health1 = "-"
 }

  if (health2 === 0){
   health1 = "-"
 }
  }
</script>

<FighterCard/>

<div class="my-14 grid grid-cols-2 gap-2"> 
  <Card img="https://media.tenor.com/5bRpcqahFjAAAAAi/sword-attack.gif" reverse={vCard}>
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Slicer</h5>
    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
      Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
    </p>
 <h1> {health2} {health2 > 0 ? 'HP' : 'Fainted'}</h1>
  </Card>

    <Card img="https://media.tenor.com/61IRFBR1DH0AAAAi/capoo-blue.gif" reverse={vCard}>
    <h5 class="mb-2 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Sheild Knight</h5>
    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400 leading-tight">
      Here are the biggest enterprise technology acquisitions of 2021 so far, in reverse chronological order.
    </p>
    <h1>{health1} {health1 > 0 ? 'HP' : 'Fainted'}</h1>

  </Card>

     <Button class="my-14" on:click={attack}>
      Attack <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5 ml-2"><path stroke-linecap="round" stroke-linejoin="round" d="M13.5 4.5L21 12m0 0l-7.5 7.5M21 12H3" /></svg>
    </Button>
</div>
<Footer>
  <FooterCopyright href="/" by="TopGunnaVv™" year={2022} />
  <FooterLinkGroup ulClass="flex flex-wrap items-center mt-3 text-sm text-gray-500 dark:text-gray-400 sm:mt-0">
    <FooterLink href="/">About</FooterLink>
    <FooterLink href="/">Privacy Policy</FooterLink>
    <FooterLink href="/">Licensing</FooterLink>
    <FooterLink href="/">Contact</FooterLink>
  </FooterLinkGroup>
</Footer>