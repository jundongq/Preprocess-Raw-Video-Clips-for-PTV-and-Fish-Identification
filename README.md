# Preprocess-Raw-Video-Clips-for-PTV-and-Fish-Identification
use python, opencv to preprocess video clips for PTV analysis and fish identification

## Directory Structure:
+ data
  - video clips (in mp4 or other readable formats)
  - img_pre.py
  - frameExtractor.py
  - imgUndistortion.py
  - imgReflectionRemove.py
  - calibration_data.npz (camera calibration data, which includes distortion coefficients and camera matrix)

## Usage:
python img_pre.py -v FishBehavior.mp4 -n 6 -cp calibration_data.npz 
