# Food-Classification-using-Convolutional-neural-network




Implementation:
The function get_prediction is an inference function for detection, classification, and semantic segmentation tasks, depending on which inputs you choose. Implemented in modules.py, where the image detection process will call the Edamam API to get nutritional information in the food. We also save nutritional information in CSV files in the folder /static/csv. 

We provide the user with the ability to customize the threshold of confidence and so that the user can find a suitable threshold for the input image. In order not to have to rerun the whole model every time these parameters are changed, when the image is sent from the client, the server will perform a perceptual hash encryption algorithm to encrypt the image and use that resulting string to name the image when saving to the server. This helps when the client sends an image whose encoding already exists in the database, the server will only post-process the previously predicted result without re-executing the prediction.

Sample Results:

![5](https://github.com/SukeshRondla/Food-Classification-using-Convolutional-neural-network/assets/65500920/27148bf3-0678-4326-abba-39722ff9d454)
![4](https://github.com/SukeshRondla/Food-Classification-using-Convolutional-neural-network/assets/65500920/80224509-772b-4ea8-a2c0-443c9e71bf4d)


Dataset:
To train the food detection model, we survey the following datasets:
Open Images V6-Food: Open Images V6 is a huge dataset from Google for Computer Vision tasks. To solve our problem, we extracted from a large dataset of food-related labels. The extracted set includes 18 labels with more than 20,000 images.
School Lunch Dataset: includes 3940 photos of a bunch of Japanese high school students, taken at the same frontal angle with the goal of assessing student nutrition. Labels consist of coordinates and types of dishes are attached and divided into 21 different words, in the dataset there is also a label "Other Foods" if the dishes do not belong to the remaining 20 words.
Vietnamese Food: a self-collected dataset on Vietnamese dishes, including 10 simple dishes of our country such as Pho, Com Tam, Hu Tieu, and Banh Mi,... Each category has about 20-30 images, divided 80-20 for training and evaluation.
