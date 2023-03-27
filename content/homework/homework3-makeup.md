# Homework 3 (make-up)

```{note}
You are free to discuss these questions with your classmates and on
our class slack, but you must write your own solutions, including your
own source code.

All code should be uploaded to Brightspace along with any analytic
derivations, notes, etc.
```


1. Consider a binary star system, with stars of mass $M_1$ and $M_2$.
   The equations of motion are:

   \begin{align*}
     \dot{x_1} &= u_1 \\
     \dot{y_1} &= v_1 \\
     \dot{u_1} &= G M_2 (x_2 - x_1) / r^3 \\
     \dot{v_1} &= G M_2 (y_2 - y_1) / r^3 \\
     \dot{x_2} &= u_2 \\
     \dot{y_2} &= v_2 \\
     \dot{u_2} &= G M_1 (x_1 - x_2) / r^3 \\
     \dot{v_2} &= G M_1 (y_1 - y_2) / r^3 \\
   \end{align*}

   where $r$ is the distance between the stars.

   Consider the stars to have a circular orbits.  The orbital radii, $r_1$ and $r_2$, are related by

   $$M_1 r_1 = M_2 r_2$$

   with $r = r_1 + r_2$.

   Place the center of mass at the origin of coordinates and integrate this system
   using the velocity-Verlet / _kick-drift-kick_ method that we saw in class.  Use
   a fixed timestep and integrate for 5 orbits.  

   Make a plot of the total energy of the system vs. time, where
   
   $$E = \frac{1}{2} M_1 (u_1^2 + v_1^2) + \frac{1}{2} M_2 (u_2^2 + v_2^2) - \frac{GM_1 M_2}{r}$$
