# DroneVehicle-Night夜间子集简介

**DroneVehicle-Night**数据集基于 **DroneVehicle** 数据集筛选和处理得到，主要提取了其中具有夜间特征的可见光图像，并在原始标注文件基础上进行了格式转换。  
在此对 **DroneVehicle** 数据集的原始贡献者 **天津大学VisDrone团队** 致以诚挚感谢 🙏。   

📊 Dataset Statistics / 数据集规模
| Split     | Images | Resolution | Annotation Type |
| --------- | ------ | ---------- | --------------- |
| **Train** | 10,357 | 840×712    | OBB             |
| **Val**   | 868    | 840×712    | OBB             |
| **Test**  | 6,013  | 840×712    | OBB             |

目标类别统计如下：

🚗 Car：241,285

🚚 Truck：9,305

🚌 Bus：9,846

🚐 Van：7,405

🚛 Freight Car：7,978

覆盖典型夜间无人机场景：城市道路、居民区、停车场 等多样环境。

包含 **10,357 对训练图像、868 对验证图像和 6,013 对测试图像**，每幅图像分辨率为 **840×712 像素**。  
在原始 XML 标注文件的基础上，经过格式转换，生成了以 **旋转边界框（Oriented Bounding Box, OBB）** 为核心的标注文件，相较于传统水平边界框更适合无人机航拍等复杂场景下的检测任务。数据涵盖多种典型无人机视角下的夜间场景，包括 **城市道路、居民区、停车场** 等。  
目标类别主要集中在车辆相关目标，包括：
- 汽车：241,285 个实例  
- 卡车：9,305 个实例  
- 公共汽车：9,846 个实例  
- 面包车：7,405 个实例  
- 货车：7,978 个实例

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
