# esSherlock
This repository contains segmentation task data on the first episode of BBC series Sherlock Holmes: A Study in Pink (McGuigan, 2010). 

**About**

This document contains details on data collection procedure for the stimuli: Sherlock Holmes. It complements neural data from the open repository: https://openneuro.org/datasets/ds001132/versions/1.0.0/00003

**Task overview**

![image](https://github.com/ksasmita/esSherlock/assets/20369844/9240b204-4339-409d-8650-9e6e7a17fb24)
 
Participants performed the segmentation task on the ~50 minute episode of Sherlock Holmes: Study in Pink (REF). Participants performed the segmentation task in video chunks, each lasting approximately 5 minute long (mean duration = 299.78s). Separate groups of participants performed the task in coarse (n = 11) and fine (n = 13) grains. 
All participants completed a practice task before they began segmenting. Practice was performed to criterion (fine = XX, coarse = XX button presses per minute). 

**Materials**

_Practice task_ 
* 2-minute video from the movie 3 Backyards (Mendelsohn, 2010) presented in two clips (1 minute and 1:03 minutes each). 
* The first 3s of the second clip overlapped with the last 3s of the first clip. 
_Segmentation task_
* 48.12 minutes (2778.3s) of the first episode of Sherlock Holmes: Study in Pink divided into 10 clips (mean duration = 299.78s). 
* This movie stimuli do not contain the ~7s blank screens present in the stimuli used in the original Sherlock paper. 
* This movie stimuli do not contain the 39s cartoon present at the beginning of each movie run in the original Sherlock paper. 
* The first clip was constructed by first selecting the first 5 minute of the full episode. We then extended this clip to the nearest scene cut. Subsequent clips were constructed in the same way, starting from the ending of the first clip. However, for subsequent clips, we added a ~12s overlap from the 5th minute point of the previous clip to the end of the clip.  

**Procedure** 
* All participants performed the segmentation task in one grain (either fine or coarse).
* All participants started with a practice task. Practice segmentation was repeated until participants reached criterion.
* Following the practice task, participants performed the segmentation task on the Sherlock clips. Clips were presented in order. Participants were told that they were allowed to take breaks in between each clip, and they can start a new clip by pressing the “SPACEBAR”. 

**Participants** 
Demographics: esSherlock_Demo.csv 

**Segmentation Data**
File: esSherlock_SegmentData.csv
Segmentation data has been preprocessed in the following way: 
* Button presses that occurred within 500ms from the previous one was removed (indicate recording artifact).
* Button presses within each clip had been adjusted to account for the overlap at the start of each clip (other than clip no 1) and referenced to the start of the Sherlock episode.
* Button press times across all clips were then concatenated to create a timeseries that reflect boundary time points for the full length of the movie stimuli. 

