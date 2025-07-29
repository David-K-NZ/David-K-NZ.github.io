---
layout: post
title: Rope Sheave Analysis
description:  Analysis of a custom aluminium rope sheave for use in a maritime environment to complete lifting procedures. Design signed of by CPEng.
skills: 
- Critical Path Analysis
- Hand Calculations
- Application of standards
- Finite Element Analysis
- Design Review & Redesign
main-image: /Screenshot 2025-07-27 211440.png

---

## Project Story

---

A client requested a validation for a design of an aluminum rope sheave block to be used in maritime lifting applications. The primary use of the sheave block was to assist in lifting mussel barrels to check them for disease or any other issues. Traditionally these have been checked by having divers swim through the farm, but as these farms are expanding this is becoming less cost effective. As a result, the sheave block was intended to transfer the lifting rope through a 90 degree arc only, with a slightly non-conventional design as a result. As the design was slightly unconventional, Finite Element Analysis (FEA) was chosen as the primary method of validation for the design.

Analysis of the sheave block began with consideration of the AS2089 - Rope Sheaves standard, where the discrepancy in the actual design and the standard designs was noted. The non-conventionality of the design was the use of a connection to structure that didn't allow the sheave block to realign all load into pure tension, and instead meant that applied load would be seen as combined tension and bending in the welded connections in the sheave body. A Free-Body Diagram (shown below), indicated the net load direction as a result of the rope loading. FEA supports indicated with green arrows, and shear flow indicated with blue arrows.

![Free Body Diagram](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%151752.png)

Based on the resultant loads, I completed a quick series of hand calculations to ensure the freewheel/axle of the sheave would be OK under the applied load before continuing to the FEA portion of the project. At a 2x overload (proof load based on AS2089) the sheave components passed the checks, but only by a slim margin. This gave confidence to move on to the FEA portion of analysing the main parts of the block with FEA, as well as awareness that the block may only just pass the applied load conditions. Screenshot from Solidworks of the mesh used below, with local refinements used to maximise information in high-stress areas.

![FEA Mesh](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%153227.png)

Mesh report indicated several cells with high aspect ratios from this refined mesh. Report shown below:

![FEA Mesh Report](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%153448.png)

Aspect ratios checked based on the above report to ensure that all elements in key areas had aspect ratios that would resolve without significant errors. Red elements in the below plots had aspect ratio >= 3.0, and dark blue indicates an aspect ratio of 1.0.

![FEA Aspect Ratios](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%153722.png)

Aspect ratios in key elements were all within range that gave at least reasonable-quality outputs. Reactions were also checked and found to be in the right range to have minimal large-scale errors with the analysis. This gave confidence in the results that followed.

Deflection plot from applied load shown below. Deflection was minimal, magnified by a factor of 150 for clarity in shape. 

![FEA Deflection](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%164313.png)

Stresses in sheave block under the applied load:

![FEA Stress 1](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-27%211440.png)

As can be seen, a decent area around the sheave axle connection was beyond the allowable stress (red), and a significant area at the welded connection also appeared to be beyond the allowable stress. Stress in the full cross-section was considered, as due to the bending nature of the loading this may have been surface stress only.

![FEA Stress 2](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%164809.png)

Stresses throughout thickness of plate in this area. Additional plates added to reduce stress below the allowable limit:

![FEA STress 3](/_projects/Rope-Sheave-Analysis/Screenshot%2025-07-28%20164936.png)

Additional plate reduced most stress below the allowable limit. Some surface stresses were still high, but this was not considered to be an issue due to the 2x proof load that was applied for this analysis. Fatigue was considered, and these areas were noted to the client as being likely points for crack formation in the sheave block. The sheave block was certified in this final configuration and an 'Approved as Correcte' drawing was issued to the client along with a Design Statement signed by a Chartered Engineer.
