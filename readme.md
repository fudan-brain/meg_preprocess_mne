## meg preprocess

### overview

#### setup
1. mne install
```
conda install --channel=conda-forge --name=base mamba
mamba create --override-channels --channel=conda-forge --name=mne mne
```

2. freesurfer
- https://surfer.nmr.mgh.harvard.edu/

3. afni
- ttps://afni.nimh.nih.gov/pub/dist/doc/htmldoc/background_install/install_instructs/steps_linux_ubuntu20.html#quick-setup

#### preprocess steps
##### mne
1. cut data
2. denoise
3. BEM model
4. source localization

##### region-based mask
1. downsample with 3dfractionize
2. mask with hcp atlas


#### function
1. data: T1 and raw '.fif'., best with suffix '_raw_tsss_mc.fif'
2. ouput: '.mat' with 180 regions according to hcp glasser atlas.
- https://afni.nimh.nih.gov/pub/dist/atlases/MNI_HCP/MNI_Glasser_HCP_2021_v1.0a/