+++
template = "page.html"
title = "Ray Tracer"
+++

# Ray Tracer

## CS 130
I took UC Riverside's undergraduate Computer Graphics class (CS130) in the Fall of 2025.
In my opinion, CS130 is easily the best computer science class at the entire university. 
It's taught by [Craig Schroeder](https://www.cs.ucr.edu/~craigs/), who is an
excellent professor. His teaching assistant is also extremely good.

## The Project
The first project in the class was a simple CPU-run ray tracer. Due to the
class's academic integrity policy, I cannot publish the code I wrote for the 
project. I've considered getting around that restriction by reimplementing the
project in a different language, but I haven't followed through with that idea
yet. Instead, I'll just show and explain some of the scenes that it can render.

The professor gave us a project template that included all the code necessary to
get started quickly; all the stuff for input parsing and vector arithmetic was already
implemented for us. All we had to do was implement the actual ray tracing math.

The project is written in C++.

We started the project by implementing the algorithm for casting rays from the 
camera, as well as the algorithm for ray-sphere intersections. That let us render
flat scenes like this:
![](images/01.png)

Then we implemented the [Phong shader](https://en.wikipedia.org/wiki/Phong_shading)
for basic diffuse and specular lighting. This was the most difficult stage of the
project for me. Not because the math is hard, but because I hadn't yet developed
the intuition for debugging vector math. Also because I didn't realize that the
Blinn-Phong model is not equivalent to the Phong model (I spent at least an hour
scratching my head trying to figure out why my specular reflections were
ever-so-slightly wrong):
![](images/13.png)

The whole point of a ray tracer is to be able to accurately render reflections
and refractions, so that was the next stage of the project:
![](images/29.png)

Handling different indexes of refraction is trivial:
![](images/30.png)

Finally, we extended the program beyond rendering spheres and into the realm of
meshes:
![](images/38.png)

We also implemented UV texture mapping:
![](images/48.png)