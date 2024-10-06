# The Biggest Lie in Video Games

{% embed url="https://www.youtube.com/watch?v=Qk_O-q_9YIQ&list=WL&index=2" %}

## Why is Fluid Simulation is Hard in Game Development?
Fluid simulation in gaming is difficult primarily because of the computational complexity involved in realistically simulating fluid behavior in real time. Fluids (like water, smoke, or lava) have highly dynamic properties that are influenced by many factors, including gravity, pressure, viscosity, turbulence, and interactions with other objects. Achieving realistic behavior while maintaining performance on consumer hardware is a challenge. Here’s why:

1. **Physics Complexity**: Fluids follow the Navier-Stokes equations, which describe how the velocity field of a fluid evolves. Solving these equations in real time for each frame in a video game is computationally expensive, especially for large volumes or highly detailed simulations.
2. **Real-Time Requirements**: Games typically aim to run at 30, 60, or even higher frames per second. Achieving this speed while simulating the fluid accurately can be very taxing on the CPU and GPU. Developers often need to make trade-offs between accuracy and performance.
3. **High Degree of Detail**: Fluids can exhibit a wide range of behaviors, such as splashing, dripping, and swirling. Simulating these nuances adds extra layers of difficulty, especially when fluid interacts with objects or characters in the game.
4. **Large Scale Simulations**: In open-world games or large environments, the sheer scale of fluid simulations can become overwhelming. Simulating oceans, rivers, or dynamic weather patterns (like storms) requires simplifying the physics, which can lead to unrealistic results if not handled carefully.
5. **Optimization Techniques**: Techniques like particle-based methods (SPH), voxel grids, and simplified physics models help, but they still require balancing accuracy and performance. Some games pre-calculate fluid behavior (baked simulations), but this limits real-time interactivity.
6. **Graphics and Rendering**: Fluids must not only behave correctly but also look good. Reflections, refractions, transparency, and surface tension effects add to the graphical load, further complicating real-time fluid simulation.

While advances in hardware and game engines have led to improvements in fluid simulation (like in games using Unreal Engine or Unity), real-time simulation that is both physically accurate and visually impressive remains challenging.

## What is Vertex Displacement?
**Vertex displacement** in game development refers to the process of altering the position of vertices (the points that make up 3D models) dynamically, typically during runtime or in the shader pipeline. This technique is used to modify the surface of a mesh, creating more detailed and complex animations or surface deformations without needing to modify the mesh geometry itself.

### How It Works:
- **Vertices** are the building blocks of a 3D model. A mesh is made up of a network of connected vertices that define its shape. 
- In **vertex displacement**, the position of each vertex is modified based on an algorithm or mathematical function, often using data like noise textures, height maps, or mathematical equations. 
- This process is usually handled by **vertex shaders**, which are part of the graphics pipeline and run on the GPU. The vertex shader receives the mesh's vertices and processes them to compute their new positions.

### Common Applications:
1. **Terrain Deformation**: Creating dynamic landscapes (hills, mountains, etc.) by using height maps or procedural noise to push or pull vertices. 
2. **Water Simulation**: Displacement can be used to animate realistic waves and water surfaces by applying noise functions to vertex positions. 
3. **Character Deformation**: Adjusting the shape of a character's skin or clothing in response to interactions, like muscles bulging or fabric rippling. 
4. **Destruction Effects**: Simulating explosions or impacts by displacing vertices to make surfaces look broken or damaged. 
5. **Procedural Effects**: Generating organic or chaotic surface details on objects without adding more geometry, making the object appear more complex without increasing computational cost.

### Advantages:
- **Efficient**: Since displacement happens in the shader, it doesn't require modifying or increasing the polygon count of the original model. This helps in maintaining performance while enhancing visual detail. 
- **Dynamic**: You can adjust the displacement in real-time, allowing for interactive effects like shifting terrain or moving water.

### Disadvantages:
- **Limited Detail**: The amount of detail in displacement depends on the density of the mesh. If there are not enough vertices, displacement won’t create fine details.
- **Performance Costs**: Although efficient, complex displacement effects can still be GPU-intensive, especially for high-resolution meshes or large environments.

## What is GOBO?
A **gobo** is a stencil or template used in lighting design to control the shape of the light that passes through it. The term is most commonly used in theatrical lighting, photography, and cinematography but also finds application in game development and virtual production.

### Gobo in Different Contexts:
1. **Theater and Film**: 
	- A gobo is placed in front of a light source, usually a stage light or spotlight, to project specific patterns, shapes, or textures onto a surface, such as a stage floor, wall, or background. 
	- Gobos can be made from metal or glass. Metal gobos create simple patterns (like leaves, grids, or abstract shapes), while glass gobos can display more complex images and even color effects. 
	- They are often used to simulate effects such as light coming through windows, creating foliage shadows, or adding intricate designs to a scene.
2. **Photography**: 
	- In photography, a gobo is often used to block or shape light. Photographers might use gobos to prevent light from spilling onto certain areas of a scene or to create specific lighting effects (e.g., casting shadows with patterns).
3. **Game Development and Virtual Production**:
	- In 3D rendering and game development, a **gobo** functions similarly to its real-world counterpart by shaping light or creating patterned shadows. Artists may simulate gobo effects in virtual environments to enhance lighting realism, cast dynamic shadows, or mimic the look of a light source passing through an object (e.g., casting tree shadows on the ground). 
	- In game engines like **Unreal Engine** or **Unity**, gobos can be simulated by using **light cookies** which are texture maps applied to light sources to project a specific pattern.

### How Gobos are Used:
- **Texture and Mood**: Gobos are widely used to add texture and depth to lighting. For example, projecting a window gobo on a stage can give the impression that light is coming from an actual window. 
- **Environmental Simulation**: Gobos can simulate environmental effects, like sunlight filtering through trees, giving a scene more atmosphere. 
- **Scene Design**: They're used to create compelling visual compositions, controlling how light interacts with characters and objects for dramatic or aesthetic effects.

### Example Applications:
- In a **theater** production, a gobo could be used to simulate the shadow of leaves on the stage to give the impression of an outdoor setting. 
- In **games**, a developer could use a gobo-like texture to cast the shadow of a barred window across a character's face, enhancing the mood of a scene.

### Summary:
A **gobo** is a versatile lighting tool used to shape or block light to create specific shadows or lighting effects. It’s a powerful tool in both physical and virtual settings for adding depth, texture, and atmosphere to a scene.