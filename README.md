<p align="left">
  <img src="logo.png" alt="Logo Gauche" width="500"/>
</p>
<p align="right">
  <img src="logo_inria.png" alt="Logo Droit" width="500"/>
</p>



# Numerical Modeling of Bifluid Flows on Quadtrees

## Context

## Equations of the Model
In a two-fluid model, each fluid, caracterised by its own density ρ and viscosity μ, satisfies the Navier-Stokes system equation:
<p align="center">
  <img src="eq1.png" alt="eqautions 1" width="500"/>
</p>

A unique momentum equation can be writen on new variables ρ and μ in order to model one single problem: 

<p align="center">
  <img src="eq2.png" alt="eqaution 2" width="500"/>
</p>

where (ρ,μ) become a function that is equal to (ρ₁,μ₁) in the first fluide and to (ρ₂,μ₂) in the second. To model the interface Γ
between fluids, the boundary is considered as the zero level of a function φ called LevelSet where:
<p align="center">
  <img src="eq3.png" alt="eqaution 3" width="500"/>
</p>

The LevelSet is updated at each iteration of the calculation through the resolution of the following Transport equation:
<p align="center">
  <img src="eq4.png" alt="eqaution 4" width="500"/>
</p>

Initially, LevelSet is choosen as the signed distance function to the interface
<p align="center">
  <img src="eq5.png" alt="eqaution 5" width="500"/>
</p>

The reconstruction of values ρ and μ from the LevelSet is done after updating, as follows:

<p align="center">
  <img src="eq6.png" alt="eqaution 6" width="500"/>
</p>

## Algorithm of the prediction-correction method
A way to solve the Navier-Stokes equation:
<p align="center">
  <img src="eq7.png" alt="eqaution 7" width="500"/>
</p>
and find the value of velocity at the next time tⁿ⁺¹ is to use the prediction-correction method which consists of the following parts:

### Predction Step:
The method starts with solving the prediction equation and fiding the value of the intermediate velocity u* defined as follows:  
<p align="center">
  <img src="eq8.png" alt="eqaution 8" width="500"/>
</p>

### Poisson equation:
By knowing the value of the u*, the value of ψ is found thanks to Poisson equation which can be writting in the following form:
<p align="center">
  <img src="eq9.png" alt="eqaution 9" width="500"/>
</p>
