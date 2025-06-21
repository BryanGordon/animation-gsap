<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'

  const tl = gsap.timeline({
    defaults: {
      duration: 2,
    }
  })

  // Funciones para controlar el timeline
  const handlePlay = () => {
    tl.play()
  }

  const handlePause = () => {
    tl.pause()
  }

  const handleRestart = () => {
    tl.restart()
  }

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

<section>
  <div class="button-container">
    <button on:click={() => handlePlay()}>Play</button>
    <button on:click={() => handlePause()}>Pause</button>
    <button  on:click={() => handleRestart()}>Restart</button>
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

  .button-container {
    width: 100%;
    display: flex;
    justify-content: center;
    gap: 20px;
  }

  button {
    padding: 10px;
    border-radius: 5px;
    text-align: center;
    cursor: pointer;
    border: none;
    color: white;
  }
</style>