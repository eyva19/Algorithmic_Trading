# Algorithmic_Trading

### 1. Establish a Baseline Performance

#####  Class -1.0 (When Actual Returns are less than 0)
Precision: The model has a precision of 1.00 for this class, it means that every time the model predicted a sample to be of class -1.0, it is always correct.

Recall: The recall 0.06 is low. This indicating that the model identified only 6% actual samples of class -1.0.
F1-score: The F1-score is 0.12,this low score reflects the model's poor overall performance for this class due to the very low recall.

##### Class 1.0 (When Actual Returns are greater than or equal to 0):
Precision: The model's precision is 0.63, which means that 63% of the samples predicted as class 1.0 were actually of this class.
Recall: The recall is 1.00, indicating that the model identified all actual samples of class 1.0 correctly.
F1-score: The F1-score is 0.77, it indicates a good balance between precision and recall for this class.

##### Overall Performance:
Accuracy: is 0.64, meaning the model correctly predicted the class for 64% of all samples.
Macro Avg: the average precision and recall for the two classes is 0.82 and 0.53, respectively, with an F1-score of 0.44.
Weighted Avg: the average precision is 0.77, recall is 0.64, and F1-score is 0.52.

##### Conclusions:
The model is good at predicting when it's class -1.0, but hasca very high number of false negatives for this class.
For class 1.0, the model performs well and identifies all cases.
While the model's overall accuracy is decent at 0.64, the extremely low recall for class -1.0 is a concern.
Adjustments or a different approach might be needed for balanced performance for this model.

### 2. Tune the Baseline Trading Algorithm (DateOffset was changed to 6 months)
Class -1.0:
Moderate precision (0.59) and low recall (0.20).
Tuned Model has a  better job at identifying class -1.0 than initial baseline Model but still misses many instances.
Class 1.0:
Tuned Model has a similar precision (0.58) as for class -1.0, but much better recall (0.89).
Tuned Model has an accuracy of 0.58 and weighted average F1-score of 0.52.

##### Conclusions:
Tuned Model provides a more balanced performance, but still has challenges with recall for class -1.0
Tuned Model has lower recall for class 1.0 compared to baseline Model.
Neither the Tuned Model nor the Baseline Model are ideal for class -1.0, with both struggling with recall.
Choice between models would depend on the specific requirements and costs associated with false positives and false negatives in the application.