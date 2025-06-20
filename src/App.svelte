<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'
  import { SplitText } from 'gsap/SplitText'

  import Counter from './lib/Counter.svelte'
  import landcape from './assets/g9qs6xez97871.jpg'

  gsap.registerPlugin(SplitText)

  // Variable par condictional rendering
  //let seeCount = false
  /*
  const tl = gsap.timeline({
      defaults: {
        duration: 2,
        // Al completar la animacion, cambia el valor de la variable
        // para que se muestre el componente
        // onComplete: () => {
          // seeCount =true
        // }
      }
    })
  */
    /*
    // Animacion con uso de timeline
    tl.to('.box.blue', {
      x: 300,
      opacity: 0.5,
      scale: 0.5,
    })
    .to('.box.pink', {
      y: -217,
      opacity: 0.5,
      scale: 0.5,
    }, '<')
    .to('.box.yellow', {
      x: 150,
      y: -437,
      opacity: 0.5,
      scale: 0.5,
    }, '-=1.5')
    */

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

    /* Segundo ejemplo de animación
    gsap.to('.box.blue', {
      x: 300,
      opacity: 0.5,
      scale: 0.5,
      duration: 2,
    })

    gsap.to('.box.pink', {
      y: -217,
      opacity: 0.5,
      scale: 0.5,
      duration: 2,
      delay: 2
   })

    gsap.to('.box.yellow', {
      x: 150,
      y: -437,
      opacity: 0.5,
      scale: 0.5,
      duration: 2,
      delay: 3
    })
    */

    /* Animacion de una imagen
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

  <!--
  {#if seeCount}
    <Counter />
  {/if}
  -->
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


