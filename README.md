# Supervised_Learning
Supervised_Learning
Case Study: Credit Risk Resampling


**Report Findings with Detailed Explanation**


**1. Findings of Classification Report of Original Prediction with Target Test (y_test) attribute:** 

Following are the findings for the Classification Report of Original Prediction with Target Test (y_test) attribute:

**Accuracy Score:** 
The Accuracy Score after considering TPs, FPs, TNs & FNs, we get the pretty high score of 0.95 i.e. 95% of accuracy in the performance of this Model. Therefore, the overall evaluation of this model states the accuracy level of 95% without breaking down at Risky & Non-Risky Loans levels.

Accuracy Score just calculates & signifies the overall confidence level of Model, and in this case when we run the Classification Report for Original Prediction with Target Test variable (y_test) it just shows that 95% accuracy rate of this Model nothing more.

**Precision Score:** 
The Precision Score is more precise than Accuracy Score for obvious reasons which is that it doesn't consider the Negatives and only focus on Positives (TPs & FPs) & particularly in this finding after considering TPs & FPs, we get:

FPs as High-Risk Loans (Value 1) was 0.85 (85%) with less confidence compared to its counterpart TPs as Healthy Loans with the reading of 1.00 (100%) i.e. the highest level of confidence in Model's Performance. Hence, the Precision Score determines the model's confidence in Healthy Loans is more as compare to Risky Loans.

**Recall Score:** 
The purpose of Recall Score is to measure the True Judgements of Model, meaning we human knows that how many are True Positive Results & False Negative Results in total which the model has missed.

Therefore, after considering TPs & FNs we get: For Value 1, 0.91 (91%) for High-Risk Loans shows the Recall Score is quite high. Whereas for Value 0, 0.99 (99%) for Healthy Loans which is quite similar to Precision Score (100%).

**F1 Score:** 
F1 Score is basically a Harmonic Mean, as a single summary statistic for the Precision and the Recall. Which actually computes after getting the Precision & Recall values and applying those values in this formula: 2 × (precision x recall) / (precision + recall).

Therefore, after computing F1 Score we get: For Value 1, 0.88 (88%) for High-Risk Loans shows the F1 Score is actually somewhere in the middle of Precision & Recall Values. Where, the Precision was 85% & Recall was 91% we get the more refined value i.e. 88% after applying the F1 Score formula. Whereas for Value 0, 1.00 (100%) confidence at 3rd level of calculation after computing Precision, Recall & F1 proves that how solid the confidence is actually lies in Healthy Loans.

**Conclusion:**
The Model Performance has been measured or evaluated by applying confusion matrix in general where we have seen that the confidence for the Values 1 & 0 with following conclusion for each of them:

1. Value 1 (High-Risk Loans): The Value 1 in particular has been varied in different accuracy tests and we get the range of 85-91% (Precision & Recall) after applying the Precision & Recall techniques. Whereas, the F1 Score which is a Harmonic Value for the Risky Loans shows the best possible value lies witin the range i.e. 88%.

This 88% shows the best possible value as the accuracy of this model after considering the TPs, FPs & FNs determining that how accurate the performance of this model is in reality.

2. Value 0 (Healthy Loans): The Value 0 shows the highest level of confidence in all 3 techniques: Precision: 100%, Recall: 99% & F1 Score: 100%. This shows that the confidence in measuring the Larger Class of Value 0 (Healthy Loans) is way too high. Machine may sound pretty confident at this level however this might get wrong in long run where machine model develops a tendency to favor Value 0 and give more precedence over Value 1.

Therefore, to avoid the unbiased behaviour we have a functionality called: Imbalanced Classes where we apply Resampling Techniques. Specifically, Oversampling is one the major technique will be leveraged for this purpose to artificially increase the size of Smaller Class so that the comparison with the Larger Class will be treated equal without getting biased, hence to get more fair results by eliminating error at fractional level.



**2. Findings of Classification Report Imbalanced of Resampled Data with Target Test (y_test) attribute:** 

**After applying "RandomOverSampler Technique"** 

Following are the findings for the Imbalanced Classification Report of Resampled Data (Predictions) with Target Test (y_test) attribute:

**Accuracy Score:** 
We get the Accuracy Score after resampling is 0.99 (99%) as compare to the Original Data's Accuracy Score which was 95%, it shows that after applying OverSampling Technique it actually improves the accuracy level.

Hence, the imbalanced oversampling technique improves the confidence level of model.


**Precision Score:** 
We get the following Precision Score readings for Values: 1 & 0 after Resampling:

FPs as High-Risk Loans (Value 1): Precision Score is 0.84 (84%) as compare to Original Data's Precision Score which was 85%, it's very slightly less than the original ones however this 1% change won't make big difference therefore it must be considered as same without much change.

TPs as Healthy Loans (Value 0): Precision Score is 1.00 (100%) as compare to Original Data's Precision Score which was 100%, therefore no change in Precision Score for Healthy Loans.


**Recall Score:** 
We get the following Recall Score readings for Values: 1 & 0 after Resampling:

TPs as Healthy Loans (Value 0): Recall Score is 0.99 (99%) as compare to Original Data's Recall Score which was 99% too, therefore there's no change in Recall Score for Healthy Loans.

FNs as High-Risk Loans (Value 1): Recall Score is 0.99 (99%) as compare to Original Data's Recall Score which was 91%, this proves that how Imbalaced OverSampling can be useful. There's an 8% increase can be seen in confidence of this model after applying Resampling Techniques.


**F1 Score:** 
We get the following F1 Score readings for Values: 1 & 0 after Resampling:

High-Risk Loans (Value 1): F1 Score is 0.91 (91%) as compare to Original Data's F1 Score which was 88%, again proving that Imbalanced OverSampling Technique is quite useful in making more rational decisions. There's a 3% hike can be seen in confidence of this model after applying Resampling Techniques.

Healthy Loans (Value 0): F1 Score is 1.00 (100%) as compare to Original Data's F1 Score which was 100%, hence no change in confidence. It always been on seventh cloud when it comes to Healthy Loans, apparently Model loves Healthy Loan Data.

**Conclusion:** 

After applying Resampling Technique, we have seen some changes particularly for Smaller Class (High-Risk Loans) in case of:

Precision Score: Where Original Data's Precision Score was 85% and Resampled Data's Precision Score was 84%, which is quite same not much difference.

F1 Score: Where Original Data's F1 Score was 88% and Resampled Data's F1 Score was 91%, an increase in confidence level by 3% is quite impressive and shows that how Harmonic Mean value has been increased in total making the model efficacy more efficient and accurate.

Value 0 (Healthy Loans) remains pretty consistent in our findings and nothing major changed at confidence level and looks like all the readings regardless the Original or Resampled data, the nature is quite similar in both.


**Summary:**

After applying Resampling Technique, we have seen some changes particularly for Smaller Class (High-Risk Loans) in case of:

**Precision Score:** 
Where Original Data's Precision Score was 85% and Resampled Data's Precision Score was 84%, which is quite same not much difference.

**F1 Score:** 
Where Original Data's F1 Score was 88% and Resampled Data's F1 Score was 91%, an increase in confidence level by 3% is quite impressive and shows that how Harmonic Mean value has been increased in total making the model efficacy more efficient and accurate.

Value 0 (Healthy Loans) remains pretty consistent in our findings and nothing major changed at confidence level and looks like all the readings regardless the Original or Resampled data, the nature is quite similar in both.
