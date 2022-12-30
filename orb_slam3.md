## ORB SLAM3

## System
> Entire SLAM system.

- Use TrackMonocular to inject measurements.
- Construction:
  1. Vocabulary file
  2. Settings file
  3. Input sensor type
  4. Sequence Name

**Steps:**
1. Initialize the SLAM system.
2. Launches
  1. **Tracking** on main thread.
  2. **LocalMapping** on separate thread.
  3. **LoopClosing** on seperate thread.

## Tracker
- Process sensor information and compute the pose of the current frame with respect to active map in realtime.
- It also decides whether current frame becomes a keyframe.

- GrabImuData
  * Stores Queue of IMU data between frames.
- GrabImageMonocular
  * Create mCurrentFrame from image and meta data
  * Track()
  * mCurrentFrame.GetPose()

**timestamp(Double):** 

## Frame
- Image (cv::MAT, Grayscale)
- TimeStamp (Double)
- ORB Extractor
- ORB Vocabulary
- GeometricCamera
- Distortion Cofficient
- Previous Frame
- Threshold close/far points
- Imu Calib

## LocalMapping
- Adds keyframes and points to active map, remove redundent once and refines the map using visual/visual inertial bundle adjustment operating a local window of keyframes close to the current frame.

## LoopClosing
- Detects common regions between the active map and the whole atlas at keyframe rate.
- If common area belongs to active map, it performs loop correction.
- If it belongs to a different map, both maps are seamlessly mearged into a single one, that becomes the active map.
- After a loop correction a full bundle adjustment is launched in an independent thread to further refine the map without affecting real-time performance.
