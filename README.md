![image](https://github.com/user-attachments/assets/d15a09c6-36a3-4fa2-b836-a5b889a58f75)# SATELLITE-IMAGING-AND-DEEP-LEARNING IN MODERN AGRICULTURE



Crop Classification: Deep learning models can effectively distinguish between different 
crop types, such as wheat, corn, soybeans, and rice, based on the spectral signatures 
captured by satellites. This information is crucial for farm management, enabling farmers 
to optimize resource allocation, track planting progress, and ensure compliance with crop 
rotation practices.
 Crop Health Monitoring: Satellite images can reveal subtle variations in vegetation 
health, often invisible to the naked eye. Deep learning algorithms can detect these changes, 
allowing for early identification of stress factors such as drought, disease, or pest 
infestation. Early detection enables farmers to take timely corrective measures and 
minimize crop losses [4].
 The potential applications of satellite imaging and deep learning in agriculture extend far 
beyond these examples. These technologies can be used for land-use monitoring, detecting 
deforestation for illegal farming practices, and tracking the spread of invasive species. 
They can also be integrated with other agricultural technologies, such as smart irrigation 
systems and autonomous farm machinery, to create a truly intelligent and interconnected 
agricultural ecosystem.
 However, implementing these technologies presents certain challenges. The accuracy of 
deep learning models relies heavily on the quality and quantity of training data. 
Additionally, the computational power required to train and run complex deep learning 
models can be significant. Furthermore, ensuring equitable access to this technology for 
small-scale farmers in developing countries is crucial for widespread adoption and 
maximizing its impact on global food security. Despite these challenges, the potential 
benefits of satellite imaging and deep learning for modern agriculture are undeniable[7]. 
By harnessing the power of these technologies, we can move towards a future of 
sustainable and efficient agriculture, ensuring food security for a growing population while 
protecting our precious natural resources. This thesis delves deeper into this exciting field, 
exploring the specific applications of satellite imaging and deep learning in modern 
agriculture, analyzing their impact on various aspects of farm management, and discussing 
the challenges and opportunities that lie ahead.

 Utilizing Copernicus Satellite Portal, Sentinel-2 satellite imagery is processed to extract 
spectral features crucial for accurate crop classification. Traditional monitoring methods 
often face limitations in terms of scalability and accuracy. Therefore a more robust 
approach is required such that the classification and assessment of crops is marginalized, 
The capabilities of Sentinel- 2 imagery using Copernicus Satellite Portal a cloud-based 
platform offers extensive access to Sentinel-2 satellite imagery which is the subsequent 
dataset for this project.
 The initial phase focuses on the implementation of deep learning algorithms, notably U
Net Image Segmentation Model, for crop segmentation and then classifying the crops 
based on extracted features. The subsequent step involves health assessment, utilizing 
vegetation indices a to create a comprehensive scoring system, providing quantitative 
insights into crop vitality.

![image](https://github.com/user-attachments/assets/ae862c7b-fcff-40b5-b3d9-5c7cb662b0d9)

![image](https://github.com/user-attachments/assets/9e9ce00d-e663-4d7f-9d2b-f6d52beb9e99)

![image](https://github.com/user-attachments/assets/030f64a4-7b02-406a-903c-e8926ca9702b)



 The crop classification methodology starts with data acquisition from the Copernicus Satellite 
Database, specifically utilizing the Sentinel II satellite images. These images provide a high- 
resolution view of the Earth's surface, capturing detailed information about vegetation and land
 37
cover. Once the satellite data is acquired, the next step is data preprocessing. This crucial phase 
involves cleaning and preparing the raw data, which may include correcting distortions caused 
by the satellite's movement, aligning the images to ensure consistency, and filtering out any 
noise or irrelevant information. This preprocessing step ensures that the data is in an optimal 
state for further analysis.
 Next, the methodology involves calculating the Normalized Difference Vegetation Index 
(NDVI), a critical metric for assessing vegetation health and density. NDVI is computed using 
the visible and near-infrared light reflected by the vegetation, providing a clear indicator of plant 
health. Once the NDVI indices are calculated, the large satellite images are divided into smaller, 
more manageable sections, a process known as tiling. This division makes it easier to handle and 
analyze the data in smaller chunks. Following tiling, segmentation is performed on these smaller 
sections. Segmentation is the process of partitioning an image into distinct regions based on 
similar characteristics, such as different crop types. This step is crucial for identifying and 
delineating various crops within the satellite images.
 After segmentation, the next critical phase in the crop classification methodology involves 
employing supervised learning techniques to train machine learning models. Supervised learning 
relies on labeled data, where each segment of the satellite imagery is associated with known 
crop types. This labeled data serves as the basis for teaching the model to accurately classify 
new segments in the image data.
 During training, the supervised learning model learns patterns and features that distinguish one 
crop type from another. This process allows the model to generalize from the training data, 
enabling it to classify segments in new satellite images based on the learned patterns.
 Following the training phase, the final steps in the crop classification process include prediction 
and review. The trained model applies its learned knowledge to predict the crop types present 
within each segmented area of the satellite imagery. These predictions are then subjected to a 
rigorous review process to ensure their accuracy and reliability.
 This review typically involves comparing the model's predictions with ground truth data, which 
may include field observations or expert assessments. By validating the predicted crop types 
against real-world data, any discrepancies or errors can be identified and corrected, thereby 
improving the overall accuracy of the classification results.
 By following this detailed methodology, accurate crop classification can be achieved, providing 
valuable information for agricultural management and planning. This approach not only
 38
enhances the efficiency of crop monitoring and management but also supports informed
 decision-making regarding crop rotations, pest management strategies, and resource allocation 
in agriculture.
 Spectral indices are calculated to extract detailed information from satellite imagery, which is 
essential for analyzing agricultural fields. Indices like NDVI which has been used in this project 
enhance the detection of vegetation health by using specific bands of light, such as red and near- 
infrared. These indices highlight differences in plant health, with healthy vegetation reflecting 
more near-infrared and less red light, leading to higher index values. Calculating multiple 
indices provides a comprehensive view of crop conditions, capturing details that single-band 
analysis might miss. This enriched data improves the accuracy of machine learning models used 
for crop classification by offering diverse spectral information. Additionally, spectral indices 
help monitor crop growth over time, detect anomalies and stress factors like pests or water 
shortages, and enable precision agriculture practices by optimizing resource management. In the
 39
workflow, stacking these indices into a single image enhances the dataset, facilitating more 
effective segmentation and classification, ultimately leading to better insights and decision- 
making in crop management.
 This project incorporates a simple yet effective data augmentation technique: horizontal 
flipping. This method involves flipping the images horizontally, which helps to increase the 
diversity of the training data. Data augmentation is crucial in machine learning, especially when 
working with limited datasets, as it helps to create variations of the training images without the 
need for additional data collection. By flipping the images, the model is exposed to different 
perspectives of the same scene, enhancing its ability to generalize and recognize features 
regardless of their orientation. This approach is particularly useful in remote sensing 
applications where objects or patterns, such as vegetation, can appear in various orientations due 
to changes in satellite angles or natural variations in the landscape. Horizontal flipping is a 
straightforward yet powerful augmentation technique that contributes to improving the 
robustness and accuracy of the segmentation model.
 The images were resized and reduced from the size of 450 Mb to 9.20 Mb. This helped to reduce 
the time in which model was trained. Although reduction of the size resulted in some of the 
features not be able to be captured by the model.
 Since the dataset used was too large to handle, the images were tiled. Tiling was used to break 
down large images into smaller, manageable sections or tiles. This division helped in efficiently 
processing and analyzing extensive image datasets. It allowed multiple segments of the image to 
be analyzed concurrently, which accelerated the segmentation process. Moreover, this approach 
enhanced the accuracy of segmentation by enabling localized analysis, where algorithms can 
more precisely identify and delineate features within each tile..

 Segmentation involves several key steps. It starts with data augmentation, where images are 
randomly flipped horizontally and vertically to increase variability and robustness. The 
augmented data is then used to create TensorFlow datasets for training, validation, and testing, 
with preprocessing functions applied to resize and scale the images. A neural network model is 
compiled with the Adam optimizer and a sparse categorical focal loss function to handle class 
imbalances. The model is trained over multiple epochs, with training progress monitored using 
accuracy metrics and a custom callback to visualize predictions after each epoch. Finally, the 
trained model's performance is evaluated by comparing its predictions to the ground truth, and 
the results are visualized to assess the segmentation quality.

 Masking in image processing, especially in the context of agricultural applications using satellite 
imagery, involves selectively focusing on specific areas of an image that are relevant for 
analysis while ignoring or removing the irrelevant parts.
 Masking helps to get rid of unwanted parts of an image that could mess up the analysis. By 
masking out these parts, the analysis can concentrate on the fields, leading to more accurate and 
reliable results. In agriculture, this means looking only at the crop fields and ignoring everything 
else. This focus ensures that the analysis is relevant and efficient, providing insights specifically 
about the crops. Moreover by removing irrelevant areas from the image, we can significantly 
improve the accuracy of classification algorithms. Non-crop areas can look very different from 
crops in the satellite images, and including them can confuse the algorithms. Masking makessure 
that only the crop areas are considered, leading to more accurate identification and classification 
of different crop types. After the segmentation is done, the training model plays its part in compiling the U-Net model 
with the Adam optimizer and Sparse Categorical Focal Loss to handle class imbalance 
effectively. The model is evaluated using accuracy metrics. A custom callback 
(DisplayCallback) is used to visualize sample predictions after each epoch, providing real-time 
feedback on the model's performance. The model is trained for 20 epochs using the training 
dataset (train_ds), and its performance is validated on the validation dataset (val_ds). The 
training process involves iterating through the dataset, updating model weights to minimize the 
loss, and tracking the accuracy to ensure the model learns to segment the images correctly.

 CROP HEALTH ASSESSMENT
 Crop health assessment using NDVI involves utilizing remote sensing technology to evaluate the 
condition and vigor of crops based on their vegetation indices. NDVI quantifies the difference 
between near-infrared (NIR) and red light reflectance from plants, giving a numerical estimate 
of vegetation density and health.In practice, NDVI values range from -1 to +1:
 44
 High NDVI Values: Close to +1 indicate dense, healthy vegetation where plants 
are actively photosynthesizing. This is because healthy plants absorb more red light 
for chlorophyll production and reflect a significant amount of NIR light.
  Low NDVI Values: Near zero or negative values suggest sparse vegetation cover or 
non- vegetated surfaces like soil or water. This could be due to stress factors such as 
water scarcity, nutrient deficiencies, pests, diseases, or environmental damage, causing 
plants to reflect more red light and less NIR light.
 By capturing NDVI data through satellite imagery or drone-mounted sensors, farmers and 
agricultural specialists can monitor crop health over large areas more efficiently than traditional 
ground-based methods. This technology enables early detection of stress conditions before they 
become visually apparent, allowing for timely interventions such as targeted irrigation, 
fertilizer application, or pest management. Ultimately, leveraging NDVI for crop health 
assessment supports sustainable farming practices by optimizing resource use, enhancing crop 
productivity, and minimizing environmental impact.
 In essence, NDVI-based crop health assessment represents a pivotal advancement in modern 
agriculture, enabling informed decision-making and sustainable practices that contribute to 
enhanced productivity and resilience in farming operations



















