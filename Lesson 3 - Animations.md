`window.requestAnimationFrame()`
used to call a function each frame.

used to rerender and also change whatever properties.

using this to change properties can lead to inconsistencies across devices due to framerate

either use time to change it 
	THREE.Clock()
or use gsap