## 15.1 Integration in Two Variables

##### Double Integral 
Intgreation of two variables 
$$\iint_D f(x,y) dA$$
- Volume of region between graph when $f(x,y) \ge 0$ on domain $D$

**Similarities Between Double and Single Integrals:**
- Double Intgerals are defined as limits of Riemann sums.
- Double integrals are evaluated using the [[Definitions#Fundamental Theorem of Calculus | Fundamental Theorem of Calculus]], but applied twice

**Integrals are broken into 3 parts**
1. Subdivision
Subdivide $[a,b]$ and $[c,d]$ by choosing partitions:
$$a=x_0 < x_1 < ... <x_N=b, \quad c = y_0<y_1<...<y_M=d$$
3. Summation
Create an $N \times M$ grid of subrectangles $R_{ij}$
5. Pasage to the limit
Choose a sample point $P_{ij}$ in each $R_{ij}$

![[Pasted image 20220228131235.png]]

##### Limit of Riemann Sums
The Riemann sum $S_{N,M}$ approaches a limit $L$ as $||P|| \rightarrow 0$ if, for all $\epsilon$ there exists $\delta > 0$  such that
$$|L-S_{N,M}| < \epsilon$$
for all partitions satisfying $||P||<\delta$ and all choices of sample points. We write 
$$\lim_{||P|| \rightarrow 0} S_{N,M}= \lim_{||P|| \rightarrow 0}\sum^N_{i=1}\sum^M_{j=1}f(P_{ij})\Delta A_{ij}=L$$
where 
$$\Delta x = \frac{b-a}{N}, \quad \Delta y = \frac{d-c}{M}$$

##### Double Integral over a Rectangle
The double integral of $f(x,y)$ over a rectangle $R$ is defined as the limit. This technique is used to find the volume of an area over a rectangle
$$\iint_R f(x,y)dA=\lim_{||P|| \rightarrow 0} \sum^N_{i=1} \sum^M_{j=1} f(P_{ij})\Delta A_{ij}$$

**Example :: Estimating Double Integral:**
> Compute the Riemann sum $S_{4,3}$ to estimate the double integral of $f(x,y)=6xy$ over $R=[1,5]×[1,4]$. Use the regular partition and upper‑right vertices of the sub‑rectangles as sample points.
> 
> 1. Calculate length of sides of subrectangle
> $$\Delta x = \frac{5-1}{4}=1, \quad \Delta y = \frac{4-1}{3}=1, \quad  \Delta A= \Delta x \Delta y = 1$$
> 2. Plug into the corresponding Riemann sum
> $$S_{4,3} = \sum^N_{i=1} \sum^M_{j=1} f(P_{ij})\Delta A_{ij}= \sum^4_{i=1}\sum^3_{j=1} (6ij)\cdot (1)$$
> 3. Sum for **Regular Partition**
> ![[Pasted image 20220228142108.png | 300]]
> $f(2,2) + f(2,3) + f(2, 4) + f(3,2) + f(3,3) + f(3, 4) +f(4,2) + f(4,3) + f(4, 4) + f(5,2) + f(5,3) + f(5, 4)  = ...$
> $6(4 + 6 + 8 + 6 + 9 + 12 + 8 + 12 + 16 + 10 + 15 + 20)=756$

##### Theorem 1: Continuous Functions Are Integrable
If a function $f$ of two variables is continuous on a rectangle $R$, then $f(x,y)$ is integrable over $R$

##### Theorem 2: Linearity of the Double Integral
Assume that $f(x,y)$ and $g(x,y)$ are integrable over a rectangle $R$. Then 
$$\text{i. } \iint_R (f(x,y) + g(x,y))dA = \iint_R f(x,y)dA + \iint_R g(x,y) dA$$
$$\text{ii. For any constant C...} \iint_R C \cdot f(x,y)dA= C \iint_R f(x,y)dA$$
**Example :: Calculating a iterated integral:**
> Evaluate the iterated integral...
> $$\int^5_1 \int^{\pi / 3} _0 x^2 \sin(y)dy dx$$
> 1. Take the inner integral (x)
> $$\int^{\pi / 3}_{x=0} x^2 \cdot \sin(y)dy =\quad x^2 \cdot [-\cos(y)]|^{\pi / 3}_0=x^2(-\cos(\frac{\pi}{3})-\cos(0))=x^2 \cdot \frac{1}{2}$$
> 2. Take the outer integral
> $$\frac{1}{2}\int^5_1 x^2dx = \frac{1}{2}[\frac{x^3}{3}]|^5_1=\frac{1}{2}(\frac{125}{3}-\frac{1}{3})=\frac{62}{3}$$

**Example :: Double Integral:**
> Evaluate the integral
> $$\iint _R \frac{23x}{y}dA, \quad R=[-2,4] \times [1,3]$$
> 1. Replace with more readable terms
> $$\iint _R \frac{23x}{y}dA = \int_{x=(-2)}^4 \int^3_1 \frac{23x}{y}dydx$$
> 2. Compute the inner integral
> $$\int^3_1 \frac{23x}{y}dy=23x\ln|y||^3_1=23x(\ln|3| - \ln |1|)$$
> 3. Compute the outer integral 
> $$(\ln|3| - \ln |1|)\int_{x=(-2)}^4 23x=(\ln|3| - \ln |1|)\cdot (\frac{23x^2}{2})|^4_{-2}=...$$
> $$(\ln|3| - \ln |1|) \cdot (\frac{23(4)^2}{2}-\frac{23(-2)^2}{2})$$
> -------
> Evaluate the integral 
> $$\iint_R y^2 \tan (x) dA,R=[0,\frac{\pi}{3}] \times [0,5]$$
> 1. Rewrite integral above
> $$\iint_R y^2 \tan (x) dA=\int^{\pi/3}_0 \int^5_0 y^2\tan(x)dydx$$
> 2. Evaluate the inner integral
> $$\tan(x)\int^5_0 y^2dy=\tan(x)(\frac{y^3}{3})|^5_0=\tan(x)(\frac{5^3}{3}-0)=\frac{125}{3}\tan(x)$$
> 3. Evaluate the outer integral
> $$\frac{125}{3} \int^{\pi/3}_0 \tan(x)=-(\frac{125}{3})(\ln|\cos(x)|)|^{\pi/3}_0=-(\frac{125}{3})(\ln|\cos(\pi/3)|-\ln|\cos(0)|)$$
> 4. Compute 
> $$-(\frac{125}{3})(\ln|\cos(\pi/3)|-\ln|\cos(0)|)=\frac{125}{3}\ln \left(2\right)$$

## 15.2 Double Integrals Over More General Regions
##### Piecewise Smooth
A multidimensional curve that acts as a boundary typically for integrals

![[Pasted image 20220313201217.png]]
##### Defining Double Integral of a Piecewise Smooth
The function $\tilde{f}$ is set equal to the function mapping the domain 
$$\iint_D f(x,y)dA = \iint_R \tilde{f}(x,y)dA$$
$$\tilde{f}(x,y)= \{f(x,y) \text{ if } (x,y) \in D \quad \& \quad 0 \text{ if } (x,y) \not\in D\}$$
![[Pasted image 20220313202257.png | 300]]
- function $f$ is integral over $D$ if the integral of $\tilde{f}$ over $R$ exists (as all shown in the image above)

##### Theorem 1
If $f(x,y)$ is continuous on a closed domain $D$ whose boundary is a simple closed piecewise smooth curve, then $\iint_D f(x,y)dA$ exists

#### Computing Regions Between Two Graphs
When $D$ is a regoin between two graphs in the xy-plane, we can evaluate double integrals over $D$ as interated integrals. Since $D$ is vertically simple if it is the region between the graph of two continuous functions $y=g_1(x)$ and $y=g_2(x)$ over a fixed interval.
$$D=\{(x,y):a \le x \le b, \quad g_1(x) \le y \le g_2 (x)$$
If $D$ is **horizontally simple**
$$D=\{(x,y):c \le y \le d, \quad h_1(y) \le x \le h_2 (y)$$

##### Theorem 2
If $D$ is **vertically simple** with description
$$D=\{(x,y):a \le x \le b, \quad g_1(x) \le y \le g_2 (x)$$
then, 
$$\iint_D f(x,y)dA=\int^b_a \int^{g_2(x)}_{g_1(x)} f(x,y)dydx$$
If $D$ is **horizontally simple** with description
$$D=\{(x,y):c \le y \le d, \quad h_1(y) \le x \le h_2 (y)$$
then,
$$\iint_D f(x,y)dA=\int^d_c \int^{h_2(x)}_{h_1(x)} f(x,y)dxdy$$

**Note:**
Since $\tilde{f}(x,y)$  is zero outside $D$, so for fixed x, $\tilde{f}(x,y)$ is zero unless y satisfies $g_1(x) \le y \le g_2(x)$ giving us
$$\int^d_c \tilde{f}(x,y)dy = \int^{g_2(x)}_{g_1(x)} f(x,y)dydx$$
**Integration over a horizontally or vertically simple region is similar to integration over a rectangle with one difference: The limits of the inner integral may be functions instead of constants.**

**Example :: Compute double integral over domain D**
> Compute the double integral of $f(x,y)=x^2y$ over the given shaded domain in the figure. Assume that $a=1$.
> 1. Describe $D$ as a vertically simple region.
> $$0 \le x \le (2a=2), \quad f(x)=? \le y \le a$$
> 2. We need to find the function $f(x)$ along the piecewise smooth. Knowing that we go right (2) a's for every down (1) a we can create a function mapping to 
> $$f(x)=\frac{y}{x}=a - \frac{1}{2}x=1- \frac{1}{2}x$$
> Now we can plug into our equation with value $a=1$ ...
> $$0 \le x \le 2, \quad 1- \frac{1}{2}x \le y \le 1$$
> 
> ![[Pasted image 20220314091106.png | 200]] 
> This segment is horizontally simple since the x value doesn't change in this piecewise smooth but the y-compontent does
> 3. Set up the iterated integral
> $$\iint_D x^2ydA = \int^2_0 \int^1_{y=(1 - \frac{1}{2}x)}x^2y \space dydx$$
> 4. Solve for y on the inner integral
> $$\int^1_{y=(1- \frac{1}{2}x)}x^2y \space dy=\int^2_0= \frac{1}{2}x^2y^2 \space \vert^1_{y=(1- \frac{1}{2}x)}= \int^2_0 x^2\left(\frac{1}{2}-\frac{\left(2-x\right)^2}{8}\right)dx$$
> 5. Solve for x on the outer integral with the new input value
> $$\int^2_0 x^2\left(\frac{1}{2}-\frac{\left(2-x\right)^2}{8}\right)dx= \int^2_0 \frac{x^2}{2} - \frac{x^2(2-x)^2}{8} = 2 - \frac{4}{5}=1.2$$
> ANS: $1.2$
> ---
> Compute the double integral of $\iint_D x^3y \space dA$ over the domain $D$ over $0 \le x \le 3, \quad x \le y \le 5x + 3$ 
> Rewrite:
> $$\int^3_0 \int^{5x+3}_x x^3 y \space dydx$$
> 1. Calculate the inner integral
> $$\int^{5x+3}_x x^3 y \space dy=\frac{1}{2}x^3y^2 \vert_x^{5x+3}=\frac{x^3(9+30x+24x^2)}{2}$$
> 2. Plug in the new value of the inner integral into the outer integral
> $$\int^3_0\frac{x^3\left(9+30x+24x^2\right)}{2}dx=\frac{18225}{8}$$
> ANS: $\frac{18225}{8}$ 
> ---
> Compute the double integral $\iint_D (70xy-x^2) \space dA$ over the region bounded below by $y=x^2$, above by $y=\sqrt{x}$. 
> 1. Find the bounds of the outer integral
> $$x^2 = \sqrt{x}, \quad x = 0,1$$
> 2. Rewrite the integral 
> $$\int^1_0 \int_{x^2}^{\sqrt{x}}(70xy-x^2) \space dydx$$
> 3. Compute the inner integral
> $$\int_{x^2}^{\sqrt{x}}(70xy-x^2) \space dy=35xy^2-x^2 \vert_{x^2}^{\sqrt{x}}=-x^2\sqrt{x}+x^4-35x^5+35x^2$$
> 4. Compute the outer integral
> $$\int^1_0(-x^2\sqrt{x}+x^4-35x^5+35x^2) \space dx=\frac{1207}{210}$$
> ANS: $\frac{1207}{210}$

#### Changing the Order of Integration
> Change the order of integration
> $$\int^b_a \int^{g_2(y)}_{g_1(y)} f(x,y)= \int^8_0 \int^8_x xe^{y^{3/64}}\space dydx$$
> $$0 \le x \le 8, \quad x \le y \le 8$$
> $$\int^8_0 \int^8_y xe^{y^{3/64}} \space dxdy=\int^8_0 \left(32e^{y^{\frac{3}{64}}}-\frac{y^2e^{y^{\frac{3}{64}}}}{2}\right)dy=$$
> $$\int^8_0 \frac{x^2e^{y^{3/64}}}{2} \vert^8_y=\int^8_0 \frac{64e^{y^{3/64}}}{2}- \int^8_0\frac{y^2e^{y^{3/64}}}{2}$$
> $$ \frac{ 3 e^{y^{3/64}}}{2y^{61/64}}- \frac{3y^3e^{y^{3/64}}}{6 * 64y^{61/64}}$$
> $$du$$
> ---
> Change the order of integration
> $$\int^9_0\int^3_{\sqrt{y}} \sqrt{x^3 + 4} \space dx dy$$
> 1. Use your imaginaton...
> $$\int^3_0\int^{x^2}_0 \sqrt{x^3+4} \space dxdy=\frac{62\sqrt{31}-16}{9}$$


##### Theorem 3
Let $f(x,y)$ and $g(x,y)$ be integrable functions on $D$
1. If $f(x,y) \le g(x,y)$ for all $(x,y) \in D$ then,
$$\iint_D f(x,y)dA \le \iint_D g(x,y)dA$$
2. If $m \le f(x,y) \le M$ for all $(x,y) \in D$ then 
$$m \cdot area(D) \le \iint_D f(x,y)dA \le M \cdot area(D)$$

#### Average Value
The average (mean) value of a function on domain $D$ is denoted as $\overline{f}$ 
$$\overline{f}=\frac{1}{area(D)} \iint_D f(x,y)dA=\frac{\iint_D f(x,y)dA}{\iint_D 1dA}$$
The value of $\overline{f}$ satisfies this relationship
$$\iint_D f(x,y)dA=\overline{f} \cdot area(D)$$
##### Theorem 4: Mean Value Theorem for Double Integrals
If $f(x,y)$ is continuous and $D$ is closed, bounded, and connected, then there exists a point $P \in D$ such that 
$$\iint_D f(x,y)dA=f(P)area(D)$$
Equivalently, $f(P)=\overline{f}$ where $\overline{f}$ is the average value of $f$ on $D$. 

**Note:**
The mean value theorem for double integrals only applies to continuous functions, therefore meaning they lie on the same domain
![[Pasted image 20220314190914.png | 300]]




**Example :: Find volume from 3 points in 3D space:**
> Calculate the double integral of $f(x,y)=5-8x$ over the triangle with verticies $O=(0,0),A=(2,7),B=(6,7)$
> $$\iint_D(5-8x)dA$$
> $$\int^7_0 \int_{\frac{2}{7}y}^{\frac{6}{7}y}(5-8x)dxdy=-\frac{686}{3}$$
> $$\int^6_0 \int^{7x/2}_{6x/2}(5-8x)dxdy$$
> ---
> Find the volume of the region bounded by $z=72-y,\quad z=y,\quad y=x^2, \quad y=36-x^2$
> $$z=72-(z),\quad z=36, \quad x^2=36-x^2, \quad x=\sqrt{18}, \quad y=18$$
> 

**Example :: Estimating area of the subdomain:**
> Using the table below find the average area of the list of sub-domains
> ![[Pasted image 20220314191152.png | 400]]
> Estimate $\iint_D f(x,y) dA$
> $$\iint_D f(x,y)dA=f(P)area(D)_1 + f(P)area(D)_2 + ...$$
> $$=1.4 * 8.6 + 0.7 * 8.6 + 0.9 * 8.5 + 0.9 * 9.1 + 1.1 * 8.5 + 1.1 * 9.1= 53.26 $$



## 15.3 Triple Integrals
Similar to double integrals except there is another degree of restriction
$$B=[a,b] \times [c,d] \times [p,q]$$
such that all points in $\mathbb{R}^3$ 
$$a \le x \le b, \quad c \le y \le d, \quad p \le z \le q$$
![[Pasted image 20220316192131.png | 300]]

To integrate over this box we subdivide the box into subboxes
$$B_{ijk}=[x_{i-1},x_i] \times [y_{j-1},y_j] \times [z_{k-1}, z_k]$$
by choosing partitions of the three intervals
$$a= x_0 < x_1 < ... < x_N = b$$
$$c = y_0 < y_1 < ... < y_M = d$$
$$p = z_0 < z_1 < ... < z_L = q$$

Here, N, M, and L are positive integers. The volume of $B_{ijk}$ is $\Delta V_{ijk}=\Delta x_i, \Delta y_j, \Delta z_k$  where 
$$\Delta x_i = x_i - x_{i-1}, \quad \Delta y_j = y_j - y_{j-1}, \quad \Delta z_k = z_k - z_{k-1}$$
Then we choose a sample point $P_{ijk}$ in each subbox $B_{ijk}$ and form the Riemann sum...
$$S_{N,M,L}=\sum^N_{i=1}\sum^M_{j=1}\sum^L_{k=1} f(P_{ijk}) \Delta V_{ijk}$$
We write $P=\{\{x_i\},\{y_j\},\{z_k\}\}$ for the partition and let $||P||$ be the maximum of the widths $\Delta x_i, \Delta y_j, \Delta z_k$. If the sums $S_{N,M,L}$ approach a limit as $||P|| \rightarrow 0$  for arbitrary choices of sample points, we say that $f$ is **integrable** over $B$. The limit value is denoted
$$\iiint_B f(x,y,z)dV = \lim_{||P|| \rightarrow 0} S_{N,M,L}$$

##### Theorem 1: Fubini's Theorem for Triple Integrals
The triple integral of a continuous function $f(x,y,z)$ over a box $B= [a,b] \times [c,d] \times [p, q]$ is equal to the iterated integral 
$$\iiint_B f(x,y,z)dV= \int^b_{x=a}\int^d_{y=c}\int^q_{z=p}f(x,y,z)dz \space dy \space dx$$
Furthermore, the iterated integral can be evaluated in any order

**Example :: Triple Integral:**
> Evaluate 
> $$\iiint_B (xz + yz^2) dV \text{ for box: } 0 \le x \le 4, \quad 2 \le y \le 4, \quad 0 \le z \le 4$$
> 1. Rewrite:
> $$\int^4_0 \int^4_2 \int^4_0 (xz + yz^2)dzdydx$$
> 2. Evaluate the inner integral
> $$\int^4_0(xz + yz^2)dz=\frac{1}{2}xz^2 + \frac{1}{3}yz^3 \vert^4_0=\frac{1}{2}x(4)^2 + \frac{1}{3}y(4)^3-(0)= 8x + \frac{64}{3}y$$
> 3. Evaluate the middle integral
> $$\int^4_2(8x + \frac{64}{3}y)dy = 8x + \frac{32}{3}y^2 \vert^4_2 = 8x(4) + \frac{32}{3}(4)^2 - \left( 8x(2) \frac{32}{3}(2)^2 \right) = 16x + 128$$
> 4. Evaluate the outer integral
> $$\int^4_0 (16x + 128)dx = 8x^2 + 128x \vert^4_0 = 640$$

##### Theorem 2
The triple integral of a continuous function $f$ over the region
$$ W \quad : \quad (x,y) \in D, \quad z_1(x,y) \le z \le z_2  \space (x,y)$$
is equal to the iterated integral
$$\iiint_W f(x,y,z) \space dV = \iint_D \left( \int^{z_2(x,y)}_{z=z_1(x,y)} f(x,y,z)dz\right)dA$$
**Note:**
More generally, integrals of functions of $n$ variables (for any $n$ ) arise naturally in many different contexts. For example, the average distance between two points in a ball in $R^3$ is expressed as a six-fold integral because we integrate over all possible coordinates of the two points. Each point has three coordinates for a total of six variables.

The volume of a region $W$ is defined as 
$$V=\iiint_W 1dV$$

**Example :: Integrating inner integral with equations:**
> Integrate $f(x,y,z)=x$ over the region $W$ in the first octant above $z=y^2$ and below $z=80-5x^2 -4y^2$ 
> Rewrite:
> $$\iint_D \int^{80-5x^2-4y^2}_{z=y^2}x$$
> 1. Now we find the ranges for the next two integrals. Knowing that the first quadrant starts at $x=0$ and $y=0$ we can assume those are the bottom constraints. For the top constaints we can set the two equations equal to one another
> $$80-5x^2-4y^2 = y^2, \quad 16 - x^2 = y^2, \quad x^2 + y^2 = 16, \quad x = 4, y = \sqrt{16-x^2}$$
> 3. Now we rewrite the integral
> $$\int_0^4 \int_0^{\sqrt{16-x^2}} \int^{80-5x^2-4y^2}_{z=y^2}x$$

> 4.  Calculate:
> $$\int_0^4 \int_0^{\sqrt{16-x^2}} \int^{80-5x^2-4y^2}_{z=y^2}x = \frac{2048}{3}$$
> ----
> Find the triple integral of the function $F(x,y,z)=z$ over the region in the figure. Assume that $a=3, b=5, c=6$
> 1. 
> 