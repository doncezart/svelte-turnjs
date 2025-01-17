<script>
    import { onMount, onDestroy } from 'svelte';
    import { browser } from '$app/environment';
      export let size, images;
    
    let bookElement;
    let jQueryInstance;
    
    onMount(async () => {
      if (browser) {
        jQueryInstance = (await import('jquery')).default;
        window.jQuery = jQueryInstance;
        await import('$lib/components/turn.js');
        
        jQueryInstance(bookElement).turn({
          width: size[0]*2,
          height: size[1],
          autoCenter: true,
          gradients: true,
          acceleration: true
        });
      }
    });
  
    onDestroy(() => {
      if (browser && bookElement && jQueryInstance) {
        jQueryInstance(bookElement).turn('destroy');
      }
    });
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