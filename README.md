<p align="left">
  <img src="logo.png" alt="Logo Gauche" width="500"/>
</p>
<p align="right">
  <img src="logo_inria.png" alt="Logo Droit" width="500"/>
</p>



# Numerical Modeling of Bifluid Flows on Quadtrees

## Context

## Equations of the Model
In a two-fluid model, each fluid, caracterised by its own density ρ and velocity μ, satisfies the Navier-Stokes system equation:
<p align="center">
  <img src="eq1.png" alt="eqautions 1" width="500"/>
</p>

In one single problem, a unique momentum equation can be writen on new variables ρ and μ: 

<p align="center">
  <img src="eq2.png" alt="eqaution 2" width="500"/>
</p>

where (ρ,μ) become a function that is equal to (ρ₁,μ₁) in the first fluide and to (ρ₂,μ₂) in the second. In order to model the interface Γ
between fluids, the boundary is considered as the zero level of a function φ called LevelSet where:
<p align="center">
  <img src="eq3.png" alt="eqaution 3" width="500"/>
</p>



## Algorithm of the prediction-correction method