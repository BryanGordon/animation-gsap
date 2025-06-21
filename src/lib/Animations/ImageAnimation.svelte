<script>
  import landcape from '../../assets/g9qs6xez97871.jpg'
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'

  onMount(() => {
    gsap.to('img', {
      duration: 1,
      scale: 0.9,
      opacity: 0,
      stagger: {
        each: 0.2,
        repeat: 1,
        yoyo: true,
        grid: 'auto',
        from: 'center'
      }
    })
  })
</script>

<section>
  <article class="grid">
    <img src={landcape} alt="Imagen 1">
    <img src={landcape} alt="Imagen 2">
    <img src={landcape} alt="Imagen 3">
    <img src={landcape} alt="Imagen 4">
    <img src={landcape} alt="Imagen 5">
  </article>
</section>

<style>
  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
    
  }
  
  .grid > img {
    border-radius: 10px;
    width: 100%;
  }
</style>