## Instructions

This demo contains two `.m` files and a `models` folder with one `.json` file.

Running `MoAEpilot_run.m` performs the following steps:

- The data of `sub-01` is downloaded in the current directory from http://www.fil.ion.ucl.ac.uk/spm/download/data/MoAEpilot/MoAEpilot.bids.zip and unzipped

- The data is slice timing corrected,

- Then spatially preprocessed with the following steps:

    -   realign and unwarp,  coregistration `func` to `anat`, `anat` segmentation,
        normalization to MNI space

- Smoothed (default FWHM is set to 6mm)

- Quality analysis for the anatomical data

- GLM at the subject level

- The contrast defined in the `model-MoAE_smdl.json` file is performed: `listening < baseline`

All processed data will be found in a `derivatives` folder, created in the current directory.
