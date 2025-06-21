# A Novel Object Detection Model for Sugar Beet Cercospora Leaf Spot in Field Scenarios Based on Large Kernel Decomposition and Spatial Channel Interaction Attention (Under review)

Cercospora leaf spot (CLS) is a widespread disease that seriously threatens beet yield and sugar quality. Timely detection enables farmers to take early control measures and reduce economic losses. Although artificial intelligence (AI)-based methods are replacing manual inspection in agriculture, CLS detection in complex field environments remains highly challenging due to subtle early-stage symptoms and severe occlusions caused by overlapping leaves and weeds. To address these challenges, this paper presents Cercospora Leaf Spot–You Only Look Once (CLS–YOLO), an enhanced detection model built upon You Only Look Once version 11 (YOLOv11), incorporating novel modules specifically designed for accurate CLS detection under challenging field conditions. To improve the detection of weak and early-stage symptoms, we design the Multi-Scale Large Kernel Decomposition (MSLKD) module, which enhances feature extraction for subtle lesions. Furthermore, we develop the Spatial-Channel Interaction Attention (SCIA) module to mitigate detection errors arising from occlusion and fragmented dis- ease patterns by refining multi-scale feature representations. Experimental results demonstrate CLS–YOLO achieves superior performance, reaching an mAP@0.5 of 73.6% ± 0.2% and an mAP@0.5:0.95 of 40.6% ± 0.3% over five independent runs, outperforming twelve mainstream object detection algorithms while maintaining lightweight efficiency. To validate generalization capability across scenarios, crops, and diseases, we conducted comparative experiments on two public crop disease datasets, where our method achieved superior overall performance. In summary, this study provides an effective AI-driven solution for precise crop disease detection, contributing to the practical advancement of intelligent agriculture.

## REQUIREMENTS
We implemented our code in Python, and you need to follow the Ultralytics installation guide to set up the required environment: [https://docs.ultralytics.com/quickstart](https://docs.ultralytics.com/quickstart).

## DATASETS
The sugar beet Cercospora leaf spot data used in this study were collected in Shihezi City, Xinjiang Uygur Autonomous Region, China (44◦18′19′′N, 86◦4′49′′E). Shihezi City was selected as the data collection site due to its extensive sugar beet cultivation areas and high incidence of CLS, providing an ideal environment for capturing a diverse range of natural infection scenarios.

Our dataset has been uploaded to [Google Drive](https://drive.google.com/drive/folders/1nsIK0I0ZrUTsJPf-d21hOPyw3DMudYFB?usp=drive_link).

### Processing dataset
Because of storage constraints, users are expected to apply the data augmentation steps by following the descriptions provided in the paper.

## Running Experiments 
Following the official Ultralytics documentation, users can construct the YAML file for the CLS dataset. Then, training can be initiated with the following command: yolo detect train data=CLS.yaml model=yolo11s.yaml epochs=100 imgsz=1280

You need to first unzip the CLS-YOLO.zip file. Our module is implemented within the yolo11o.yaml configuration file.
