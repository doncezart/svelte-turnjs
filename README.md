# svelte-turnjs

A Svelte 5 component library that provides a book-like page flip animation using turn.js.

## Features

- Seamless integration with Svelte 5
- Smooth page flip animations
- Customizable book layouts
- Responsive design
- Easy-to-use components

## Installation

```bash
npm install svelte-turnjs
```

## Usage

### Using a list of images

```svelte
<script>
    import { ImageFlip } from 'svelte-turnjs';
	let images =[
		"https://picsum.photos/400/600/",
        "https://picsum.photos/400/600/"
	]
	let size = [400,600] // width, height of images
</script>

<ImageFlip {size} {images} />
```

## Documentation

For detailed documentation and examples, visit our [documentation page](docs/README.md).

## Requirements

- Svelte 5
- turn.js library
- jquery

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with [Svelte](https://svelte.dev)
- Powered by [turn.js](http://www.turnjs.com)