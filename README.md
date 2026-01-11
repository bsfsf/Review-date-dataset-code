## DroneVehicle-Night Subset Overview

**DroneVehicle-Night** is a curated nighttime subset derived from the **DroneVehicle** dataset.  
It is constructed by selectively extracting visible-light images with distinct nighttime characteristics and converting the original annotation files into a unified format.

We would like to express our sincere gratitude to the original contributors of the **DroneVehicle** dataset, the **VisDrone Team at Tianjin University**, for their invaluable efforts and publicly available resources 🙏.

The dataset contains **10,357 training image pairs, 868 validation image pairs, and 6,013 test image pairs**, with each image having a resolution of **840 × 712 pixels**.  
Based on the original XML annotations, all labels are converted into **Oriented Bounding Box (OBB)** annotations. Compared with conventional horizontal bounding boxes, OBB annotations are more suitable for object detection in complex UAV aerial scenarios, especially under nighttime conditions.

The dataset covers a wide range of typical nighttime UAV scenes, including **urban roads, residential areas, and parking lots**.  
Target categories mainly focus on vehicle-related objects, as detailed below:

- 🚗 **Car**: 241,285 instances  
- 🚚 **Truck**: 9,305 instances  
- 🚌 **Bus**: 9,846 instances  
- 🚐 **Van**: 7,405 instances  
- 🚛 **Freight Car**: 7,978 instances  

### 📊 Dataset Statistics

| Split | Images | Resolution | Annotation Type |
|:------:|:-----------:|:--------:|:--------:|
| **Train** | 10,357 | 840 × 712 | OBB |
| **Val** | 868 | 840 × 712 | OBB |
| **Test** | 6,013 | 840 × 712 | OBB |

  
  
## ⭐ Benchmark Results on DroneVehicle-Night

**Table Simple performance evaluation on the DroneVehicle-Night dataset**

## RGB-based Methods

| Method | Publication | Backbone | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|:------:|:-----------:|:--------:|:--------:|:---:|:-----:|:-----------:|:---:|:---:|:------:|
| Faster R-CNN | TPAMI 2017 | ResNet-50 | RGB | 74.9 | 27.5 | 28.0 | 77.4 | 40.3 | 49.6 |
| RetinaNet | ICCV 2017 | ResNet-50 | RGB | 72.5 | 12.2 | 23.4 | 49.4 | 31.0 | 37.7 |
| S²A-Net | TGRS 2021 | ResNet-50 | RGB | 72.2 | 21.1 | 23.8 | 78.1 | 36.8 | 46.4 |
| YOLOv8s | Ultralytics 2023 | CSPDarkNet53 | RGB | **88.6** | **45.7** | **52.5** | **89.6** | **52.3** | **65.7** |

---

## Infrared-based Methods

| Method        | Publication | Backbone        | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|:------:|:-----------:|:--------:|:--------:|:---:|:-----:|:-----------:|:---:|:---:|:------:|
| Faster R-CNN  | TPAMI 2017  | ResNet-50       | IR       | 89.8 | 47.4 | 52.2 | 88.2 | 48.0 | 65.1 |
| RetinaNet     | ICCV 2017   | ResNet-50       | IR       | 89.1 | 18.2 | 35.3 | 70.3 | 32.9 | 49.2 |
| S²A-Net       | TGRS 2021   | ResNet-50       | IR       | 89.4 | 41.8 | 56.6 | 88.9 | 45.8 | 64.5 |
| YOLOv8s       | Ultralytics 2023 | CSPDarkNet53 | IR | **98.1** | **69.3** | **75.8** | **96.5** | **58.7** | **79.7** |

---

## RGB-IR Fusion Methods

| Method        | Publication | Backbone        | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|:------:|:-----------:|:--------:|:--------:|:---:|:-----:|:-----------:|:---:|:---:|:------:|
| CFT           | arXiv 2022  | CSPDarkNet53    | RGB+IR   | 97.4 | 71.2 | 75.5 | **96.3** | 61.6 | 80.4 |
| CALNet        | ACM MM 2023 | CSPDarkNet53    | RGB+IR   | 89.8 | 72.6 | 68.9 | 88.8 | 59.0 | 75.8 |
| C²Former      | TGRS 2024   | ResNet-50       | RGB+IR   | 90.0 | 67.2 | 62.9 | 89.1 | 57.8 | 73.4 |
| ICAFusion     | PR 2024     | CSPDarkNet53    | RGB+IR   | 98.1 | 77.2 | **81.2** | 96.1 | 64.0 | 83.3 |
| DAMSDet       | ECCV 2024   | ResNet-50       | RGB+IR   | 95.8 | 72.5 | 79.4 | 94.2 | 64.0 | 81.2 |
| M²D-LIF       | ICCV 2025   | CSPDarkNet53    | RGB+IR   | 97.6 | **80.9** | 76.0 | 96.1 | **68.9** | **83.9** |
| MS2Fusion     | Inf. Fusion 2025 | CSPDarkNet53 | RGB+IR | **98.2** | 75.4 | 79.2 | 96.2 | 65.2 | 82.8 |

**Notes:**
- All results are evaluated on the **DroneVehicle-Night** Val set.
- Metrics are reported in **mAP@0.5 (%)**.
- Bold numbers indicate the **best performance** in each column.
- Backbone and modality information follow the original implementations.


## 🔗 Download
- [Baidu Netdisk](https://pan.baidu.com/s/1Oe7g_4c5XHPeuFsqphmumg) (Code:4av6)
- [Google Drive](https://drive.google.com/file/d/1kjbTMPQSJsbf_XD5Hi1T1A7F8ukaugHx/view?usp=sharing)

📝 **Citation**：

```bibtex
@article{sun2022drone,
  title={Drone-based RGB-infrared cross-modality vehicle detection via uncertainty-aware learning},
  author={Sun, Yiming and Cao, Bing and Zhu, Pengfei and Hu, Qinghua},
  journal={IEEE Transactions on Circuits and Systems for Video Technology},
  volume={32},
  number={10},
  pages={6700--6713},
  year={2022},
  publisher={IEEE}
}


❤️ Acknowledgment

   We sincerely thank the VisDrone Team (Tianjin University) for providing the original DroneVehicle dataset.

