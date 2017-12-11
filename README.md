# Preprocess-Raw-Video-Clips-for-PTV-and-Fish-Identification
use python, opencv to preprocess video clips for PTV analysis and fish identification

## Directory Structure:
```
+ data
  - video clips (in .mp4 or other readable formats)
  - img_pre.py
  - frameExtractor.py
  - imgUndistortion.py
  - imgReflectionRemove.py
  - calibration_data.npz (camera calibration data, which includes distortion coefficients and camera matrix)
```
## Usage:
cd data

python img_pre.py -v FishBehaviorExample.mp4 -n 6 -cp calibration_data.npz 

this code will sample 1 frame from 'FishBehaviorExample.mp4' in every 6 frames, and generate a subdirectory 'sampledFrames'; then all sampled frames will be undistorted and stored in 2nd new subdictory 'Undistorted'; then the light reflection on all undistorted images will be removed and the preprocessed images will be stored in 3rd new subdictory 'UndistortedPreprocessed'.

So, the resulted directory structure is:
```
+ data
  + FishBehaviorExample
    + sampledFrames
      - *.png
    + Undistorted
      - *.png
    + UndistortedPreprocessed
      - *.png
```
