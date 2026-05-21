# SCALABLE NEURAL QUANTUM STATES ARCHITECTURE FOR QUANTUM CHEMISTRY

Tianchen Zhao, James Stokes, Shravan Veerapaneni

This repository includes the codes for the paper "Scalable neural quantum states architecture for quantum chemistry" (https://arxiv.org/pdf/2208.05637.pdf).

## How to Use

To use this code, follow these steps:

1. Download this repository.

    ```
    git clone https://github.com/Ericolony/made-qchem.git
    ```

2. Navigate to the working directory.

    ```
    cd made-qchem
    ```

### 1. Environment Setup

To set up the environment, follow these instructions:

- Make sure your operating system meets the requirements for PyTorch 1.12.0 and CUDA 11.6.

- Install the required packages using pip and conda:

    ```
    pip install numpy
    conda install pytorch==1.12.0 torchvision==0.13.0 torchaudio==0.12.0 cudatoolkit=11.6 -c pytorch -c conda-forge
    pip install torch torchvision torchaudio
    pip install tensorboardX
    pip install backpack-for-pytorch
    pip install pytorch-model-summary
    pip install openfermionpsi4
    pip install yacs
    ```

- Download and install Psi4:

    ```
    curl "http://vergil.chemistry.gatech.edu/psicode-download/Psi4conda-1.7-py38-Linux-x86_64.sh" -o Psi4conda-1.7-py38-Linux-x86_64.sh --keepalive-time 2
    bash Psi4conda-1.7-py38-Linux-x86_64.sh -b -p $HOME/psi4conda
    echo $'. $HOME/psi4conda/etc/profile.d/conda.sh\nconda activate' >> ~/.bashrc
    echo "source $HOME/psi4conda/etc/profile.d/conda.csh\nconda activate" >> ~/.tcshrc
    ```

- Verify that Psi4 is working correctly:

    ```
    psi4 --test
    ```

### 2. Demo

To run the demo, execute the following script:

```
./run.sh
```

The script will evaluate the H2 molecule on various basis sets and save the results in the `./logger` directory. The results include the energy and convergence information for each basis set, as well as the time taken for each calculation. Please note that the demo may take some time to run, depending on your hardware, the size of the basis sets, number of training iterations (learning rate), batch size (for larger molecules).

## Citation

If you use this code, please cite:

```bibtex
@article{zhao2023scalable,
  title={Scalable Neural Quantum States Architecture for Quantum Chemistry},
  author={Zhao, Tianchen and Stokes, James and Veerapaneni, Shravan},
  journal={Machine Learning: Science and Technology},
  volume={4},
  number={2},
  pages={025034},
  year={2023}
}
```

Paper: https://arxiv.org/abs/2208.05637  
Project page: https://ericolony.github.io/Publications/scalable-neural-quantum-states-architecture-for-quantum-chemistry/
