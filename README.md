# Food-Classification-using-Convolutional-neural-network


Implementation:
The "get_prediction" function serves as a versatile tool for tasks such as detection, classification, and semantic segmentation. Its implementation can be found in the "modules.py" module. The process involves interfacing with the Edamam API to extract nutritional data from food images for image detection. This nutritional information is then stored in CSV files in the "/static/csv" directory.

Granted users the ability to personalize confidence thresholds. This empowers them to identify the optimal threshold for input images. A perceptual hash encryption algorithm is employed to prevent the need for re-running the entire model whenever these parameters change. This algorithm encrypts the image, generating a resultant string used for naming and storing the image on the server. This strategic approach proves advantageous when the client sends an image with an encoding already present in the database. In such instances, the server simply carries out post-processing on the pre-predicted result, avoiding the need for re-executing the prediction process.

Sample Results:

![5](https://github.com/SukeshRondla/Food-Classification-using-Convolutional-neural-network/assets/65500920/27148bf3-0678-4326-abba-39722ff9d454)
![4](https://github.com/SukeshRondla/Food-Classification-using-Convolutional-neural-network/assets/65500920/80224509-772b-4ea8-a2c0-443c9e71bf4d)


Dataset:
- Open Images V6-Food: We utilized the extensive Open Images V6 dataset, primarily focusing on food-related labels. Our extraction yielded 18 specific labels, encompassing over 20,000 images.
- School Lunch Dataset: This collection comprises 3,940 photographs capturing Japanese high school students. All images are taken from a consistent frontal angle and serve the purpose of evaluating student nutrition. The dataset contains 21 distinct labels, indicating the types of dishes along  with their coordinates. Notably, an "Other Foods" label is present for categorizing dishes not falling within the defined 20 categories.
- Vietnamese Food: We curated a dataset showcasing traditional Vietnamese dishes. This self-collected dataset showcases 10 common Vietnamese dishes, such as Pho, Com Tam, Hu Tieu, and Banh Mi. Each category is represented by approximately 20 to 30 images, with an 80-20 split for training and evaluation purposes.
