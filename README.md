# Breaking Neural Networks

Implementation of Carlini & Wagner's algorithm (https://arxiv.org/abs/1608.04644).

**Distance Metric**   
$L_2$ distance between $x$ and $x'$ is computed $||x - x'||_2$.

**Objective Function**   
Find $\delta$ that solves: min $||\delta||_2 + c * f(x + \delta)$, such that $x+\delta \subset [0,1]^n$.

**Box Constraints**
$\delta_i = 1/2 (tanh(w_i)+1) - x_i$

$-1 <= \tanh(w_i) <= 1$, so $0 <= x_i + \delta_i <= 1$.

![equation](http://latex.codecogs.com/gif.latex?Concentration%3D%5Cfrac%7BTotalTemplate%7D%7BTotalVolume%7D)  
