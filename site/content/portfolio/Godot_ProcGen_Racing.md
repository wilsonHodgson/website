---
title: "Godot Procedural Generated Racing"
subtitle: ""
summary: "This is an ongoing project to explore how procedural generated content would fit into racing games."
date: 2018-09-09T00:02:07-05:00
featured_image: "Godot_ProcGen_Racing.png"
draft: false
---
This is an ongoing project to explore how procedural generated content would fit into racing games.

## My experience
The most thrilling part of this project was when I attempted to take a Spline curve and coerce it's approximation into an OpenGL buffer for rendering and collision calculations.
When I attempted this I knew what I needed was an interpolation along the spline, calculating the tangent so that I could place points offset from the curve by a magnitude along the normal.
The interface in Godot provided an interpolation function, but no method to calculate the tangent. This I knew was basic calculus, but I hadn't calculated a derivative in years.

Instead I recalled that a derivative can be conceptualized as a rate calculation over an immeasurably small distance.
So my quickest solution to get something close to a tangent was to interpolate along the spline to the desired position 
$$ x $$
Then, to interpolate to the position after it in the smallest magnitude (lets say). 
$$ x + 0.000001 $$

When I attempted this approach I was skeptical, but when I ended up rendering it the result was so close to what I desired that I ended up keeping it for the final draft! (after a bit of knob twiddling).
So the lesson learned is that if your reasoning skills are strong enough, then it is often best to remember the basic concepts of a study, and then derive the specific concepts when needed.

## Check it out

- [Source Code](https://github.com/wilsonHodgson/Track-Generation) 
