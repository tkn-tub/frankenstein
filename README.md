# Frankesntein
This project develops a circuit model for the human cardiovascular system.

## Description
This project develops an electric circuit model in Matlab/Simulink to evaluate the pressure and flow in the human vessels. The model includes the electric circuit of the left ventricle in the heart and the main arteries; see Fig. 1 below. The code plots the pressure along a variety of vessel segments in the main arteries; see Fig. 2


<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankenstein/blob/main/figures/simulink.png?raw=true" alt="electric circuit model of the human cardiovascular system" width="500">
    </p>
</figure>
<p align="center">
Fig. 1: Representation of the electric circuit design in Matlab/Simulink.
</p>

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankenstein/blob/main/figures/pressure_arms.png?raw=true" alt="electric circuit model for the heart" width="500">
    </p>
</figure>
<p align="center">
Fig. 2: Evaluation of the pressure in the arms.
</p>

Each vessel segment is modeled with an L-inverted topology which includes a resistor (resistance to blood), inductor (blood inertia), and capacitor (vessel elasticity); see Fig. 3 below. The parameters are provided in [2]. All the vessel segments are connected as illustrated in the diagram in Fig. 4 and their segments represents the vessels listed in Table 1. A complete explanation is given within the paper in the section ''How to reference this work''.

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankenstein/blob/main/figures/vessel_electric.png?raw=true" alt="electric circuit model for the vessels" width="250">
    </p>
</figure>
<p align="center">
Fig. 3: Model of the vessel segments.
</p>

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankenstein/blob/main/figures/markov.png?raw=true" alt="electric circuit model for the vessels" width="500">
    </p>
</figure>
<p align="center">
Fig. 4: Represenation of the cardiovascular system and their vessel segments.
</p>

| Markov States | Vessel Segment |
| --------------|----------------- |
| S1 | Right Heart |
| S2 | Lungs|
| S3 | Left Heart
| S4 | A. Ascendens
| S5 | Arcus Aorta
| S6 | A. Anonyma
| S7 | Head
| S8 (S17) | A. Subclavia s. (d)
| S9 (S18) | A. Axillaris s. (d.)
| S10 (S19) |  A.Brachialis s. (d.)
| S11 (S20) | A. Radialis s. (d.)
| S12 (S21) | A. Interossea Volaris s. (d.)
| S13 (S22) | A. Ulnaris s. (d.)
| S14 (S23) | V. Brachialis s. (d.)
| S15 (S24) | V. Axillaris s. (d.)
| S16 (S25) |  V. Subclavia s. (d.)
| S26 (S27) |  Jugular Vein s. (d.)
| S28 | Superior Vena Cava
| S29 | Thoratica Aorta
| S30 | Thorax and Back
| S31 | Abdominal Aorta
| S32 | Mesenterica Superior
| S33 | Mesenterica Inferior
| S34 | Liver
| S35 | Kidneys
| S36 | Abdominal Vein
| S37 | Inferior Vena Cava
| S38 (S45) | A. Iliaca Communis and Externa s. (d.)
| S39 (S46) | A. Femoralis Profundis s. (d.)
| S40 (47) | A. Poplitea s. (d.)
| S41 (S48) | A. Tibialis Anterior s. (d.)
| S42 (S49) | A. Tibialis Posterior s. (d.)
| S43 (S50) | V. Poplitea s. (d.)
| S44 (S51) | V. Iliaca Communis and Externa s. (d.)

## Installation
This code is tested in MATLAB 2023b, and the required toolboxes are listed in the table below.

Table 2: Required Matlab Toolboxes
| Matlab Toolbox  | Version |
| ------------- | ------------- |
| Symulink  | 23.2  |
| Symulink Real-Time  | 23.2  |
|Simscape   | 23.2  |
|Simscape Electrical  | 23.2  |
|Stateflow|23.2|
|Econometrics Toolbox|23.2|

## Usage

