# RL_STM_manipulation

RL based automated workflow for STM manipulation. Here we carry out STM manipulation using a machine learning based workflow which utilizes an RL agent for parameter optimization. The workflow combines YOLO based object detection models for detection of carbon monoxide (CO) molecules and reinforcement learning (RL) algorithms to automate the manipulation process.

## Overview

This project implements an automated STM (Scanning Tunneling Microscopy) manipulation system using reinforcement learning. The main executable notebook is [`Multiple_Manipulations.ipynb`](Multiple_Manipulations.ipynb), which orchestrates the entire workflow by utilizing various classes, environments, and functions defined in the Python source files.



## Key Components

### Python Files Description


- **`Manipulation_env.py`** - Implements the main RL environment class `Manipulation_multi_object` that defines the state space, action space, and reward functions for the manipulation task.

- **`detect_molecules.py`** - Provides YOLO-based object detection functionality for identifying and localizing CO molecules in STM images using trained neural network models.

- **`stm_manipulation_experiments.py`** - Contains core experimental routines for performing STM manipulations and scanning operations via TCP communication with the Nanonis system.

- **`get_reward.py`** - Implements various reward functions to evaluate manipulation success, including displacement-based and state-based reward calculations.

- **`drift_estimation.py`** - Handles drift correction algorithms to compensate for thermal and mechanical drift during long manipulation sequences.

- **`nanonis_TCP.py`** - Provides TCP communication interface for controlling the Nanonis SPM system programmatically.

- **`stm_utils.py`** - Utility functions for STM image processing, file handling, and coordinate transformations.

- **`expt_utils.py`** - General experimental utility functions for data processing, file management, and coordinate calculations.

- **`experimental_routines.py`** - High-level experimental procedures and workflow management functions.

- **`Manipulation_coords.py`** - Coordinate system management and manipulation trajectory planning functions.

- **`get_target.py`** - Target selection algorithms for choosing manipulation goals and computing target coordinates.

- **`display_results.py`** - Visualization functions for displaying manipulation results and experimental progress.

- **`buffer_functions.py`** - Buffer management utilities for handling data streams and experimental sequences.

- **`env_functions.py`** - Environment-specific helper functions supporting the RL framework implementation.

## Credits

The RL methodology is implemented using the [d3rlpy](https://github.com/takuseno/d3rlpy) codebase, a comprehensive offline reinforcement learning library for Python.


The nanonisTCP repository is based on ['Julian Ceddia'/'nanonisTCP'] (https://github.com/New-Horizons-SPM/nanonisTCP/tree/v1.0.2), doi:10.5281/zenodo.7402664
