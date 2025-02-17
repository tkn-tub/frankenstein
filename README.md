# Frankesntein
This project develops a circuit model for the human cardiovascular system.

## Description
This project develops an electric circuit model in Matlab/Simulink to evaluate the preassure and flow in the human vessels. The model includes the electric circuit of the left ventricle in the heart and the electric circuit of the main arteries; see Fig. 1 below.

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/NN_molecular_communications/blob/main/Figures/simulink.png?raw=true" alt="nn" width="500">
    </p>
</figure>
<p align="center">
Fig. 1: Representation of the electric circuit design in Simulink (Matlab).
</p>

## Installation
This code is tested in MATLAB 2023b, and the required toolboxes are listed in the table below.

| Matlab Toolbox  | Version |
| ------------- | ------------- |
| System Identification Toolbox  | 23.2  |
| Deep Learning Toolbox  | 23.2  |
|Statistics and Machine Learning Toolbox|23.2|

## Usage

This project directly runs from the file `A_Master_File.mlx`. This file calls to the other three project files: `Parameters.mlx`, `Noordergraaf_Rideout.slx` and `B_Plot_Results.mlx`.

## Features
- **Realistic modeling for the left ventricle in the heart:** This design in Simulink includes an electric circuit model of the left ventricle in the heart, where the frequency can be varied programatelly in `Parameters.mlx`. The model follows the desing in [1, Fig. 4.2.1 pag. 79] and provides the ventricular preassure as a voltage signal.
- **Realistic modeling for the main arteries in the cardiovascular system:** This solution features a 2 nodes NN to accurately estimate the distance to a cancer cell from a neighbord immune cell.

<figure>
    <p align="center">
        <img src="https://github.com/tkn-tub/frankesntein/blob/main/Figures/heart.png?raw=true" alt="nn" width="500">
    </p>
</figure>
<p align="center">
Fig. 2: Representation of signals and schematic of the left ventricle in the heart.
</p>

## Contributing
Interested contributors can contact the project owner. Please refer to the Contact Information below. We identify further developments for more complex scenarios like estimating the distance to multiple cancer cells.

## License
![Licence](https://img.shields.io/github/license/larymak/Python-project-Scripts)

## Acknowledgements
We want to acknoledge the support provided by Mohammad Zoofaghari, author of the paper in [1] for giving us the code to generate the dataset.

## References
<a name="fn1">[1]</a>: M. Zoofaghari, F. Pappalardo, M. Damrath, and I. Balasingham, “Modeling Extracellular Vesicles-Mediated Interactions of Cells in the Tumor Microenvironment,” IEEE Transactions on NanoBioscience,
vol. 23, no. 1, pp. 71–80, Jan. 2024. [Link](https://ieeexplore.ieee.org/document/10149035)

## Contact Information

- **Name:** Jorge Torres Gómez

    [![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github)](https://github.com/jorge-torresgomez)

    [![Email](https://img.shields.io/badge/Email-jorge.torresgomez@ieee.org-D14836?logo=gmail&logoColor=white)](mailto:jorge.torresgomez@ieee.org)

    [![LinkedIn](https://img.shields.io/badge/LinkedIn-torresgomez-blue?logo=linkedin&style=flat-square)](https://www.linkedin.com/in/torresgomez/)

    [![Website Badge](https://img.shields.io/badge/Website-Homepage-blue?logo=web)](https://www.tkn.tu-berlin.de/team/torres-gomez/)