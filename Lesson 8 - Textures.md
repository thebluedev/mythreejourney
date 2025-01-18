With native JavaScript, first, you must create an `Image` instance, listen to the `load` event, and then change its `src` property to start loading the image:

```javascript
// textures

const image = new Image();

const texture = new THREE.Texture(image);

texture.colorSpace = THREE.SRGBColorSpace

image.onload = () => {

    texture.needsUpdate = true;

}

  

image.src = '/textures/door/color.jpg'
```
this is the native / long way to load textures. three has a better way

### TextureLoader

```javascript
const texture = new THREE.TextureLoader().load('./textures/door/color.jpg')

texture.colorSpace = THREE.SRGBColorSpace
```

one texture loader can load how many every textures needed

the **load** method can be supplied with 3 call back functions
to give either of the three below status'
	load
	progress
	error

### LoadingManager

Helps keep track of 'loading' progress, when we load many different things, this helps.

```javascript
const loadingManager = new THREE.LoadingManager()
loadingManager.onStart = () =>
{
    console.log('loading started')
}
loadingManager.onLoad = () =>
{
    console.log('loading finished')
}
loadingManager.onProgress = () =>
{
    console.log('loading progressing')
}
loadingManager.onError = () =>
{
    console.log('loading error')
}

const textureLoader = new THREE.TextureLoader(loadingManager)
```
