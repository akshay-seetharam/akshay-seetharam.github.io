# Polar Integration
This is my first time taking real-time notes in Obsidian. I hope it goes well.

## Review
We had specified that for some region $D$, $$\iint_D f(x, y)\,\text{d}x\,\text{d}y = \iint_D rf'(r, \theta)\,\text{d}r\,\text{d}\theta $$ where $f'(r,\theta) = f(x,y)$ using the traditional transformations of $x = r\cos(\theta)$ and $y = r\sin(\theta)$. Written more simply, this can be expressed as $\text{d}A = r\,\text{d}r\,\text{d}\theta$.
![[Pasted image 20220425142348.png]]

If we're dealing with a volume, of course $$V = \iint_D f(r, \theta)r\,\text{d}r\,\text{d}\theta.$$ We are to do the practice problems with maximum efficiency.
 ## Practice Problems and Preview of Assignment 11
 ### Paraboloid and Plane
* *Find the volume below the curve $z = x^2 + y^2$ and above the circular region in the $xy$-plane defined by $r\leq 2$ (circle of radius $2$ centered at the origin).*

The height of the parabola above the circle can be obtained as a $f(r, \theta)$ through substitutions in the paraboloid equation. $$\begin{align*} z &= x^2 + y^2  \\ &= (r\cos(\theta))^2 + (r\sin(\theta))^2 \\ &= r^2 \end{align*}$$.Next, we just integrate $z = r^2$ from $r = 0$ to $r = 2$ and $\theta$ from $\theta = 0$ to $\theta = \tau$ using $\text{d}A = r\,\text{d}r\,\text{d}\theta$. $$\begin{align*}V &= \iint_D r\,\text{d}r\,\text{d}\theta = \\ &= \int_0^\tau \int_0^2 r^3\,\text{d}r\,\text{d}\theta \\ &= \int_0^\tau 4\,\text{d}\theta \\ &= 4\tau\quad\blacksquare\end{align*}$$
### Volume of Cylinder
*a) Without doing any actual integration, what is the volume of the 3-D region defined by the circular region $r\leq 2$ in the $xy$-plane and the surface $z = x$.*

Because $z=x$ lies at a $45^\circ$ angle, exactly half of the bounded volume lies above and exactly half lies below the $xy$-plane, so the volume of the region is $0. \quad\blacksquare$
![[Pasted image 20220425145117.png]]
*b) Find the volume of part a), but for only the semicircular region in the $xy$-plane: $\{r \leq 2, x > 0\}$.*

The height from the $xy$-plane to $z=x$ is just $z = x$. We integrate from $r = 0$ to $r = 2$ and $\theta = -\frac{\tau}{2}$ to $\theta = \frac{\tau}{2}$. $$\begin{align} V &= \iint_D x\,\text{d}A \\ &= \int_{-\frac{\tau}{2}}^{\frac{\tau}{2}}\int_0^2r^2\cos(\theta)\,\text{d}r\,\text{d}\theta \\ &= \int_{-\frac{\tau}{2}}^{\frac{\tau}{2}}\frac{8}{3}\cos(\theta)\,\text{d}\theta \\ &= \frac{16}{3}\quad\blacksquare \end{align}$$
### Sphere
Find the volume of a sphere of radius $"a"$ using polar integration.

We consider the sphere centered on the origin to be the implicit function $x^2 + y^2 + z^2 = r^2$. To simplify computations, we only consider the hemisphere above the $xy$-plane such that $z^2 = r^2-x^2 - y^2 \implies z = \sqrt{r^2-x^2 - y^2}$.
![[Pasted image 20220425150054.png]]
![[Pasted image 20220425150303.png]]
Next, we simply integrate from $r = 0$ to $r = a$ and $\theta = 0$ to $\theta = \tau$, remembering to multiply by $2$ to get the volume of both hemispheres. $$\begin{align} V &= \iint_D \sqrt{r^2 - x^2 - y^2} \text{d}A \\ &= \int_0^\tau\int_0^a r\sqrt{r^2 - r^2\cos^2(\theta) - r^2\sin^2(\theta)}\,\text{d}r\,\text{d}\theta \\ &= 0\quad\blacksquare\end{align}$$
