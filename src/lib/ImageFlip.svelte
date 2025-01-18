<script lang="js">
    import { onMount } from 'svelte'
  
    let { size, images } = $props()
    let bookElement
    
    async function init() {
      const jQuery = (await import('jquery')).default
      await import('./turn.js')
      
      jQuery(bookElement).turn({
        width: size[0]*2,
        height: size[1],
        autoCenter: true,
        gradients: true,
        acceleration: true
      });
  
      return () => jQuery(bookElement).turn('destroy')
    }
    
    onMount(() => init())
  </script>
  
  <div class="book-container">
    <div bind:this={bookElement} class="book">
          {#each images as image}
              <img width={size[0]} height={size[1]} src={image} alt="Page">
          {/each}
    </div>
  </div>
  
  <style>
    .book-container {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
    }
    
    .book {
      margin: 0 auto;
    }
  </style>