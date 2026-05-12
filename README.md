# binary-stiffness-wrench

## Background

When using a conventional adjustable wrench, adjusting the jaw size requires manually
scrolling the adjustment screw every time the fastener size changes, which is tedious
and slows down the work process. The binary stiffness mechanism addresses this by
allowing the jaw to switch between two states: in the low stiffness state, the jaw is
compliant and can freely adjust to fit around any fastener without manual sizing, and
once in position, toggling the mechanism into the high stiffness state locks the jaw
rigid so it can function as a normal wrench to apply torque.

## Fusion 360 Workflow

To design the binary stiffness wrench, Fusion 360 was used across its Design and
Simulation workspaces. In the Design workspace, User Parameters (Modify > Change
Parameters) were set up to drive all critical dimensions — beam thickness, V-angle,
hinge width, and bistable gap — so that any geometry update propagated automatically.
The wrench profile and both flexure mechanisms were drawn using Create Sketch, with
constraints and parameter-linked dimensions ensuring full definition.
In the Simulation workspace, Static Stress
studies were configured to validate the two-state behavior: a Fixed Constraint on the
jaw face served as the boundary condition,and a Force Load drove the bending study . 
The simulation used to directly observe
how the V-shaped negative stiffness beams deform and bend under load — the Displacement
result contour map visualized the snap-through bending behavior of the V-geometry and
confirmed the deformation pattern before committing to the final geometry. 

Once the design was validated through simulation,
the final wrench was fabricated using a digital fabrication method 
which was well suited to producing the monolithic compliant structure as
a single piece without any assembly required.

## Reference

Kuppens, P. R., Bessa, M. A., Herder, J. L., & Hopkins, J. B. (2021). Monolithic
binary stiffness building blocks for mechanical digital machines. *Extreme Mechanics
Letters*, 42, 101120. https://doi.org/10.1016/j.eml.2020.101120
