# Smart-Traffic-Enforcement-System


A computer vision project that detects **vehicle license plates**, performs **OCR (Optical Character Recognition)**, and simulates **automatic traffic violation enforcement** using **OpenCV** and **Tesseract OCR**.  
Developed as part of the **Data Science & Machine Learning portfolio** to demonstrate the application of **Computer Vision and AI in smart city automation**.  

---

## 🚦 Project Overview  

Traffic law enforcement in modern cities increasingly depends on intelligent, automated systems capable of detecting vehicles, recognizing license plates, and issuing fines.  
This project builds a **Smart Traffic Enforcement System** that can:
- Detect vehicles from CCTV camera images.  
- Identify and extract **license plate regions** using bounding box data.  
- Apply **OCR** to read the license plate number.  
- Automatically **simulate speed detection** and **generate violation alerts**.  

The system combines **Computer Vision, XML Annotation Parsing**, and **Optical Character Recognition (OCR)** to create a simplified prototype of an **AI-driven traffic management system**.  

---

## 🧩 Objectives  

- Build an **end-to-end traffic enforcement pipeline** using OpenCV and OCR.  
- Read and parse **bounding box annotations** from XML files.  
- Detect and extract **license plate regions** from car images.  
- Recognize the text on license plates using **pytesseract**.  
- Simulate **speed limit checks** and issue automatic fine alerts.  

---

## 🗃️ Dataset Description  

**Dataset Source:** [Open Images - Car License Plate Dataset](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)  

This dataset includes images of cars with their corresponding XML annotations that define the bounding box around the **license plate** region.  

### 📁 Files Used  
- `.png` — car images  
- `.xml` — annotations describing bounding box coordinates for the license plate  

Each XML file follows the **PASCAL VOC** annotation format. Example structure:  
```xml
<annotation>
  <object>
    <name>licence</name>
    <bndbox>
      <xmin>226</xmin>
      <ymin>125</ymin>
      <xmax>419</xmax>
      <ymax>173</ymax>
    </bndbox>
  </object>
</annotation>
