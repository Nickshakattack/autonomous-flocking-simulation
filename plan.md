What I'm Modeling:
A Boid class to represent each autonomous agent.

A Flock class to manage the array of Boids and their interactions.

Variables and Data Structures:
ArrayList<Boid> flock: stores all boid objects.

Constants for weights of different behaviors: SEPARATION_WEIGHT, ALIGNMENT_WEIGHT, COHESION_WEIGHT.

Parameters like maximum speed and force for limiting velocity and acceleration.

Setup:
Create a canvas.

Initialize a Flock object.

Add a set number of Boids to the flock with random starting positions and velocities.

Flow of draw():
Clear the background.

Update and display each boid in the flock.

Each boid:

Applies flocking behaviors.

Updates its velocity and position.

Wraps around edges if needed.

Draws itself on the screen.

Classes:
Boid
Properties:

PVector position

PVector velocity

PVector acceleration

float maxForce

float maxSpeed

Methods:

update(): Update position based on velocity and acceleration.

applyForce(PVector force): Add a force to acceleration.

flock(ArrayList<Boid> boids): Calculates steering based on neighbors.

separation(...), alignment(...), cohesion(...): Steering rules.

edges(): Handle screen wrap-around.

show(): Draw the boid on screen.

Flock
Properties:

ArrayList<Boid> boids

Methods:

addBoid(Boid b): Add a new boid to the flock.

run(): Calls update() and show() for all boids.

Optional Additions (if time permits):
Add mouse interaction to spawn new boids.

Sliders to adjust weights of separation, alignment, and cohesion.

Add predator agents or obstacles to avoid.
