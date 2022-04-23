##### Question 1: 
(1) We have a thin metal plate on the part of $x^2 + y^2 \le 9$ in the first quadrant which has a density of $\rho(x,y) = Kx - K^3 y$, in $kg/m^3$. Determine the value of $K$ which makes the metal plate have the maximum mass, and then determine this maximal mass.

1. mass = $\iint_S \delta (x,y,z)dS$ 
2. $g(x,y) = x^2 + y^2 - 9$ 
	1. $g_x = 2x$
	2. $g_y = 2y$
3. Find $dS$
	1. $dS = \sqrt{1 + g_x^2 + g^2_y}dxdy = \sqrt{1 + 4x^2 + 4y^2}dydx$ 
4. Find x
	1. $x = \sqrt{\frac{9}{y^2}}$ 
5. Plug in x
	1. $\rho(x,y) = K(\sqrt{\frac{9}{y^2}}) - K^3 y = \frac{3K}{y} - K^3 y$  
	2. $3K = K^3y^2$ ; $y^2 = 3K^2$; $K = \sqrt{y^2/3}$ 
6. Plug in y
	1. ANS: $K = \frac{1}{\sqrt{3}}$ 
---
##### Question 2: 

(2) An object is moving along the path $\langle t^2, t-t^3 \rangle$ for which starting when $t = -1$. The object is in the presence of a force field $F(x,y) = \langle y, x \rangle$ 
1. Find a function which calculates the work done by the vector field if the object moves until $t=T$?
	1. $r(t) = \langle t^2, t-t^3 \rangle$
	2. $r'(t) = \langle 2t, 1-3t^2 \rangle$ 
	3. $F(r(t)) = \langle t - t^3, t^2 \rangle$
	4. $$\int^T_{-1} F(r(t)) \cdot r'(t) = \langle t - t^3, t^2 \rangle \cdot \langle 2t, 1-3t^2 \rangle = \int^T_{-1} 2t^2 - 2t^4 + t^2 - 3t^4$$
	5. $$= \int^T_{-1} -5t^4 + 3t^2 = t^3 -t^5 \Big |^T_{-1} = T^3 - T^5 - 0 = T^3-T^5$$
	6. ANS: $T^3 - T^5$
2. After how many seconds is the work done maximized?
	1. $\frac{d}{dT}(T^3 - T^5) = 3T^2 - 5T^4$ 
	2. $T^2(3 - 5T^2)$ 
	3. separate T and take the square root
	4. ANS: $\sqrt{\frac{3}{5}}$

----
##### Question 3: 
(3) Let $D$ be the part of the plane $x + 2y - z = 0$ which lies inside the cylinder $x^2 + y^2 = 9$
1. Give a parametrization for $D$
	1. $0 \le t \le 3$ and $0 \le \theta \le 2 \pi$ 
	2. $z = x + 2y$
	3. $D(t, \theta) = \langle t \cos \theta, t \sin \theta, t \cos \theta + 2t \sin \theta \rangle$  
2. Calculate the surface area for $D$
	1. $D(t, \theta)_t = \langle \cos \theta, \sin \theta, \cos \theta + 2\sin \theta \rangle$
	2. $D(t, \theta)_{\theta} = \langle -t \sin \theta, t \cos \theta, -t \sin \theta + 2t \cos \theta \rangle$ 
	3. 
	4. $$\begin{bmatrix} i & j & k \\ -t \sin \theta & t \cos \theta & -t \sin \theta + 2t \cos \theta \\ \cos \theta & \sin \theta & \cos \theta + 2\sin \theta\end{bmatrix} = \langle t\cos ^2\theta+t\sin ^2\theta, 2t\cos ^2\theta+2t\sin ^2\theta , -t\sin ^2\theta - t\cos ^2\theta \rangle$$
3. Let $C$ be the boundary of $D$, oriented counter-clockwise when viewed from above. Give a parametrization for $C$.
4. Set up an integral to calculate the arc length of $C$
5. (C) Use an online calculator to evaluate the integral

