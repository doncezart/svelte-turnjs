<script>
    import { ImageFlip } from '$lib/index.js'
  
    let images = [
      'https://picsum.photos/400/600/',
      'https://picsum.photos/400/600/',
    ]
    let size = [400, 600]
  </script>
  
  <ImageFlip {size} {images} />