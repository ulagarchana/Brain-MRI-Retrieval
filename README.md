# Brain-MRI-Retrieval 

**Course**: CSE 515 - Multimedia and Web Databases  
**Phase**: Project Phase 1  
**Group 4**
---

## **Team Members**  
- Ulagarchana Ulaga Narasimhan  
- Harshini Balamurugan Vadivazhagi 
- Pranav Mandava  
- Siddharth Mehta  

---

## **Project Overview**  
This project implements a **Content-Based Image Retrieval (CBIR)** system for **Brain MRI scans**.  

We use a hybrid of **handcrafted features (HOG)** and **deep learning features (ResNet-AvgPool-512)** to represent images and retrieve the **top-k most similar MRI scans** from the dataset.  

---

## **Key Highlights**  
- **HOG (Histogram of Oriented Gradients)** – captures edges and structure (504-dimensional feature vector).  
- **ResNet-AvgPool-512** – captures high-level semantic patterns using pretrained ResNet50.  
- **Similarity Measures**:  
  - Euclidean Distance → HOG features.  
  - Cosine Similarity → ResNet features.  
- **Retrieval Output**: Query image + Top-5 similar dataset images with similarity scores.  
- Entire workflow runs on **Google Colab**.  

---

## **Folder Setup**  

In your **Google Drive**, create the following structure:  

```

CSE515\_Phase1/
│── dataset/
│   └── phase1\_data/          # dataset images
│── queries/
│   └── phase1\_queries/       # query images
│── Code/
│   ├── CSE515\_PHASE1\_t01.ipynb   # Tasks 0 & 1
│   ├── CSE515\_PHASE1\_t23.ipynb   # Tasks 2 & 3

````

---

## **Execution Instructions (Google Colab)**  

1. Upload the `CSE515_Phase1` folder to **Google Drive**.  
2. Mount Drive in Colab:  
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
````

3. Open and run the appropriate notebook:

   * `CSE515_PHASE1_t01.ipynb` → Tasks 0 & 1
   * `CSE515_PHASE1_t23.ipynb` → Tasks 2 & 3
4. Provide the query image path and choose **k**:

   ```
   Enter full path to query image: /content/drive/MyDrive/CSE515_Phase1/queries/phase1_queries/brain_menin_0001.jpg
   Enter k: 5
   ```
5. The notebook will display the **query image + top-k retrieved results** with similarity scores.

---

## **Results**

* **HOG**: Captured edges and textures.
* **ResNet**: Captured high-level semantic features.
* Retrieval was consistent → retrieved MRI scans had strong visual resemblance to the queries.

---

## **Inferences**

* **HOG** is effective for structural patterns.
* **ResNet** improves retrieval by leveraging deep semantic information.
* Hybrid systems combining both are promising for medical image retrieval tasks.

---

## **References**

1. Dalal, N., & Triggs, B. (2005). *Histograms of Oriented Gradients for Human Detection*. CVPR.
2. He, K., Zhang, X., Ren, S., & Sun, J. (2016). *Deep Residual Learning for Image Recognition*. CVPR.
