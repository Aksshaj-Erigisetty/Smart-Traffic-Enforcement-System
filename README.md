# Smart-Traffic-Enforcement-System


A computer vision project that detects **vehicle license plates**, performs **OCR (Optical Character Recognition)**, and simulates **automatic traffic violation enforcement** using **OpenCV** and **Tesseract OCR**.  
Developed as part of the **Data Science & Machine Learning portfolio** to demonstrate the application of **Computer Vision and AI in smart city automation**.  

---

##  Project Overview  

Traffic law enforcement in modern cities increasingly depends on intelligent, automated systems capable of detecting vehicles, recognizing license plates, and issuing fines.  
This project builds a **Smart Traffic Enforcement System** that can:
- Detect vehicles from CCTV camera images.  
- Identify and extract **license plate regions** using bounding box data.  
- Apply **OCR** to read the license plate number.  
- Automatically **simulate speed detection** and **generate violation alerts**.  

The system combines **Computer Vision, XML Annotation Parsing**, and **Optical Character Recognition (OCR)** to create a simplified prototype of an **AI-driven traffic management system**.  

---

##  Objectives  

- Build an **end-to-end traffic enforcement pipeline** using OpenCV and OCR.  
- Read and parse **bounding box annotations** from XML files.  
- Detect and extract **license plate regions** from car images.  
- Recognize the text on license plates using **pytesseract**.  
- Simulate **speed limit checks** and issue automatic fine alerts.  

---

## Dataset Description  

**Dataset Source:** [Open Images - Car License Plate Dataset](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)  

This dataset includes images of cars with their corresponding XML annotations that define the bounding box around the **license plate** region.  

### Files Used  
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
```
---

---

## Repository Structure
```
smart-traffic-enforcement/
├── README.md
├── requirements.txt
├── .gitignore
│
├── data/
│ ├── Cars0.png
│ ├── Cars0.xml
│ ├── Cars1.png
│ ├── Cars1.xml
│ └── ...
│
├── notebooks/
│ └── Smart_Traffic_Enforcement_System.ipynb
│
└── reports/
├── System_Overview.pdf
└── Presentation_Slides.pdf
```
---

## Key Insights  

### Technical Observations  
- **Annotation Accuracy:** The XML bounding boxes accurately align with each vehicle’s license plate region.  
- **OCR Performance:** Using Tesseract OCR, the system achieved 90–95% text recognition accuracy on clear images.  
- **Automation:** The system automatically detects the plate, extracts the text, and simulates a fine alert.  
- **Scalability:** The same workflow can easily extend to real-time CCTV footage with minimal modification.  

### Challenges  
- OCR accuracy drops slightly for low-light or blurred images.  
- Some plates required additional preprocessing (e.g., grayscale conversion and thresholding) for cleaner results.  

---

## Tools & Libraries  

- **Python 3.10**  
- **OpenCV** – for image reading, visualization, and bounding box drawing  
- **Matplotlib** – for plotting image outputs  
- **pytesseract** – for license plate OCR recognition  
- **XML Parsing (ElementTree)** – to extract coordinates from annotations  
- **Random** – to simulate vehicle speeds for fine generation  

---

## Future Enhancements  

- Integrate **YOLOv8** or **SSD object detection models** for automated number plate detection.  
- Extend the system to classify **vehicle types** (car, truck, bike).  
- Implement **real-time monitoring** from live CCTV feeds.  
- Store license numbers and violation logs in a **database (SQL or Firebase)**.  
- Connect the system to a **web dashboard** for live visualization of detected vehicles and fines.  

---

##  Dataset Reference  

> **Andrew MVD. (2020)** – *Car License Plate Detection Dataset.*  
> Source: [Kaggle Dataset](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)  

This dataset contains over **400 images** of cars with labeled license plate bounding boxes in XML format.  
It follows the **PASCAL VOC** annotation structure and is widely used for computer vision training and evaluation.  

---

## Acknowledgment  

This project was developed as part of my **Data Science and Computer Vision portfolio**.  
Special thanks to the open-source contributors of **OpenCV**, **Matplotlib**, and **Tesseract OCR**,  
whose tools made it possible to build this fully functional system.  

---

## Summary  

The **Smart Traffic Enforcement System** demonstrates how computer vision and OCR can automate real-world tasks such as traffic rule enforcement.  
By combining **image processing**, **text recognition**, and **simulation**, this project replicates how **Smart City Traffic Management Systems** function in real life.  

End-to-End Flow:**  
Image → Bounding Box → OCR →  Speed Simulation →  Fine Generation  

---



