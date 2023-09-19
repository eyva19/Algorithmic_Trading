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

### 2.1 Tune the Baseline Trading Algorithm (DateOffset was changed to 6 months)
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

### 2.2 Tune the Baseline Trading Algorithm (DateOffset was changed to 6 months and short_window = 15, long_window = 250)

For class -1.0 Tuned Model_v2 provides a more balanced performance between precision and recall compared to Tuned Model, which has a higher precision but significantly lower recall.
The F1-score for Tuned Model_V2 for class -1.0 is better than that of Tuned Model (0.54 vs. 0.29).

For class 1.0 Tuned Model_v2 has lower recall vs Tuned Model (0.55 vs 0.89).
However, Tuned Model_v2 has a more balanced precision and recall, resulting in a lower F1-score than Tuned Model (0.57 vs. 0.70).

Tuned Model_v2 provides a more balanced performance across both classes.


### Evaluate a New Machine Learning Classifier

##### New Model vs. Baseline Model 
Class -1.0 Performance: The Baseline Model has good precision but poor recall, similar to the New Model which has lower precision and similarly poor recall.
F1-scores for both models for class -1.0 are quite close (0.13 for the New Model vs. 0.12 for the Baseline).

Class 1.0 Performance: The New Model has a slightly lower precision (0.56 vs. 0.63) but high recall (0.92). The F1-score for the New Model is slightly lower for class 1.0 (0.70 vs. 0.77).

The New Model has a lower accuracy (0.55 vs. 0.64).
Both macro and weighted average F1-scores for the Baseline Model are better than those of the New Model.

The New Model has a larger dataset (4092 samples vs 128 for the Baseline Model). 
The Baseline Model, despite its challenges with recall for class -1.0, overall outperforms the New Model in terms of accuracy and F1-scores. The Baseline Model performs better than the New Model.

##### New Model vs. Tuned Model_v2
Class -1.0 Performance: the Tuned Model_v2 outperforms the New Model in terms of precision, recall, and F1-score for class -1.0. The Tuned Model_v2 is more balanced, resulting in a higher F1-score.

Class 1.0 Performance: the New Model has a slightly lower precision than the Tuned Model_v2, but a much higher recall.However, the F1-score for the Tuned Model_v2 is slightly lower for class 1.0 compared to the New Model.

The Tuned Model_v2 has a marginally higher accuracy than the New Model (0.56 vs. 0.55).
Both macro and weighted average F1-scores for the Tuned Model_v2 are better than those of the New Model. The Tuned Model_v2 performs better than the New Model.