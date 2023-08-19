# Noise2Seg: Automatic Few-Shot Selection from Noisy Web Data for Underwater Tropical Fishes Segmentation
## Project Steps:

Scrapped web-collected data set available [here](https://www.kaggle.com/datasets/naumanullah/qatar-tropical-fishes-10-qtf-10). our obtained real-world noisy Qatar Tropical Fishes data set contains 10 categories with 5,341 web-collected images from Google image databases, the training set contains 4,841, and the test set is 500 samples respectively.

# 1. Automatic Data Acquisition
![ds_creation_pipeline](https://github.com/GilalNauman/Automatic-Few-shot-Selction-ISNCC/assets/62802429/66e279d2-0396-47dd-b704-cbff9d6e2beb)

Auto dataset creation pipeline: Starting from the taxonomy of tropical fishes found in Qatar obtained through the public resource Qatar e-Nature, we use a Python script integrated with Chrome Drivers and Selenium that is able to communicate with the web browser.

# 2. Few-shot Selection Process
![overview](https://github.com/GilalNauman/Automatic-Few-shot-Selction-ISNCC/assets/62802429/c8fe98b9-2158-4a59-a268-1ac1fa858a72)

Fig.2. Overview of Automatic FSS: Our automatic FSS scheme operates on the QTF-10 web-collected dataset $D$, which comprises a mixture of noisy and clean samples. We employ an auto-cleaning scheme that utilized transfer learning via EfficientNet. This involves calculating the losses and eliminating images with higher losses. Subsequently, we rank the remaining losses and select the images with the minimum loss as high-quality samples. To annotate the selected images, we employed the roboflow online tool. Finally, we perform YOLOv8 segmentation on the annotated images.

# 3. Results

![image](https://github.com/GilalNauman/Automatic-Few-shot-Selction-ISNCC/assets/62802429/6d851396-f3d6-4a97-8878-035887e56dc7)


![image](https://github.com/GilalNauman/Automatic-Few-shot-Selction-ISNCC/assets/62802429/8220d015-3801-4724-81d3-d96e8c2b5e56)


![image](https://github.com/GilalNauman/Automatic-Few-shot-Selction-ISNCC/assets/62802429/cd79299e-7e8f-4715-b710-84c4251567da)
The visual segmentation results on QTF-10 dataset: The top row displays the manual FSS; the middle row exhibits the automatic segmentation results using FSS with a baseline approach; and finally, the bottom row shows the automatic segmentation outcomes using FSS with a cleaning scheme, employing five images per class. While the red bounding box colors signify where predictions are incorrect and missing.

More Visual Segmentation results:

https://www.dropbox.com/s/8u9ss4ea50hv4r6/Noise2Seg.mp4?dl=0
