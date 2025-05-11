# Parameterestimation
respiratory for Parameter estimation of motor with encoder using Matlab simulink







In this project we were asked to apply the fundamental concepts of system
modeling to build the mathematical model of the physical system we will work on
and estimate its parameters.
First of all, our mechatronic system we will model is a DC motor which will
attached via a timing belt drive to a cart moving on a linear guide rail. In our
report we will represent a schematic representation of the system, the
mathematical model, the block diagram model of the system, the system’s
parameter estimation steps, the simulation model on Simulink, a comparison
between the physical model acquired data and the simulation model results, and
some comments about the accuracy of the identified system model.


Mathematical model of the system
• Electrical Model:
o by applying KVL:
▪ Vin = IR + L(𝑑𝐼
𝑑𝑡
)+ eb (Note: eb = Kb ∗ 𝜔)
o by taking S domain:
▪ Vin(s) = IR(𝑠) + LSI(𝑠) + (Kb ∗ 𝜔(𝑠))
▪ I(s) = [ Vin(s) − (Kb ∗ 𝜔(𝑠)] / [R+LS]
• Mechanical Model:
o J𝜃̈= J𝜔̇= ∑ T
o J𝜔̇= Tm − bm ∗ 𝜔
o by taking S domain:
▪ JS𝜔(𝑠) = Tm(s) − bm ∗ 𝜔(s)
▪ So, Tm(s) = (JS + bm) * 𝜔(s)
▪ ∴ 𝜔(𝑠) = Tm(s)/ [JS+bm] (Note Tm = I ∗ 𝐾t)
▪ ∴ 𝜔(𝑠) = [I*Kt] /[JS+bm]
▪ ∵ I(s) = [ Vin(s) − (Kb ∗ 𝜔(𝑠)] / [R+LS]
▪∴ 𝜔 (𝑠) = ([ Vin(s) − (Kb ∗ 𝜔(𝑠)] * Kt)/ ([JS+bm] * [R+LS] )