----
##### Question 4: 
(4) A wire is parametrized by $\langle \frac{t^2}{2}, 5t-3, 3-t^2 \rangle$ from $0 \le t \le 1$. 
1. The density of the wire is given $\rho(x,y,z) = \sqrt{x}$  g/cm. What is the total mass of the wire?
	1. $f(r(t)) ||r'(t)||dt$
	2. Find $r'(t)$
		1. $r'(t) = \langle t, 5, -2t \rangle$ 
		2. $||r'(t)|| = \sqrt{t^2 + 5^2 + (-2t)^2} = \sqrt{5t^2 + 25}$ 
	3. Find $f(r(t))$
		1. $F(r(t)) = \sqrt{\frac{t^2}{2}}$ 
		2. $f(r(t)) \cdot ||r'(t)|| = \sqrt{\frac{t^2}{2}} \cdot \sqrt{5t^2 + 25} = \frac{t\sqrt{5t^2+25}}{\sqrt{2}}$ 
	4. Integrate
		1. $\int^1_0 \frac{t\sqrt{5t^2+25}}{\sqrt{2}} = \frac{1}{15 \sqrt{2}}(5t^2 + 25)^{3/2} \Big |^1_0 = \frac{1}{15 \sqrt{2}} (30 \sqrt{30} - 125)$ 
	5. ANS: $\frac{1}{15 \sqrt{2}} (30 \sqrt{30} - 125)$
2. An electric field is given by $E(x,y,z) = \langle y + 3, 2x, 2x + z \rangle$. What is the work done by the field on an electron moving along the parametrization
	1. $\int F(r(t)) \cdot r'(t)dt$
	2. $F(r(t)) = \sqrt{\frac{t^2}{2}}$
	3. $F(r(t)) \cdot r'(t)dt =  (t, 0,0) \cdot \langle t, 5, -2t \rangle$ 
	4. $\int^1_0 t^2 = \frac{t^3}{3} \Big |^1_0 = \frac{1}{3} - 0 = \frac{1}{3}$
	5. ANS: $1/3$ 

