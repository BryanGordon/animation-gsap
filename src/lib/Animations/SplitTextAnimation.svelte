<script>
  import { onMount } from 'svelte'
  import { gsap } from 'gsap'
  import { SplitText } from 'gsap/SplitText'

  // Uso del registro de puglins
  gsap.registerPlugin(SplitText)

  onMount(() => {
    const splitText = new SplitText('h1', {
      // Se puede utilizar type con valores como 'lines', 'words', 'chars'
      type: 'lines',
    })

    gsap.from(splitText.lines, {
      duration: 1.5,
      y: 100,
      //opacity: 0,
      autoAlpha: 0, // Hace algo parecido a opacity, pero con display none
      stagger: 0.5,
      filter: "blur(5px)"
    })
  })
</script>

<section>
  <h1>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Itaque quasi laborum tempore enim maxime exercitationem distinctio quam molestiae magni ex?</h1>
</section>

<style>
  h1 {
    color: skyblue;
    text-align: center;
    font-size: 25px;
    text-wrap: balance;
  }
</style>