snabbt.js
========
Arbitrary DOM animations. (WIP)


Basic usage
-----------

	snabbt(e, {
	  start_pos: [0, 0, 0],
	  end_pos: [10, 10, 10],
	  start_rot: [0, 0, 0],
	  end_rot: [0, 0, 0],
	  duration: 100,
	  easing: 'linear'
	});


Chaining animations
-------------------

    snabbt(e, {
	  start_pos: [0, 0, 0],
	  end_pos: [10, 10, 10],
	  duration: 200,
	  easing: 'cos',
	}).then({
	  start_pos: [0, 0, 0],
	  end_rot: [0, 0, 0],
	  duration: 100,
	});

Chaining animations
-------------------
The following easing function are present:

 - 'linear'
 - 'cubic'
 - 'atan'
 - 'cos'
 - 'sinc_wobbler'

Under the hood
--------------
matrix3d and requestAnimationFrame so performance seems to be decent.