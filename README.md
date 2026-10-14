## Adeyemi Sadeeq

Computer vision and perception researcher. I work on one problem: keeping each object's identity while it is hidden,
in multi-object tracking and segmentation (MOTS).

**Now: Segment Anything through occlusion.** Meta's SAM 3 and SAM 3.1, zero-shot, on KITTI-MOTS and MOTS20
(validation and training splits; test-set scores not yet submitted).

| | SAM 3 | SAM 3.1 |
|---|---|---|
| KITTI-MOTS val, cars, HOTA | 82.6 | 74.6 |
| MOTS20 train, HOTA | 72.6 | 61.5 |
| Same identity after a real occlusion (245 events) | 94% | 63% |

- About half of SAM 3.1's gap comes from the tracking settings it ships with: with SAM 3's settings its car HOTA
  rises from 74.0 to 78.3.
- A Kalman-filter identity layer on SAM's output raises SAM 3.1's identities kept through occlusion from 63% to 70%,
  and does not help SAM 3: motion outside the tracker says where an object is, not who it is.
- Next: motion inside SAM 3's tracker, recovery after occlusion, and test-server submissions.

**Before that**

- An occlusion-aware tracker that keeps identities through 1 to 5 second hides: 0% to 89% in simulation, and 2% to 57%
  on real street geometry from 1,256 driving clips.
- Robotics Research Assistant, University of Maine Robotics Laboratory: ROS 2, EKF localization, lidar perception.

**Where to look**

- Portfolio, CVs and results: [sadeeqgandalf.github.io](https://sadeeqgandalf.github.io)
- Live occlusion lab: [lunar-occlusion-tracking](https://sadeeqgandalf.github.io/lunar-occlusion-tracking/track.html)
- SAM 3 / SAM 3.1 benchmark and the filter layer: [av-stack/research/sam_mots_benchmark](https://github.com/sadeeqgandalf/av-stack/tree/main/research/sam_mots_benchmark)
- Tracker and simulation code: [lunar-occlusion-tracking](https://github.com/sadeeqgandalf/lunar-occlusion-tracking)

Python, C++, PyTorch, ROS 2, OpenCV, filterpy, MATLAB, TrackEval.
Contact: [sideeqadeyemi@icloud.com](mailto:sideeqadeyemi@icloud.com)
