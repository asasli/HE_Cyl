# Hydrostatic Equilibrium for rotating cylindrical poolytropes


## Lane-Emden Equation

The Lane-Emden equation is $$θ''+\frac{θ'}{ξ}=-θ^n+β$$

where β is a constant being correlate with the rotation of a NS,

n is the polytropic index from the polytropic EOS ($P=Kρ^Γ$ with $Γ=1+\frac{1}{n}$),

and θ from the density's function $ρ(θ)={ρ_c}θ^n$




### *Numerical Solution for Lane-Emden Equation*

#### Runge-Kutta Method:

- The DE is $$θ''+\frac{θ'}{ξ}=-θ^n+β$$


- Assuming $θ'=\frac{dθ}{dξ}=z$, $θ''=\frac{d^2θ}{dξ^2}=z'$ and also replacing ξ with x, θ with y and β with b


- The DEs are $$z'=-\frac{z}{x}-y^n+b=f(y,z)$$ $$and$$ $$y'=z$$


- Initial Conditions: The density at the center of the star is known to be equal to $ρ_n$, so θ(0)=y(0)=1 and z(0)=0. Therefore, $z'(0)=-\frac{z(=0)}{x(=0)}-1+b$ $\implies(De L' Hospital)\implies f(0)=z'(0)=\frac{-1+b}{2} $


- $\underline{Numerical}$ $\underline{Solution}$: $${y_{i+1}}={y_i}+\frac{k_1 +2k_2 +2k_3+ k_4}{6}$$ 
$${z_{i+1}}={z_i}+\frac{l_1 +2l_2 +2l_3+ l_4}{6}$$


where 

$k_1=hy'_i,$

$k_2=hy'(z_i+\frac{l_1}{2}),$

$k_3=hy'(z_i+\frac{l_2}{2}),$

$k_4=hy'(z_i+l_3).$

$l_1=hf_i,$

$l_2=hf(x_i+\frac{h}{2},y_i+\frac{k_1}{2},z_i+\frac{l_1}{2}),$

$l_3=hf(x_i+\frac{h}{2},y_i+\frac{k_2}{2},z_i+\frac{l_2}{2}),$

$l_4=hf(x_i+h,y_i+k_3,z_i+l_3).$


## Rotation - β constant

The dimensionless variable b is $$β=\frac{Ω^2}{2πGρ_c}$$

Every star have a maximum Rotation (Ω) depending from the polytropic index n. If b exceed the maximum limit $β_c$, the star will be destroyed (mass shedding). In this case, the equilibrium not apply and therefore it is $\frac{dP}{dr}=0$ at the surface of the star. So, at this boundary condition the Lane-Emden Equation (for $ξ=ξ_1$) takes the form: $$θ''(ξ1)=β$$.



