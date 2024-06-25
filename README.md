# 2024-07-04-insar-python-tudelft
Software Workshop of Processing Radar Interferometry Data with Novel Python Libraries

## Setup for the workshop

The setup of this workshop is tested on Unix-like system (Linux, macOS, or WSL on Windows). If you use Windows, we recommend you use Anaconda to continue the setup.

### Step 1: Download the datasets used in the workshop

    Download the following files and move them to your working directory:

    1. Example Sentinel-1 corregistered interferogram stack: [link](https://figshare.com/ndownloader/files/41012180)
    2. Example CSV of a set of processed scatterers: [link](https://figshare.com/ndownloader/files/47231389)
    3. BAG dataset of Amsterdam region: [link](https://figshare.com/ndownloader/files/41012444)

### Step 2: Setup the Python environment
    
    Install dependencies using `conda` or `mamba`. Here is an example with `mamba`:

    ```bash
    mamba env create -f https://raw.githubusercontent.com/esciencecenter-digital-skills/2024-07-04-insar-python-tudelft/main/environment.yaml
    ```

    The above command create a new environment named `insar-python` from the [environment.yaml](https://github.com/esciencecenter-digital-skills/2024-07-04-insar-python-tudelft/blob/main/environment.yaml) file. You can also download this file and create the environment manually.

### Step 3: Verify the installation

    Activate the environment:

    ```bash
    conda activate insar-python
    ```

    Start Jupyter Lab from the command line:

    ```bash
    jupyter lab
    ```

    Create an empty notebook and run the following importing commands:

    ```python
    import sarxarray
    import stmtools
    import numpy as np
    import geopandas as gpd
    import dask
    from dask import visualize
    ```

    If you don't see any error, you are ready for the workshop!