----
##### Question 5: 
(5) For the following vector fields and surfaces, calculate the flux integral $\iint_S F \cdot dS$
1. $F(x,y,z) = \langle 1 + z, -2, y \rangle$ and $S$ is the part of the plane $x + 3y  + 2z = 6$ which lies in the first octant, oriented away from the origin.
	1. $\iint_S F \cdot dS = \iint_D F(G(u,v)) \cdot N(u,v) dudv$
	2. Find parametrization:
		1. $z = \frac{6 - x - 3y}{2}$ 
		2. $f(x,y) = \langle x, y, \frac{6 - x - 3y}{2} \rangle$ 
	3. Find the partial derivatives of $f(x,y)$
		1. $f_x = (1, 0, -\frac{1}{2})$
		2. $f_y = (0, 1, \frac{-3y}{2})$
	4. Cross multiply $f_x$ and $f_y$
		1. $$N(u,v) = f_x \times f_y = \begin{bmatrix}i & j & k \\ 1 & 0 & -1/2 \\ 0 & 1 & -3/2 \end{bmatrix} = \Big (\frac{1}{2}, \frac{3}{2}, 1 \Big )$$
	5. Calculate $F \cdot N(u,v)$
		1. $$F \cdot N(u,v) = \langle 1 + z, -2, y \rangle \cdot \Big (\frac{1}{2}, \frac{3}{2}, 1 \Big ) = \frac{1 + z}{2} -3 + y $$
	6. Integrate $\iint_S F \cdot dS = \iint_D F(G(u,v)) \cdot N(u,v) dudv$
		1. $0 \le y \le 2$
		2. $0 \le x \le 6-3y$
		3. $\frac{1 + z}{2} -3 + y  = \frac{1 + \frac{6 - x - 3y}{2}}{2} -3 + y = \frac{8-x-3y-12+4y}{4}$ 
		4. $\frac{8-x-3y-12+4y}{4} = \frac{1}{4} (-x+y-4)$ 
		5. $$\frac{1}{4}\int^2_0 \int_0^{6-3y} (-x + y -4)dxdy $$
		6. Calculate the inner integral
			1. $$\int_0^{6-3y} (-x + y -4)dx = -\frac{x^2}{2} + \frac{y^2}{2} - 4x \Big |_0^{6-3y} = $$ 
			2. $$=-3y^2+18y-\frac{\left(-3y+6\right)^2}{2}-24$$
		7. Calculate outer integral
			1. $$\frac{1}{4} \int^2_0 (-3y^2+18y-\frac{\left(-3y+6\right)^2}{2}-24) dy$$
			2. $$=\frac{1}{4} (-y^3 + 9y^2 - \frac{(3y - 6)^3}{18} -24y \Big|^2_0 = -20 + 12 = -8$$
	7. ANS: $-8$ 
2. $F(x,y,z) = \langle z, y, x\rangle$ and $S$ is the part of the parabolic cylinder $z = 1 −x^2$ which lies above the xy-plane and between $y = 0$ and $y = 2$, oriented upwards.
	1. Find the parametrization
		1. $r(u,v) = (u, v, 1-u^2)$
		2. $r_u = (1, 0, -2u)$
		3. $r_v = (0, 1, 0)$
	2. Cross multiply $r_u$ and $r_v$
		1. $r_u \times r_v = - (-2u)i - 0j + - (-1)k = (2u, 0, 1)$ 
	3. Integrate
		1. $$\iint_S F \cdot N(u,v)dS = \int^2_0 \int^1_{-1} (2u-2u^3 + u) dudv$$
		2. Inner integral
			1. $$\int^1_{-1} (2u-2u^3 + u) du = u^2 - \frac{u^4}{2} + \frac{u^2}{2} \Big|^1_{-1} = 1-1 = 0$$
			2. No need to calculate the other integral
		3. ANS: $0$ 
3. $F(x,y,z) = \langle y, x, 2z \rangle$ and $S$ is the unit sphere, oriented upwards
	1. Find the parametrization
		1. $r(u,v) = (\cos u \sin v, \sin u \sin v, \cos v)$
		2. $r_u = (-\sin u \sin v, \cos u \sin v, 0)$
		3. $r_v = (\cos u \cos v, \sin u \cos v, -\sin v)$
	2. Cross multiply
		1. $N = r_u \times r_v = \begin{bmatrix} i & j & k \\ -\sin u \sin v &  \cos u \sin v &  0 \\ \cos u \cos v & \sin u \cos v & -\sin v \end{bmatrix}$ 
		2. $N = (-\cos u \sin ^2 v, -\sin u \sin^2 v, -\sin^2 u \sin v \cos v - \cos^2 \sin v \cos v)$
		3. $N = (-\cos u \sin ^2 v, -\sin u \sin^2 v, -\sin v \cos v)$ 
	3. Bounds
		1. Unit sphere = $0 \le \theta \le  2\pi$ and $0 \le \phi \le  2\pi$ 
	4. Integrate $\iint_S F \cdot dS = \iint_D F(G(u,v)) \cdot N(u,v) dudv$ 
		1. $\int_0^{2\pi} \int_0^{2\pi} (\cos u \sin v, \sin u \sin v, \cos v) \cdot (-\cos u \sin ^2 v, -\sin u \sin^2 v, -\sin v \cos v)dudv$
		2. $\int_0^{2\pi} \int_0^{2\pi} (-\cos^2 u \sin^3 v -\sin^2 u \sin^3 v -\sin v \cos^2 v)dudv$ 

----
##### Question 6: 
(6) Consider a parabolic solar panel which lies in the part of $z = x^2 + y^2$ below the plane $z = 1$ which is oriented downwards. A field of photons is given by $(x^2, y^2, -z)$. Calculate the flux of the photon field through the solar panel.

1. Variables
	1. $F = (x^2, y^2, -z)$
	2. $T(r, \theta) = (r \cos \theta, r \sin \theta, r)$ 
		1. $T_r = ( \cos \theta,  \sin \theta, 1)$
		2. $T_\theta = (-r \sin \theta, r \cos \theta, 0)$
	3. Cross multiply
		1. $N = T_r \times T_\theta = (r \cos \theta, r \sin \theta, -r)$ 
	4. $F(r, \theta) = (r^2 \cos^2 \theta, r^2 \sin^2 \theta, -r)$ 
	5. Dot product to get $F(r, \theta) \cdot N(r, \theta)$
		1. $F(r, \theta) \cdot N(r, \theta) = (r^2 \cos^2 \theta, r^2 \sin^2 \theta, -r) \cdot (r \cos \theta, r \sin \theta, -r)$ 
		2. $F(r, \theta) \cdot N(r, \theta) = r^3\cos^3 \theta, r^3 \sin \theta, r^2$ 
	6. Integrate
		1. $\int_0^{2\pi} \int^1_0 (r^3\cos^3 \theta + r^3 \sin^3 \theta + r^2)r drd\theta$
		2. Inner integral
			1. $\int^1_0 (r^3\cos^3 \theta + r^3 \sin^3 \theta + r^2)r dr = \frac{r^5\cos^3 \theta}{5} + \frac{r^5 \sin^3 \theta}{5} + \frac{r^4}{4} \Big |^1_0$  
			2. $\frac{r^5\cos^3 \theta}{5} + \frac{r^5 \sin \theta}{5} + \frac{r^4}{4} \Big |^1_0 = \frac{\cos^3 \theta}{5} + \frac{\sin^3 \theta}{5} + \frac{1}{4}$ 
		3. Compute outer integral
			1. $\int^{2\pi}_0 \frac{\cos^3 \theta}{5} + \frac{\sin^3 \theta}{5} + \frac{1}{4} d\theta = \frac{1}{4}\theta \Big |_0^{2\pi} = \frac{2\pi}{4} - 0 = \frac{\pi}{2}$
2. ANS: $\frac{\pi}{2}$   

----
##### Question 7: 
(7) Consider the vector field $E(x,y,z) = \langle x, y, z-3 \rangle$; this vector field can be visualized as an explosion outwards from the point $(0,0,3)$. Consider two surfaces in $\mathbb{R}^3$: $D$, the unit disk lying in the xy-plane, and S, the top half of the unit sphere, both oriented downwards
1. Make a prediction for which surface the field will have the greater flux.
2. Calculate the flux of the field through each of the surfaces.
3. Was your prediction correct? Can you explain why or why not?

##### Question 8: 
The concentration of a chemical can be given by the function $C(x,y,z) = \frac{z}{1 + x^2 + y^2}$. By the law of the diffusion, the chemical will begin to flow in the direction where the concentration decreases the fastest. Let S be part of the cylinder $x^2 + y^2 = 1$ where $x \ge 0, y \ge 0, 0 \le z \le 2$, oriented away from the origin. Calculate the flux of the chemical flow through S.
1. Find where the concentration decreases the fastest
	1. $C_x = -\frac{2zx}{(1 + x^2 + y^2)^2}$ 
	2. $C_y = -\frac{2zy}{(1 + x^2 + y^2)^2}$
	3. $C_z = \frac{1}{1 + x^2 + y^2}$ 
	4. Greatest increase = $\langle -\frac{2zx}{(1 + x^2 + y^2)^2}, -\frac{2zy}{(1 + x^2 + y^2)^2}, \frac{1}{1 + x^2 + y^2} \rangle$ 
	5. Least increase = $\langle \frac{2zx}{(1 + x^2 + y^2)^2}, \frac{2zy}{(1 + x^2 + y^2)^2}, -\frac{1}{1 + x^2 + y^2} \rangle$ 
2. Find the flux
	1. Flow rate = $\iint_S v \cdot dS$
	2. $r(u,v) = \langle \cos v, \sin v, u \rangle$
	3. $r_u = \langle 0, 0, 1 \rangle$
	4. $r_v = \langle -\sin v, \cos v, 0 \rangle$
	5. $N = r_u \times r_v = \langle -\cos v, -\sin v, 0 \rangle$ 
3. $\iint_S \nabla C(u, v) \cdot dS = \langle \frac{2(u)(\cos v)}{(1 + (\cos v)^2 + (\sin v)^2)^2}, \frac{2(u)(\sin v)}{(1 + (\cos v)^2 + (\sin v)^2)^2}, -\frac{1}{1 + (\cos v)^2 + (\sin v)^2} \rangle \cdot \langle -\cos v, -\sin v, 0 \rangle$   
	1. Dot product of $C(u,v)$ and $dS$
		1. $\langle \frac{2u\cos v}{(1 + \cos^2 v + \sin^2 v)^2}, \frac{2u\sin v}{(1 + \cos^2 v + \sin^2 v)^2} \rangle \cdot \langle -\cos v, -\sin v \rangle =\frac{2u\cos^2 v}{(1 + \cos^2 v + \sin^2 v)^2} - \frac{2u\sin^2 v}{(1 + \cos^2 v + \sin^2 v)^2}$   
		2. $u\cos^2 v - u\sin^2 v$ 
		3. $\frac{1}{16}\int_0^{2\pi} \int^2_0 u\cos^2 v - u\sin^2 dudv = \frac{1}{16}\int_0^{2\pi} \int^2_0 u^3$  
		4. Inner integral
			1. $\frac{u^4}{4} \Big |^2 _0 = 4 - 0 = 4$
		5. outer integral
			1. $\frac{1}{16}\int^{2\pi}_0 4 = \pi/2$
	2. ANS: $\pi/2$ 

----
##### Question 9: 
(9) Calculate the following line integrals using the fundamental theorem of line integrals; be sure to check that the vector fields are conservative
1. $\int_C F \cdot dr$, where $F(x,y) = \langle 4xye^{x^2}, 2e^{x^2} -3y^2 \rangle$ where $C$ is the path along $(5t - 4t^2 + t^3, 3 + 3t - 2t^2)$ for $0 \le t \le 2$ 
	1. Calculate the [[115 Line and Surface Integrals#Curl|curl]] of $F$
		1. $$Curl(F) = \begin{bmatrix} \frac{\partial}{\partial x} & \frac{\partial}{\partial y}  \\ 4xye^{x^2} & 2e^{x^2} - 3y^2\end{bmatrix} = x4e^{x^2} - x4e^{x^2} = 0$$
		2. $t=0: 5(0) - 4(0)^2 + (0)^3, 3 + 3(0) - 2(0)^2) = (0,3)$ 
		3. $t=3: 5(2) - 4(2)^2 + (2)^3, 3 + 3(2) - 2(2)^2) = (2, 1)$
	2. Find $\nabla F$
		1. $\nabla F = (8xye^{x^2}, -6y) \cdot$ 
	3. Plug into equation
		1. $F(0, 3) = 2(0)e^{(0)^2} - ()^3o = -25
		2. $F(2,1) = 2(1)e^{(2)^2} - (1)^3 =  2e^4 - 5$
		3. $F(2, 1) - F(3, 0) = 2e^4 - 5 - (-25) = 2e^4 + 20$
		4. ANS: $2e^4 + 20$
2. $\int_C (2xy-3z, x^2 + 8y^3 z, 2y^4 - 3x)$ where $C$ is the path $(\cos (\pi t), 3t^2 - 5t, t \sin^2 (\pi t/4)$ from $(1, 0,0)$ to $(1,2,2)$
3. $\oint_C A \cdot dr$, where $A(x,y,z) = \langle \frac{y^2}{z^2 + 1}, \frac{2xy}{z^2 + 1}, \frac{-2xy^2z}{(z^2 + 1)^2} \rangle$ and $C$ is the path along the ellipse $4x^2 + 3xy + y^2 = 10$ oriented counter-clockwise
	1. Since $z^2 + 1$ in each component enables the shape of $A$ to be a circle, we get the answer of $0$
	2. ANS: 0
---
##### Question 10: 
Consider the work integral $\int_C (y - x^2 )dx + (1 - x) dy$ Consider the following two paths that start at $(-1, 1)$ and end at $(3, 9)$ where
- $(-1 + 4t, 1 + 8t)$ over $0 \le t \le 1$
- $(t, t^2)$ over $-1 \le t \le 3$ 

a) Therefore, The path $(-1 + 4t, 1 + 8t)$ has more work done
$work = \int F(r(t)) \cdot r'(t)$ 
1. $r'(t) = (4, 8)$
2. $F(t) = (y-x^2, 1 - x)$
3. $F(r(t)) = ((1 + 8t - (-1 + 4t)^2, 1 - -1 + 4t) =(2 + 12t, 2 + 4t)$ 
4. $F(r(t)) \cdot r'(t) = (8 + 48t, 16 + 32t)$
5. $\int (8 + 48t + 16 + 32t)$
6. $8t + 24t^2 + 16t + 16t^2 \Big |^1_0 =24 + 40 = 64$ 
7. Next problem
8. $r'(t) = (1, 2t)$
9. $F(t) = (y-x^2, 1 - x)$
10. $F(r(t)) = (t^2 - t^2, 1 - t) = (0, 1-t)$
11. $F(r(t)) \cdot r'(t) =  (2t - 2t^2)$
12. $\int^3_{-1} 2t - 2t^2 dt = t^2 - \frac{2t^3}{3} \Big |^3_{-1} =9 - 18 -(1 - 2/3) =8\frac{2}{3}$   
b) Because the path isn't conservative
c) 