This project directly runs from the file `A_Master_File.mlx`. This file calls to the other three project files: `Parameters.mlx`, `Noordergraaf_Rideout.slx` and `B_Plot_Results.mlx`. Each file performs the following actions

- `A_Master_File.mlx`: This is the master file to run the project. This code is organized in three sections: 1) loads the circuit parameters for the resistors, inductors, and capacitors by calling to `Parameters.mlx`, 2) In a second section it runs the Simulink file `Noordergraaf_Rideout.slx` , and 3) in the last section it plot the results calling to the folder `B_Plot_Results.mlx`

- Parameters.mlx: This code includes the values for the heart following the design in [1, Fig. 4.2.1 pag. 79]. Furthermore, it loads the values for the resistor, inductor, and capacitor of the main arteries in the file `Parameters.xlsx`.

- `Noordergraaf_Rideout.slx`: This file includes the Simulink design for the heart and the arteries; see Fig. 1 above.

- `B_Plot_Results.mlx`: This file includes the plot for the pressure, flow, and also the calculation of stationary probabilities.


## Features
- **Realistic modeling for the left ventricle in the heart:** This design in Simulink includes an electric circuit model of the left ventricle in the heart, where the frequency can be varied programatelly in `Parameters.mlx`. The model follows the desing in [1, Fig. 4.2.1 pag. 79] and provides the ventricular preassure as a voltage signal.
- **Realistic modeling for the main arteries in the cardiovascular system:** The project model the each different vessel segment with the resistance to blood (resistor value), the inertia of the blood (inductor value), and the elasticity of the vessels (capacitor value); as follows from [2]

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankenstein/blob/main/figures/heart.png?raw=true" alt="electric circuit model for the heart" width="500">
    </p>
</figure>
<p align="center">
Fig. 5: Representation of signals and schematic of the left ventricle in the heart.
</p>

## Contributing
Interested contributors can contact the project owner. Please refer to the Contact Information below. We identify further developments for more complex scenarios like estimating the distance to multiple cancer cells.

## License
![Licence](https://img.shields.io/github/license/larymak/Python-project-Scripts)

## Acknowledgements
We want to thank Dr.Bettina Krueger for the very helpful discussion about the physiological parameters of the HCS to validate our electrical circuit model.The reported research was supported by the project NaBoCom, funded by the German Research Foundation (DFG)under grant DR639/21-2 as well as by the project IoBNT, funded by the Federal Ministry of Education and Research (BMBF, Germany)under grant 16KIS1986K.

## References
[1] Vincent C. Rideout. 1991. Mathematical and Computer Modeling of Physiological Systems. Prentice Hall, Upper Saddle River, NJ

[2] Abraham Noordergraaf, Pieter D. Verdouw, and Herman B.K. Boom. 1963. The use of an analog computer in a circulation model. Progress in Cardiovascular Diseases 5, 5 (March 1963), 419–439. [Link](https://doi.org/10.1016/s0033-0620(63)80009-2)

## Contact Information

- **Name:** Jorge Torres Gómez

    [![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github)](https://github.com/jorge-torresgomez)

    [![Email](https://img.shields.io/badge/Email-jorge.torresgomez@ieee.org-D14836?logo=gmail&logoColor=white)](mailto:jorge.torresgomez@ieee.org)

    [![LinkedIn](https://img.shields.io/badge/LinkedIn-torresgomez-blue?logo=linkedin&style=flat-square)](https://www.linkedin.com/in/torresgomez/)

    [![Website Badge](https://img.shields.io/badge/Website-Homepage-blue?logo=web)](https://www.tkn.tu-berlin.de/team/torres-gomez/)

## How to reference this work

Please refer to this work through the reference 

Jorge Torres Gómez, Jorge Luis González Rios and Falko Dressler, "Electric Circuit Representation of the Human Circulatory System to Estimate the Position of Nanosensors in Vessels," Elsevier Nano Communication Networks, vol. 40, pp. 100499, July 2024. 