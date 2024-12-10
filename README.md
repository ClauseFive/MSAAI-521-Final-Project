#### **Project Title**  
**Underwater Trash Detection with Object Detection**

---

### **Introduction**  
Marine pollution poses significant challenges to ocean ecosystems and biodiversity. This project leverages advanced object detection methods to tackle underwater trash detection. Utilizing YOLOv10, a state-of-the-art object recognition model, this project aims to detect marine debris efficiently and accurately, aiding environmental conservation efforts.

---

### **Methodology**  

#### **Model Selection**  
We use the YOLOv10 model for its high performance in object detection tasks. This model's dual-head architecture enables enhanced accuracy through a combination of one-to-one and one-to-many labeling approaches. 

#### **Dataset**  
The TrashCan dataset from JAMSTEC is used, featuring 7,212 annotated images focused on underwater debris. This dataset ensures robust training by covering diverse trash types and underwater conditions.[Link](https://conservancy.umn.edu/items/6dd6a960-c44a-4510-a679-efb8c82ebfb7)

#### **Preprocessing**  
Data annotations, provided in COCO format, are converted to YOLO format for compatibility. Preprocessing involves normalizing bounding boxes and generating a `dataset.yaml` file to define training and validation parameters.

#### **Training Setup**  
The YOLOv10n model is trained on 6,065 images for 10 epochs using augmentation techniques like flipping, resizing, and color adjustments. The lightweight architecture enables deployment on resource-constrained devices such as remotely operated vehicles (ROVs).

---

### **Results and Analysis**  

- **Validation Batch Predictions**  
  Generated visual outputs confirm the model's ability to detect underwater trash with high confidence.
  
- **Performance Metrics**  
  - **F1-Confidence Curve**: Optimal balance achieved at a confidence threshold of 0.274 with an F1 score of 0.62.  
  - **Precision-Confidence Curve**: Precision peaks at a threshold of 1.0, reflecting low false positives.  
  - **Recall-Confidence Curve**: Recall reaches 0.89, indicating high sensitivity in detecting debris.  
  - **Confusion Matrix**: Highlights areas of misclassification, providing insight into model improvement opportunities.

---

### **Integration with Autonomous Systems**  
The YOLOv10n model integrates seamlessly with ROVs, enabling real-time underwater trash detection. These systems provide enhanced precision and autonomy, reducing human intervention and optimizing resource allocation for marine cleanup efforts.

---

### **Conclusion**  
This project demonstrates the efficacy of YOLOv10n in addressing marine pollution through automated trash detection. The results underscore the potential of AI-driven object detection in promoting sustainable ocean conservation.

---

### **References**  
- Dupont, M. (2024). Comparing YOLOv10 with other object detection models. *LabelVisor*. [Link](https://www.labelvisor.com/comparing-yolov10-with-other-object-detection-models/)  
- Potrimba, P. (2024). What is YOLOv10? *Roboflow*. [Link](https://blog.roboflow.com/what-is-yolov10)  
- Bochkovskiy, A., Wang, C.-Y., & Liao, H.-Y. M. (2024). YOLOv10: Towards more efficient object detection models. *arXiv*. [Link](https://arxiv.org/html/2402.16370v1)  
- Wang, J., Han, Q., Ge, K., & Sun, L. (2024). Marine garbage detection for turbid and high-dynamic underwater environments using CSC-YOLO and Mobile SAM. *SSRN*. [Link](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5021819)
