<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'

  onMount(() => {
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
  })
</script>

<section>
  <div class="box blue">
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
</style>