# Homework 2 (make-up)

```{note}
You are free to discuss these questions with your classmates and on
our class slack, but you must write your own solutions, including your
own source code.

All code should be uploaded to Brightspace along with any analytic
derivations, notes, etc.
```


1. Consider the  gamma function,

   $$\Gamma(a) = \int_0^\infty x^{a-1} e^{-x} dx$$

   We want to evaluate this numerically.  Consider a variable 
   transformation of the form:

   $$z = \frac{x}{x + c}$$

   as we saw in class.  This will map $x \in [0, \infty)$ to $z \in
   [0, 1]$, allowing us to do this integral numerically in terms of
   $z$.

   For convenience, we express the integrand as $\phi(x) = x^{a-1} e^{-x}$.  

   * For what value of $x$ is the integrand $\phi(x)$ maximum?

   * Choose the value $c$ in our transformation such that the 
     peak of the integrand occurs at $z = 1/2$---what value is $c$?

     This choice spreads the interesting regions of integrand over
     the domain $z \in [0,1]$, making our numerical integration 
     more accurate.

   * Find $\Gamma(a)$ for a few different value of $a$ using and
     numerical integration method you wish, integrating from $z = 0$ to
     $z = 1$.  Keep the number of points in your quadrature to a
     reasonable amount ($N \lesssim 50$).

     Don't forget to include the factors you pick up when changing
     $dx$ to $dz$.

     Note that roundoff error may come into play in the integrand.
     Recognizing that you can write $x^{a-1} = e^{(a-1)\ln{x}}$ can
     help minimize this.

