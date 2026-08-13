# Prompt2Point

**A Prompt-Driven, LiDAR-Free Dataset for Dynamic Volumetric Quality Assessment**

Prompt2Point is an open-source dataset for objective quality assessment of dynamic volumetric media. It provides **synchronized per-frame mesh (OBJ) and point cloud (PLY) sequences** generated through a fully reproducible, prompt-driven pipeline — no LiDAR or multi-camera capture hardware required.

Unlike capture-based datasets, Prompt2Point provides **noise-free, topology-consistent mesh ground truths**, enabling precise full-reference distortion analysis, perceptual metric calibration, and cross-representation quality benchmarking.

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

```text
Text/Image Prompt
       ↓
    MeshyAI
       ↓
  Rigged FBX
       ↓
    Blender
(Frame Extraction)
       ↓
 Per-frame OBJ
       ↓
CloudCompare / PyMeshLab
       ↓
 Per-frame PLY
```

All post-processing relies on open tools, including **Blender**, **CloudCompare**, and **PyMeshLab**.

The released dataset is fully self-contained and does **not** require access to MeshyAI for reuse.

## Paper

📄 **Prompt2Point: A Reference-Based Dataset for Dynamic Volumetric Quality Assessment**

**Jashanjot Singh Sidhu and Abdelhak Bentaleb**  
*2026 18th International Conference on Quality of Multimedia Experience (QoMEX)*  
Pages 1–7, 2026.

**DOI:** [10.1109/QoMEX69967.2026.11617375](https://doi.org/10.1109/QoMEX69967.2026.11617375)

## Citation

If you use **Prompt2Point** in your research, please cite our paper:

### IEEE Reference Format

```text
J. S. Sidhu and A. Bentaleb, "Prompt2Point: A Reference-Based Dataset for Dynamic Volumetric Quality Assessment," in 2026 18th International Conference on Quality of Multimedia Experience (QoMEX), 2026, pp. 1–7, doi: 10.1109/QoMEX69967.2026.11617375.
```

### BibTeX

```bibtex
@inproceedings{sidhu2026prompt2point,
  author    = {Sidhu, Jashanjot Singh and Bentaleb, Abdelhak},
  title     = {{Prompt2Point}: A Reference-Based Dataset for Dynamic Volumetric Quality Assessment},
  booktitle = {2026 18th International Conference on Quality of Multimedia Experience (QoMEX)},
  year      = {2026},
  pages     = {1--7},
  doi       = {10.1109/QoMEX69967.2026.11617375}
}
```

## License

Please refer to the dataset download page for licensing details.

## Contact

For questions or issues, please open a GitHub issue.
