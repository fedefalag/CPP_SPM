## Instructions

This demo contains two `.m` files and a `.json` file in the `models` folder.

Running `MoAEpilot_run.m` performs the following steps:

- The data of `sub-01` is downloaded in the cd in bids format from http://www.fil.ion.ucl.ac.uk/spm/download/data/MoAEpilot/ and unzipped

- The data is slice timing corrected,

- Then spatially preprocessed with the following steps:

    -   realign and unwarp,  coregistration `func` to `anat`, `anat` segmentation,
        normalization to MNI space

- Smoothed (default FWHM is set to 6mm)

- Quality analysis is performed:

    -   for anatomical data
    -   for functional data

- GLM at the subject level is performed

- The contrast defined in the `model-MoAE_smdl.json` file is performed: Listening < baseline
