# human-image-detection
A deep learning project for human identification using ResNet50 and LFW dataset
# 🧑‍💻 Human Identification Using Deep Learning  

## 📌 Overview  
This project implements a **human face identification system** using **deep learning**. It leverages the **Labeled Faces in the Wild (LFW)** dataset and a **transfer learning approach with ResNet50** to classify images of different individuals.  

The system is capable of:  
- Detecting and classifying human faces into identities.  
- Training on multiple classes of people with high accuracy.  
- Supporting **real-time image predictions** for new, unseen faces.  



## 🗂️ Dataset  
- **Source**: [Labeled Faces in the Wild (LFW)](http://vis-www.cs.umass.edu/lfw/) dataset.  
- **Details**: Contains 13,000+ face images of over 5,700 people, collected from the web.  
- **Usage in project**: Only individuals with at least **50 face samples** are included for better performance.  



## ⚙️ Project Workflow  
1. **Data Preprocessing**  
   - Resize & normalize images.  
   - Convert grayscale to RGB (for ResNet compatibility).  
   - One-hot encode labels.  

2. **Data Augmentation**  
   - Random rotations, shifts, and flips to avoid overfitting.  

3. **Model Architecture**  
   - **Base model**: Pre-trained ResNet50 (ImageNet weights, frozen layers).  
   - **Custom layers**:  
     - Global Average Pooling  
     - Dense (ReLU)  
     - Dropout  
     - Softmax output for classification  

4. **Training**  
   - Optimizer: Adam  
   - Loss: Categorical Crossentropy  
   - Epochs: 10 (adjustable)  
   - Batch Size: 32  

5. **Evaluation**  
   - Accuracy & loss curves plotted.  
   - Confusion matrix (optional).  

6. **Real-Time Prediction**  
   - Ability to classify a **new image** not in training set.  


## 📊 Results  
- Achieved **~90% accuracy** on test set.  
- Robust generalization on unseen images.  
- Successful predictions on real-time test images.  


## 🖼️ Example Output  
```plaintext
True: George_W_Bush
Predicted: George_W_Bush
✅ Correct identification
