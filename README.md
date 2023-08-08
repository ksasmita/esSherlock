# esSherlock
This repository contains segmentation task data on the first episode of BBC series Sherlock Holmes: A Study in Pink (McGuigan, 2010). 

**About**

This document details the data collection procedure for the movie Sherlock Holmes. It complements the neural data from the open repository: https://openneuro.org/datasets/ds001132/versions/1.0.0/00003 published originally in: Chen, J., Leong, Y., Honey, C. et al. Shared memories reveal shared structure in neural activity across individuals. Nat Neurosci 20, 115–125 (2017). https://doi.org/10.1038/nn.4450

**Task overview**

<img width="980" alt="image" src="https://github.com/ksasmita/esSherlock/assets/20369844/abf588f9-39af-4be3-87ae-b0fc7b57a214">
 
Participants performed the segmentation task on 10x5 minute clips (mean duration = 299.78s) extracted from the Sherlock Holmes episode used in Chen et al., 2017. Separate groups of participants performed coarse (n = 11) and fine (n = 13) segmentation. 
Prior to the start of the experiment, all participants completed a practice task until they reached performance criterion (fine = 15-36, coarse = 3-8 button presses per minute). 

**Materials**

_Practice task_ 
* 2-minute video from the movie 3 Backyards (Mendelsohn, 2010) presented in two clips (1 minute and 1:03 minutes each). 
* The first 3s of the second clip overlapped with the last 3s of the first clip. 
_Segmentation task_
* 48.15 minutes (2888.8s) video of Sherlock Holmes: A Study in Pink divided into 10 clips (mean duration = 299.78s).
* Note that we removed the 7s blank screens at the end and the cartoon clip at the beginning of each movie run used in the original Sherlock paper (Chen et al., 2017). 
* To construct the clips, we first divided the Sherlock video into 5-minute chunks. We then extended the ends of each clip to the nearest scene cut (mean extension duration = 11.05s). Next, we included the extended portion of each clip to the beginning of the following clip (except for the first clip). 

**Participants** 

Coarse segmentation (N = 11), Fine segmentation (N = 13). 

**Segmentation Data**

File: esSherlock_SegmentData.csv

File headers: 

bpTime (button press time relative to the start of the 48-min video stimuli), subid (subject ID), clipNo (index of the 5m-clip the button press originated from), bp (total number of button presses made for the listed clipNo). 

Segmentation data has been preprocessed in the following way: 
* Button presses that occurred within 500ms from the previous one were removed (indicate recording artifact).
* Button presses within each clip had been adjusted to account for the overlap at the start of each clip (other than clip no 1) and referenced to the start of the Sherlock episode.
* Button press times across all clips were then concatenated to create a time series that reflected boundary times for the full length of the video stimuli.
