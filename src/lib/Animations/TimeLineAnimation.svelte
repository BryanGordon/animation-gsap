<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'

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

  onMount(() => {
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
  })
</script>

<section>
  <div class="box blue">
    <span>Texto del cuadrado</span>
  </div>

  <div class="box pink">
    <span>Texto del cuadrado</span>
  </div>

  <div class="box yellow">
    <span>Texto del cuadrado</span>
  </div>
</section>

<style>
  .box {
    border-radius: 12px;
    width: 200px;
    height: 200px;
    background-color: aquamarine;
    margin-bottom: 20px;
  }

  .box.blue {
    background-color: skyblue
  }

  .box.pink {
    background-color: pink;
  }

  .box.yellow {
    background-color: yellow;
  }

  .box > span {
    font-size: 20px;
    color: black;
  }
</style>