---
##### Question 11: 
Consider the vector field $F(x,y,z) = (2y + 4, 2x - z^2, -2yz)$ and the path defined by $r(t) = (t^2, 3 + t, -t)$ for $-1 \le t \le 2$.
1. Calculate the work done by the field along the path
	1. $P = r(-1) = (1, 4, 1)$
	2. $Q = r(2) = (4, 5, -2)$
		1. $f(Q) - f(P) = 2(5) + 4, 2(4) - (-2)^2, -2(5)(-2) - 2(0) + 4, (1) - (1)^2, -2(4)(1)$
		2. $= (14, 4, 20) - (4, 0, -8) = (10, 4, 28)$
		3. $\sqrt{10^2 + 4^2 + 28^2} = 30$ 
	3. ANS: $30$
2. Show that this vector field is conservative. What theorem does this allow us to use?
	1. The cross-partials equation, which allows us to to find the potential function
3. Find the potential function for this field
	1. $\frac{\partial F_1}{\partial y} = \frac{\partial F_2}{\partial x} \quad \quad \frac{\partial F_2}{\partial z} = \frac{\partial F_3}{\partial y} \quad \quad \frac{\partial F_3}{\partial x} = \frac{\partial F_1}{\partial z}$ 
	2. $\frac{\partial F_1}{\partial y} = \frac{\partial F_2}{\partial x}: (2y + 4, 2x - z^2, -2yz)$ 
		1. $2=2$
	3. $\frac{\partial F_2}{\partial z} = \frac{\partial F_3}{\partial y}: (2y + 4, 2x - z^2, -2yz)$
		1. $-2z = -2z$
	4. $\frac{\partial F_3}{\partial x} = \frac{\partial F_1}{\partial z}: (2y + 4, 2x - z^2, -2yz)$ 
		1. $0 = 0$
	5. We have a valid vector field
		1. $\int (2y + 4)dx = 2xy + 4x$
		2. $\int (2x - z^2)dy = 2xy - z^2y$
		3. $\int (-2yz) = -yz^2$ 
	6. Potential function = $2xy + 4x -z^2y$ 
