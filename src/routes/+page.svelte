<script>
    import { ImageFlip } from '$lib/index.js'
    let images =[
		"https://raw.githubusercontent.com/blasten/turn.js/refs/heads/master/demos/magazine/pages/01.jpg",
		"https://raw.githubusercontent.com/blasten/turn.js/refs/heads/master/demos/magazine/pages/02.jpg",
		"https://raw.githubusercontent.com/blasten/turn.js/refs/heads/master/demos/magazine/pages/03.jpg",
		"https://raw.githubusercontent.com/blasten/turn.js/refs/heads/master/demos/magazine/pages/04.jpg"
	]
	let size = [400,600]
</script>

<ImageFlip {size} {images} />