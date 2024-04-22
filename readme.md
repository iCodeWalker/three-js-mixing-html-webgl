# Three.js Mixing HMTL and WebGL

1. We will integrate HTML into the scene like if the DOM element is part of the WebGL.

2. We will add a DOM element to the HTML and this dom element will follow a point on the model.

3. Add a point example : a <div> element to out HTML file.

4. We need the point to be hidden when it is not supposed to be visible, we are going to hide it and only show it if there is a visible class on it.

5. We need to store the points.

   1. We will use an array of objects with each object corresponding to one point.
   2. Each point object will have two properties. 3D position and reference to the HTML element

6. We are going to update the points elements on each frame in the tick function.
   We need to get the 2D screen position of the 3D scene position of the point.

   Clone the point's position because we are going to convert it to the screen coordinates and we don't want to mess with the initial position.
   const screenPosition = point.position.clone()
