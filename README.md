# DroneVehicle-Night夜间子集简介

  **DroneVehicle-Night**数据集基于 **DroneVehicle** 数据集筛选和处理得到，主要提取了其中具有夜间特征的可见光图像，并在原始标注文件基础上进行了格式转换。  
  在此对 **DroneVehicle** 数据集的原始贡献者 **天津大学VisDrone团队** 致以诚挚感谢 🙏。   

  包含 **10,357 对训练图像、868 对验证图像和 6,013 对测试图像**，每幅图像分辨率为 **840×712 像素**。  
  在原始 XML 标注文件的基础上，经过格式转换，生成了以 **旋转边界框（Oriented Bounding Box, OBB）** 为核心的标注文件，相较于传统水平边界框更适合无人机航拍等复杂场景下的检测任务。数据涵盖多种典型无人机视角下的夜间场景，包括 **城市道路、居民区、停车场** 等。  目标类别主要集中在车辆相关目标，包括：

  🚗 Car：241,285 个实例

  🚚 Truck：9,305 个实例

  🚌 Bus：9,846 个实例

  🚐 Van：7,405 个实例 

  🚛 Freight Car：7,978 个实例


  📊 Dataset Statistics / 数据集规模
  | Split     | Images | Resolution | Annotation Type |
  | --------- | ------ | ---------- | --------------- |
  | **Train** | 10,357 | 840×712    | OBB             |
  | **Val**   | 868    | 840×712    | OBB             |
  | **Test**  | 6,013  | 840×712    | OBB             |
  
  
  ## 📊 Benchmark Results on DroneVehicle-Night

**Table Simple performance evaluation on the DroneVehicle-Night dataset**

### RGB-based Methods

| Method        | Publication | Backbone        | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|---------------|-------------|-----------------|----------|-----|-------|-------------|-----|-----|--------|
| Faster R-CNN  | TPAMI 2017  | ResNet-50       | RGB      | 74.9 | 27.5 | 28.0 | 77.4 | 40.3 | 49.6 |
| RetinaNet     | ICCV 2017   | ResNet-50       | RGB      | 72.5 | 12.2 | 23.4 | 49.4 | 31.0 | 37.7 |
| S²A-Net       | TGRS 2021   | ResNet-50       | RGB      | 72.2 | 21.1 | 23.8 | 78.1 | 36.8 | 46.4 |
| YOLOv8s       | Ultralytics 2023 | CSPDarkNet53 | RGB | 88.6 | 45.7 | 52.5 | 89.6 | 52.3 | 65.7 |

---

### Infrared-based Methods

| Method        | Publication | Backbone        | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|---------------|-------------|-----------------|----------|-----|-------|-------------|-----|-----|--------|
| Faster R-CNN  | TPAMI 2017  | ResNet-50       | IR       | 89.8 | 47.4 | 52.2 | 88.2 | 48.0 | 65.1 |
| RetinaNet     | ICCV 2017   | ResNet-50       | IR       | 89.1 | 18.2 | 35.3 | 70.3 | 32.9 | 49.2 |
| S²A-Net       | TGRS 2021   | ResNet-50       | IR       | 89.4 | 41.8 | **56.6** | 88.9 | 45.8 | 64.5 |
| YOLOv8s       | Ultralytics 2023 | CSPDarkNet53 | IR | **98.1** | 69.3 | 75.8 | **96.5** | 58.7 | 79.7 |

---

### RGB-IR Fusion Methods

| Method        | Publication | Backbone        | Modality | Car | Truck | Freight_car | Bus | Van | mAP@50 |
|---------------|-------------|-----------------|----------|-----|-------|-------------|-----|-----|--------|
| CFT           | arXiv 2022  | CSPDarkNet53    | RGB+IR   | 97.4 | 71.2 | 75.5 | 96.3 | 61.6 | 80.4 |
| CALNet        | ACM MM 2023 | CSPDarkNet53    | RGB+IR   | 89.8 | 72.6 | 68.9 | 88.8 | 59.0 | 75.8 |
| C²Former      | TGRS 2024   | ResNet-50      | RGB+IR   | 90.0 | 67.2 | 62.9 | 89.1 | 57.8 | 73.4 |
| ICARFusion    | PR 2024     | CSPDarkNet53   | RGB+IR   | **98.1** | 77.2 | **81.2** | 96.1 | 64.0 | 83.3 |
| DAMSDet       | ECCV 2024   | ResNet-50      | RGB+IR   | 95.8 | 72.5 | 79.4 | 94.2 | 64.0 | 81.2 |
| M³D-LIF       | ICCV 2025   | CSPDarkNet53   | RGB+IR   | 97.6 | **80.9** | 76.0 | 96.1 | **68.9** | **83.9** |
| MS2Fusion     | Inf. Fusion 2025 | CSPDarkNet53 | RGB+IR | 98.2 | 75.4 | 79.2 | 96.2 | 65.2 | 82.8 |

**Notes:**
- All results are evaluated on the **DroneVehicle-Night** test set.
- Metrics are reported in **mAP@0.5 (%)**.
- Bold numbers indicate the **best performance** in each column.
- Backbone and modality information follow the original implementations.


## 🔗 Download / 下载地址
- [Baidu Netdisk / 百度网盘](https://pan.baidu.com/s/1Oe7g_4c5XHPeuFsqphmumg) Code:4av6
- [Google Drive / 谷歌网盘](https://drive.google.com/file/d/1kjbTMPQSJsbf_XD5Hi1T1A7F8ukaugHx/view?usp=sharing)

📝 **Citation / 参考文献**：

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


❤️ **Acknowledgment / 致谢**

- 感谢 VisDrone Team (TJU) 提供原始 DroneVehicle 数据集支持。
