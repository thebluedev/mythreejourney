idk 
`meshLambertMaterial` - most performant

`import { RGBELoader } from "three/examples/jsm/loaders/RGBELoader.js";`
```javascript
rgbeLoader.load("./textures/environmentMap/2k.hdr", (environmentMap) => {

  environmentMap.mapping = THREE.EquirectangularReflectionMapping;

  

  scene.background = environmentMap;

  scene.environment = environmentMap;

});
```

use above code to load environment textures (HDRIs)
