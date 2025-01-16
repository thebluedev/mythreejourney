## Every Three Scene needs to have

### 1. A Scene
`const scene = new THREE.Scene();`
### 2.  Some Objects
The objects contain the geometry 
`const mygeo = new THREE.SphereGeometry(1, 32);`
and material 
`const material = new THREE.MeshBasicMaterial({color: 0xff0000,wireframe:true});`
which are made into a mesh
`const mesh = new THREE.Mesh(mygeo, material);`
### 3. A Camera
`const camera = new THREE.PerspectiveCamera(75, sizes.width / sizes.height);`
### 4. A Renderer

`const renderer = new THREE.WebGLRenderer({ canvas });`

the renderer, needs a size to be set

`renderer.setSize(sizes.width, sizes.height);`

All of which have to be added to the `scene` 
	`scene.add(mesh)`
	`scene.add(camera)`
