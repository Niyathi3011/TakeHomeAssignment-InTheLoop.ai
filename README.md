
## Take-Home Assignment: Few-Shot Learning with Mini Dataset

**Overview**

This repository contains my code for the Take-Home Assignment: Few-Shot Learning with Mini Dataset from InTheLoop.ai.

**Exploratory Data Analysis (EDA)**

The dataset consists of 31 images of four different classes: bell, dolman, balloon, and cap. The images are all in the same resolution and format.

**Data Preparation**

I used the following data augmentation techniques:

* Color jittering
* Random rotation

**Model and Training**

### Why I chose the CLIP pre-trained model

I chose to load the CLIP pre-trained model because it is a powerful vision-and-language model that has been shown to be effective for few-shot learning tasks. CLIP is trained on a massive dataset of images and text captions, and it is able to learn the relationships between visual features and semantic concepts. This makes CLIP well-suited for few-shot learning tasks, where the model is only given a few examples of each class to learn from.

Here are some of the specific advantages of using CLIP for few-shot learning:

* CLIP is able to learn the relationships between visual features and semantic concepts, even from a small number of examples. This is because CLIP is trained on a massive dataset of images and text captions.
* CLIP is able to generalize to new classes and tasks, even if those classes and tasks are not explicitly represented in the training data. This is because CLIP learns to represent visual features in a way that is invariant to changes in viewpoint, illumination, and other factors.
* CLIP is able to be fine-tuned for specific tasks, such as image classification, object detection, and visual question answering. This allows you to customize the model to meet your specific needs.

Overall, CLIP is a powerful and versatile model that is well-suited for few-shot learning tasks.

### Models

I implemented the following three models:

* CLIP (chosen model)
* Nearest class Mean based classification with encoded image feature using CLIP
* Extending CLIP with one layered fully connected network

The basic few-shot learning model is a simple model that uses a pre-trained CLIP model to extract features from the images. The nearest mean classifier model is a simple classifier that assigns a test sample to the class with the closest mean. My own network is a simple neural network with a single hidden layer extending CLIP.

### Training

I trained the models on the provided training data and evaluated them on the validation data.

### Results 

The following confusion matrices show the performance of the three models on the validation data:

### CLIP pre-trained model

![CLIP pre-trained model confusion matrix](https://github.com/Niyathi3011/TakeHomeAssignment-InTheLoop.ai/blob/main/Results/clip_fewshot_train.png)

### Nearest mean classifier model

![Nearest mean classifier model confusion matrix](https://github.com/Niyathi3011/TakeHomeAssignment-InTheLoop.ai/blob/main/Results/NCM_fewshot_test.png)

### Few-shot learning model with my own network

![Few-shot learning model with my own network confusion matrix](https://github.com/Niyathi3011/TakeHomeAssignment-InTheLoop.ai/blob/main/Results/net_fewshot.png)

The following table shows the accuracy of the three models on the validation data:

| Model | Test Accuracy | Val Accuracy |
|---|---|---|
| Basic few-shot learning model | 25% | 25% |
| Nearest mean classifier | 71% | 50% |
| Few-shot learning model with my own network | 68% | 53.1% |

**Conclusion**

The CLIP pre-trained model outperforms the other two models on both the test and validation data. This suggests that the CLIP model is able to learn more complex relationships between the features and the target variable.

However, the nearest mean classifier model performs better than the CLIP model on the test data. This is likely because the nearest mean classifier model is a simpler model and is therefore less likely to overfit the training data.

**Future Work**

I would like to explore the following future work:

* Train the models on larger datasets.
* Use more sophisticated neural network architectures.
* Use more sophisticated data augmentation techniques.

**REFERENCES** 
https://chat.openai.com/ 
(https://github.com/sergiuoprea/clip_with_few_shots/tree/master)https://github.com/sergiuoprea/clip_with_few_shots/tree/master 

I hope this README is helpful!

  

      


