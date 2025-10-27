

### Aeroelasticity Crash Course from [[Vogt_AeroelasticityTurbomachines]]:
[[Flutter]] is a **self-excited phenomena**
![[Pasted image 20251020201146.png]]
Associated with **negative overall damping**:
- vibration starts by itself if the fluid-structure coupled system goes unstable
- rapidly diverges.
- In reality, it usually hits a "limit cycle oscillation" or LCO
- ![[Pasted image 20251020201526.png]]
- Can be tolerated

Interaction between **structures** and **aerodynamics**:
![[Pasted image 20251020201600.png]]
But what about F(t)?
- Due to **flow** and **motion** of the blade
- Arbitrary direction, but only the component **in direction of the mode** that matters
- Most probably **not perfectly in phase with the motion**
![[Pasted image 20251020201719.png]]
==The part of the **aerodynamic force that's out-of-phase** with the motion (thus leading to a "positive damping") is referred to as [[Aerodamping]]==

**Aerodynamic Influence**: you don't usually just have one blade, you have a dozens.. A single oscillating blade will influence all the other blades via the unsteady flow field, here's an example with one blade moving:
![[Pasted image 20251020202358.png]]

**Traveling wave mode stability** and the [[Influence Coefficient Approach]]: linear superposition of unsteady pressure:
![[Pasted image 20251020202549.png]]
![[Pasted image 20251020202601.png]]