4. Calculate the potential at the starting and end points of the path
	1. $P(P) = 2(1)(4) + 4(1) - (1)^2(4) = 8$
	2. $P(Q) = 2(4)(5) + 4(4) - (-2)(5) = 40 + 16 + 10 = 66$
5. What is the difference in potential between these points?
	1. 66 - 8 = 58
	2. Potential difference of 58
----
##### Question 12: 
Consider a particle starting at the point (0,0,1) moving with an acceleration of $(4e^{-2t}, 3, 3t^2)$ and an initial velocity of $(5, 2, -4)$. The particle is moving through the force field $B(x,y,z) = (2y^2, 4xy, -3z^2)$
1. $v(t) = \int (4e^{-2t}, 3, 3t^2) = (-2e^{-2t}, 3t, t^3)$ 
2. $P = (v(0) - v(0) = (5, 2, -4) - (-2, 0,0) = (7, 2, -4)$
3. $v(t) = (-2e^{-2t}+7, 3t + 2, t^3 - 4)$
4. $s(t) = \int v(t) = \int (-2e^{-2t}+7, 3t + 2, t^3 - 4) = (e^{-2t} + 7t + C, \frac{3t^2}{2} + 2t + C, \frac{t^4}{4} - 4t + C)$
5. $s(0) = (0,0,1)$
6. $s(t) = (e^{-2t} + 7t - 1, \frac{3t^2}{2} + 2t, \frac{t^4}{4} - 4t + 1)$ 
7. Potential function
	1. $fx = \int 2y^2 x dx = 2xy^2 + C$ 
	2. $fy = \int 4xy dy = 2xy^2 + C$
	3. $fz = -\int 3z^2 = -z^3 + C$
	4. Potential function = $f = 2xy^2 -z^3$
8. $f = 2(e^{-2t} + 7t - 1)( \frac{3t^2}{2} + 2t) - (\frac{t^4}{4} - 4t + 1)^3$
9. $f(2) = 2(e^{-2(2)} + 7(2) - 1)( \frac{3(2)^2}{2} + 2(2))^2 - (\frac{(2)^4}{4} - 4(2) + 1)^3 = 200e^{-4} + 2628$
10. ANS: $200e^{-4} + 2628$


----

