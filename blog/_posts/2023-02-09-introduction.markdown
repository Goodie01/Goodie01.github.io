---
layout: post
author: Thomas Goodwin
title:  "Cohesion and Coupling"
date:   2023-02-09
---

When talking about Cohesion and Coupling I feel as though a major point is often missed. They are the same thing. Often talking about 

To quote wikipedia

> In software engineering, coupling is the degree of interdependence between software modules; a measure of how closely connected two routines or modules are; the strength of the relationships between modules.
> 
> Coupling is usually contrasted with cohesion. Low coupling often correlates with high cohesion, and vice versa. Low coupling is often thought to be a sign of a well-structured computer system and a good design, and when combined with high cohesion, supports the general goals of high readability and maintainability.

We can use both terms to talk about the same things.

> The classes within the authentication module should be highly cohesive
>
> The authentication module and the book checkout module should have low cohesion

Replacing "highly cohesive" with "tightly coupled" and "low cohesion" with "loosly coupled" and these statements still make complete sense.

> The classes within the authentication module should be tightly coupled
>
> The authentication module and the book checkout module should have loosly or not at all coupled

This is typically broken down to the number of ways a given "system" talks to other "systems".

![Wikipedias examplar image for Coupling Vs Cohesion](https://en.wikipedia.org/wiki/Coupling_%28computer_programming%29#/media/File:CouplingVsCohesion.svg)

Conclusion

In conclusion I want to state a better rule

> For a given boundry layer, the exposed interface, and ways we talk to other system's exposed interfaces should be limited and well considered.

A following rule I think sits nicely with this:

> Crossing a given boundry layer should happen at either a modules lowest abstraction or highest abstraction point

In this case, a abstraction layer could be a class, module, service, or our entire application.
