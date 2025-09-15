# **Brain MRI Image Retrieval using HOG and ResNet Features**

**Course**: CSE 515 - Multimedia and Web Databases  
**Phase**: Project Phase 1  
**Group 4**
---

## **Team Members**  
Ulagarchana Ulaga Narasimhan  
Harshini Balamurugan Vadivazhagi       
Pranav Mandava  
Siddharth Mehta  

---

## **Project Overview**  
This project explores feature extraction and image retrieval techniques by implementing Histograms of Oriented Gradients (HOG) and ResNet variant models on a dataset of brain MRI images. These models visualize the image and extract the corresponding feature descriptors. We then store the features and compute the similarity or distance between the images to retrieve most similar k images in the dataset. This project uses python as the programming environment, pytorch as the deep learning library and torchvision as the visual information extraction package. The outcomes indicate the ability of different models to visualize image features and their similarity. 

---

## **Key Highlights**  
- **HOG (Histogram of Oriented Gradients)** – feature descriptor that uses magnitude and angle of the gradient to compute features. It focuses on capturing the edges and structure of an object in an image.  
- **ResNet-AvgPool-512** – feature vector driven from the layers of a pretrained deep neural network, ResNet50. It utilizes average pooling to reduce the dimensionality of its feature map to 512 channels. 
- **Similarity Measures**:  
  - Euclidean Distance for HOG features.  
  - Cosine Similarity for ResNet features.  
- **k-NN Retrieval**: Finds the k most similar images with respective similarity scores using distance or similarity functions for given query image.
- Entire workflow runs on Google Colab.  

---

## **System Requirements**  

- **Platform**: Google Colab  
- **Python Version**: 3.9+  
- **Hardware**: Colab in-built CPU  
- **Libraries**:  
  - torch  
  - torchvision  
  - scikit-image  
  - scikit-learn  
  - matplotlib  
  - pandas  
  - opencv-python

---

## **Folder Setup**  

In **Google Drive**, create the following structure:  

```

CSE515/_Phase1/
│── dataset/
│   └── phase1/_data/          # dataset images
│── queries/
│   └── phase1/_queries/       # query images
│── Code/
│   ├── code01.ipynb   # Tasks 0 & 1
│   ├── code02.ipynb   # Tasks 2 & 3

````

---

## **Execution Instructions (Google Colab)**  

1. Upload the `CSE515_Phase1` folder to Google Drive.
2. All the data images and query images are uploaded to the google drive.
3. The dataset images are inside the /content/drive/MyDrive/phase1_data folder.
4. The query images are inside the /content/drive/MyDrive/phase1_queries folder.
5. Mount to google drive. Set path accordingly.
4. Open and run the appropriate notebook:

   * `code01.ipynb` → Tasks 0 & 1
   * `code02.ipynb` → Tasks 2 & 3
5. Provide the query image path and choose k:

   ```
   Enter full path to query image: /content/drive/MyDrive/CSE515_Phase1/queries/phase1_queries/brain_menin_0001.jpg
   Enter k: 5
   ```
6. The notebook will display the query image + top-k retrieved results with similarity scores.

---

## **Results**

**HOG**: Captured edges and textures.            
**ResNet**: Captured high-level semantic features.          
Retrieved MRI images had strong visual resemblance to the queries indicating that retrieval was consistent.

