# Robust_Superconductivity

Input files and data provided for "Unraveling the Robust Superconductivity Phenomenon of High-Entropy Alloy" soon to be posted to arXiv. 

In each system directory ("Nb", "NbTi_crystal", "NbTi_SQS", "HEA") has a folder for calculation inputs ("input_files") at 6 pressures (0,30,60,90,120,150 GPa). 

Also in each system directory is a single <code>data.h5</code> file, which contains the electronic band structure and density of states, phonon dispersion and phonon density of states, and the Eliashberg spectral function for each pressure studied. An example showing how to interact with this file using h5py is provide in "interface_example.ipynb". 

File structure of <code>data.h5</code>
```
├── electronic
│   ├── 0_GPa (attributes: description, bandstructure_cols, electronic_dos_cols, fermi_energy_eV, kpath)
│   │   ├── band_structure
│   │   └── electronic_dos
│   └── 30_GPa (attributes: description, bandstructure_cols, electronic_dos_cols, fermi_energy_eV, kpath)
│   │   ├── ... 
│   │   └── ...
│   ...
├── phonons
│   ├── 0_GPa (attributes: description, phonon_dispersion_cols, phonon_dos_cols, kpath)
│   │   ├── phonon_dispersion
│   │   └── phonon_dos
│   └── 30_GPa (attributes: description, phonon_dispersion_cols, phonon_dos_cols, kpath)
│   │   ├── ... 
│   │   └── ... 
│   ...
└── elph
    ├── 0_GPa (attributes: description, a2F_cols)
    │   └── a2F
    └── 30_GPa (attributes: description, a2F_cols)
    │    ├── ...
    ...

```
