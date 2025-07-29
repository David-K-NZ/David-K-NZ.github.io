---
layout: post
title: Seismic Design of Fuel Storage Tank
description:  Validation and certification of horizontal cylindrical fuel storage tank for seismic loading. Involved regulatory compliance, hand calculations, Finite Element Analysis, anchor consideration & validation, and communication with the client.
skills: 
- Understanding of regulations to use various Standards
- Hand Calculations
- Communication with clients
- Time management
- Presentation to Senior Engineers
- Finite Element Analysis
main-image: /Screenshot 2025-07-27 211225.png 
---

## Project Story

---

This was a semi-standard project for Motovated; all large fuel storage tanks in New Zealand need to be validated for earthquake loads and signed off by a Chartered Engineer. In this case, I did the calculations/validation of the design and the Chartered Engineer reviewed and signed off on the outputs of this work. The tank in question was a double-skinned horizontal cylindrical tank with flat ends, which would be used to store insulation oil for a power generation system.

The first part of this project was a review of the critical components of this tank that would need to be validated in order to certify the design as being fit for purpose. The critical path that was decided upon was documented and is screenshot below:

![Critical Path](/_projects/Seismic-Validation/Screenshot%202025-07-29%20105732.png)

This was used in the early stage checkin for the project to ensure that the project remained on track to complete within time/budget.

The impulsive assumption refers to the Seismic Design of Storage Tanks model for fluid motion in a storage container under earthquake loads and how this motion is dependent on the freeboard in the vessel. In this case, there was not enough freeboard to support convective motion and the fully impulsive assumption was applicable.

From here the hoop stress under combined dead load, fuel dead load, and ULS earthquake load was analysed (load combination as per NZS1170.0). This was a fairly simple check, and assumed the full load was acting on only half the wall of the tank. This is a simplification on the actual mode of failure, but I'm not aware of any horizontal cylindrical tanks that have failed through this mode under seismic loading- nor was the Chartered Engineer who signed this off. As a result, this was considered to be reasonable grounds and we considered the flat ends of the tank. Below is an image of the model of the tank used for FEA, outer skin hidden.

![FEA endcap model](/_projects/Seismic-Validation/Screenshot%202025-07-29%20110736.png)

The end of the tank was modelled, meshed, and evaluated in Solidworks. We had a CAD file from the client, but for the purpose of FEA it was decided that it would be faster to build a new model of the areas of interest only. Mesh of the endcap below:

![FEA endcap mesh](/_projects/Seismic-Validation/Screenshot%202025-07-29%20110931.png)

Mesh used primarily shell elements for the tank body/endcap itself, and solid elements for the stiffeners only. Shell elements were deemed to be more accurate for the tank body/endcap, but as the stiffeners were Equal Angle sections they were easier to model as solid without significant loss in accuracy.

Stresses within the endcap under combined load shown below. Hydrostatic load applied as linear varying equation with maximum at base of tank, and earthquake dynamic load applied as a force equally distributed across the entirety of the inner face. All stresses normalised to allowable bending stress of AS3990 - Mechanical Steelwork, which in this case is 180 MPa.

![FEA endcap stress 1](/_projects/Seismic-Validation/Screenshot%202025-07-29%20111642.png)

Stress error plot:

![Stress error plot](/_projects/Seismic-Validation/Screenshot%202025-07-29%20111752.png)

So stresses on the internal skin/stiffeners were all OK, but very high around the ends of the stiffeners. As error was also high in these places, it was assumed that what would liokely be happening was that the stiffeners were 'punching through' the internal shell of the tank. CLoseups on the ends of the stiffeners below:

![FEA Stiffener ends](/_projects/Seismic-Validation/Screenshot%202025-07-29%20112034.png)

So stiffeners extended to the shell of the tank to reduce risk of punching through. Stresses under extended stiffener condition:

![FEA ext. stress](/_projects/Seismic-Validation/Screenshot%202025-07-29%20112258.png)

Stresses much better than previously. Some very high stresses at ends of stiffeners, but this was expected to be an artifact of the shell/solid elements interacting and the relatively high aspect ratio of some elements in the stiffeners. Magnified deflection plot below shows tank end deflecting as expected under the applied load:

![FEA ext. deflection](/_projects/Seismic-Validation/Screenshot%202025-07-29%20112359.png)

This was considered to be the point at which reasonable grounds were achieved for the endcaps of the tank. After this, validation was completed for the saddles that the tank rested on. FEA was conducted in a similar manner to the above, using shells for all aspects of the saddle model, and the saddles were found to be OK under the applied loads. Stress plots of a saddle under a typical longitudinal load below:

![FEA saddle stress](/_projects/Seismic-Validation/Screenshot%202025-07-29%20125636.png)

From here, anchor loading was considered. Anchors were validated using the Hilti PROFIS Engineering software based on a worst-case overturning load. Screenshot from that analysis below, showing the anchoring at one end of a saddle where a transverse overturning load was being considered.

![HILTI Anchor check](/_projects/Seismic-Validation/Screenshot%202025-07-29%20125805.png)