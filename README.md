# Analysis of Deblurring and Object Detection using Richardson-Lucy Algorithm and YOLO Model

**Course:** COMP6001 — Computer Vision and Multimodal Machine Learning

**Student:** Arif Kunto Wibisono

**Student ID:** a1915248

**Institution:** Adelaide University

## Project Description ✨
This project investigates the relationship between classical image deblurring methods and object detection performance using COCO 2017 dataset. Two deblurring methods were implemented: Wiener filtering and Richardson-Lucy (RL) filtering. Both methods use an estimated Gaussian Point Spread Function (PSF) rather than a measured one. Blur intensity was calculated using Fast Fourier Transform (FFT) and categorised into three levels: very blurry, blur, and slightly blurry. Quantitative evaluation using Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity Index Measure (SSIM) revealed that both deblurring methods failed to improve the image quality, with metrics decline after deblurring process due to mismatch PSF. Object detection was performed using YOLO version 11 medium model across blur, deblurred, and sharp image types. The detection metrics used in this report are precision, recall, mAP50, mAP50-95, and F1-score. Results showed that deblurred images achieved the lowest detection performance across all metrics. A fine-tuned YOLO model trained on RL-filtering deblurred images was also evaluated, showing that while it partially adapted to the deblurred image, it had significant trade off to performance on blur and sharp images. These findings highlight that PSF accuracy is substantial in classical image deblurring methods and that improper application of deblurring is detrimental to object detection task afterwards.

## Requirements 📜
- Python 3.9 or higher
- YOLO version 11 medium
- GPU recommended
- Key libraries in Python:
    - opencv-python
    - ultralytics
    - scikit-image
    - pandas
    - numpy
    - matplotlib
    - seaborn
    - os
    - shutil
    - glob
    - time

## Hadrware Specification 💻
- Device: ASUS TUF A 15
- Processor: AMD Ryzen 9 8945
- RAM: 32 GB
- Integrated GPU: AMD Radeon 780M
- Dedicated GPU: NVidia GeForce RTX 4060 8GB

## Usage and Installation 📈

### Clone the repository
git clone https://github.com/arifkuntow/computer_vision_assignment_1.it
### Download the dataset
Download the blurry version of COCO 2017 dataset in https://www.kaggle.com/datasets/iamravigarg/cocoblur
Download the validation images and annotations from COCO 2017 dataset from https://cocodataset.org/#download
### Extract The Ground Truth
Extract the ground truth label from data/instances_val2017.json
### Extract the yaml file
Extract the yaml file and copy it to train_test_split folder

### Folder Structure
ai_logs: to store the generative AI logs
data: to store the images used in this project
notebooks: to store the notebooks used in this project

### Data Folder
Put the blur images on blur folder and sharp images on sharp folder

### Jupyter Notebook Description
- wiener_deblurring.ipynb: to run the wiener deblurring and analyse the result
- richardson_deblurring.ipynb: to run the richardson-lucy deblurring and analyse the result
- object_detection.ipynb: to run the YOLO model on the images and analyse the result
- training_yolo.ipynb: to train the YOLO model, run it on the dataset, and analyse the result

## License 💸
This project is for academic purposes only as part of a university assignment. All rights reserved.

## Contact Information 👨‍💻
GitHub: https://github.com/arifkuntow/computer_vision_assignment_1