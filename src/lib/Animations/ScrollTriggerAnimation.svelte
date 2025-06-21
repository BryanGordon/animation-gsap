<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'
  import { ScrollTrigger } from 'gsap/ScrollTrigger'

  gsap.registerPlugin(ScrollTrigger)

  onMount(() => {
    gsap.to('h1', {
      scale: 1.3,
      autoAlpha: 0,
      scrollTrigger: {
        // scrub: true, // Vincula la animacion para que se sincronice con el scroll
        scrub: 1 // Aumenta la suavidad de la animacion, añade un retraso
      }
    })
  })
</script>

<section class="scroll-section">
  <h1>Nombre Producto</h1>
</section>

<style>
  .scroll-section {
    display: flex;
    height: 100dvh;
    align-items: center;
    justify-content: center;
  }
  
  h1 {
    color: plum;
    text-align: center;
    font-size: 90px;
    width: 95%;
  }
</style>