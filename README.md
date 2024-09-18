# Melanoma-Detection-Assignment
> Melanoma-Detection-Assignment using CNN


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)



## General Information
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. 
It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

<!-- You can include any other section that is pertinent to your problem -->

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Technologies Used
Keras
Tensor flow
  - library - version 3.0
Augmentor
  - library - version 0.2.10

Matplotlib

seaborn

PIL


<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->
### Conclusions

<img width="1584" alt="Screenshot 2024-09-18 at 11 51 03 AM" src="https://github.com/user-attachments/assets/bddc9133-2f42-465b-afe2-ea078fa0a3e3">


Based on the charts and the metrics above, here's a detailed breakdown of the observations:

---

#### 1. **Training and Validation Accuracy (Left Plot):**

- **Steady Increase in Training Accuracy:**
  The light blue line (Training Accuracy) shows a steady and consistent improvement over the 30 epochs. 
  - By the 30th epoch, the training accuracy reaches **81.03%**, indicating that the model is learning from the rebalanced dataset and improving its prediction capability on the training set.
  
- **Fluctuations in Validation Accuracy:**
  The yellow/orange line (Validation Accuracy) shows a fluctuating behavior. While there is an increasing trend, we observe sharp peaks and drops throughout the training process. This suggests:
    - **Epoch Overfitting:** The model fits very well during certain epochs but may be overfitting some parts of the dataset, leading to sudden drops in validation accuracy.
    - **Less Stable Validation Performance:** By the 30th epoch, validation accuracy reaches **75.11%**, which is still good but highlights slight instability in performance across various epochs.

---

#### 2. **Training and Validation Loss (Right Plot):**

- **Smooth Decrease in Training Loss (Green Line):**
  The training loss shows a steady decrease, which is expected when the model improves its learning during training. By the 30th epoch, the training loss is down to **0.4833**, confirming that the model is learning and minimizing the errors during training.

- **Spiking and Fluctuating Validation Loss (Red Line):**
  The validation loss is highly volatile, showing multiple peaks and drops. This is consistent with the behavior of the fluctuating validation accuracy. Some sharp spikes in validation loss can be seen between Epochs 10 and 15.
    - The **instability in validation loss** may indicate that the model is not generalizing well at certain epochs due to the rebalancing of classes.
    - However, the overall trend shows a **decreasing pattern**, ending with a **validation loss of 0.7506** in the last epoch. 
    - **Erratic peaks** are an indicator of overfitting or sensitivity to class rebalancing, meaning the model may perform worse when tested against unseen data.

---

#### 3. **Final Model Metrics (Post-Rebalancing):**

- **Training Accuracy:** **81.03%**
  - This shows that the model has learned to predict the target labels with reasonable accuracy on the training data.
  
- **Validation Accuracy:** **75.11%**
  - A 75% validation accuracy points toward a reasonable generalization capability, though there is room for improvement. The gap between training accuracy and validation accuracy (~6%) suggests slight overfitting but not very severe.

- **Training Loss:** **0.4833**
  - A fairly low training loss, meaning the model fits the training data quite well.

- **Validation Loss:** **0.7506**
  - There is a noticeable difference between training and validation loss. The **difference of ~0.27** confirms that validation data still challenges weak generalization, requiring more fine-tuning, and rebalancing might have introduced instability.

---



### Summary

- The CNN model's training performance is solid, showcasing an **81.03% training accuracy** and a **validation accuracy of 75.11%** after class rebalancing.
- **Instability** in validation accuracy and loss suggests that despite rebalancing, the model encounters difficulty generalizing consistently.
- Modifications such as early stopping, learning rate tuning, and stronger regularization strategies might reduce overfitting and boost the model's generalization to unseen melanoma data.
- Less differences between train and validation accuracies indicate that model has not overfitted
- Have used dropouts and maxpooling to reduce overfitting and increase stability
- Training Loss reduces below 0.5. However, Validation loss shows downward trend initially but increases gradually after 30 epochs
- As compared to the previous Models, this model performed better than former Models



## Acknowledgements

- This project was created as a submission for Melanoma detection assignment


## Contact
Created by [@aravindvcyber] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
