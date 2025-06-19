<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap';
  
  import Counter from './lib/Counter.svelte'
  import landcape from './assets/g9qs6xez97871.jpg'

  onMount(() => {
    /* Primer ejemplo de animación 
    gsap.to('div', {
      x: 220,
      duration: 1.2,
      rotate: 180,
      stagger: {
        each: 0.3,
        repeat: 1,
        yoyo: true,
      }
    })
    */

    gsap.to('.box.blue', {
      x: 300,
      opacity: 0.1,
      scale: 0.5,
      duration: 1.5,
      rotate: 360,
      yoyo: true,
      repeat: 2,
      ease: 'bounce.out'
    })

    gsap.to('.box.pink', {
      x: 300,
      opacity: 0.1,
      scale: 0.5,
      duration: 1.5,
      rotate: 360,
      yoyo: true,
      repeat: 2
    })
/*
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
*/
  })
</script>

<section>
  <div class="box blue">
    <span>Texto del cuadrado</span>
  </div>

  <div class="box pink">
    <span>Texto del cuadrado</span>
  </div>

</section>

<!--
<section>
  <article class="grid">
    <img src={landcape} alt="Image">
    <img src={landcape} alt="Image">
    <img src={landcape} alt="Image">
    <img src={landcape} alt="Image">
    <img src={landcape} alt="Image">
  </article>
</section>
!-->

<style>
  section {
    margin-block: 50px;
  }

  .box {
    border-radius: 12px;
    width: 280px;
    height: 280px;
    background-color: aquamarine;
    margin-bottom: 20px;
  }

  .box.blue {
    background-color: skyblue
  }

  .box.pink {
    background-color: pink;
  }
  .box > span {
    font-size: 20px;
    color: black;
  }

  /*
  .grid {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 15px;
    
  }
  
  .grid > img {
    border-radius: 10px;
    width: 100%;
  }
*/
</style>


