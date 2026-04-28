# Prompt2Point

A Prompt-Driven, LiDAR-Free Dataset for Dynamic Volumetric Quality Assessment

---

Prompt2Point is an open-source dataset for objective quality assessment of dynamic volumetric media. It provides **synchronized per-frame mesh (OBJ) and point cloud (PLY) sequences** generated through a fully reproducible, prompt-driven pipeline — no LiDAR or multi-camera capture hardware required.

Unlike capture-based datasets, Prompt2Point offers **noise-free, topology-consistent mesh ground truths**, enabling precise full-reference distortion analysis, perceptual metric calibration, and cross-representation quality benchmarking.

## Dataset Overview

| | |
|---|---|
| **Avatars** | Girl, Robot, Soldier, WSoldier, ZombieDoll |
| **Animations per avatar** | 5 (locomotion, combat, acrobatics, dance, gestures) |
| **Total sequences** | 25 single-object + multi-object composite scenes |
| **Formats** | Per-frame OBJ meshes + PLY point clouds |
| **Frame rates** | 30 fps (default), 60 fps (Soldier, WSoldier) |
| **Points per frame** | ~650K–2M |

Composite multi-object scenes with controlled inter-object occlusion are also included for evaluating visibility-aware culling and tile-based streaming.

## Download

The full dataset (meshes, point clouds, FBX assets, and conversion scripts) is publicly available:

🔗 **[Download Prompt2Point Dataset](https://tinyurl.com/Prompt2point)**

## Pipeline

    Text/Image Prompt → MeshyAI → Rigged FBX → Blender (frame extraction) → Per-frame OBJ
                                                                               ↓
                                                             CloudCompare / PyMeshLab → PLY

All post-processing relies on open tools (Blender, CloudCompare, PyMeshLab). The dataset is fully self-contained and does not require access to MeshyAI for reuse.

## Paper

📄 Coming soon.

## License

Please refer to the dataset download page for licensing details.

## Contact

For questions or issues, please open a GitHub issue.
