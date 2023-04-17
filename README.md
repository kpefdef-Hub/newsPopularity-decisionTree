# newsPopularity-decisionTree

Used SAS Miner to use  Decision Tree to review data content (containing 26,000 observations of newsShared) collected from a Digital Consulting firm to identify the important factors that influence the probability that content will be shared.

Explained the output of the decision tree to the management and make recommendations to the management on how to create content that are more likely to be shared.

Computed the Gini split criteria for the first split from the root node.

Performed a logistic regression with the same data set.

Compared the decision tree and logistic regression models using the confusion matrix from
the test data using the following metrics (5 points)
  a. Accuracy
  b. Precision
  c. Recall

Recommended the best model for Design Associates based on my comparison of the models


ANALYSIS

![image](https://user-images.githubusercontent.com/114897374/232611107-2c1d5f73-8316-4fbf-a2b5-204f6ccfeb2b.png)


![image](https://user-images.githubusercontent.com/114897374/232611140-243d73f2-741f-40fd-9201-409d63784afc.png)


Identifying the Important Factors
Based on the output of the Decision tree, the following are important factors that influence the probability that the content will be shared:
•	Relevancy of the Content to the reader (Relevancy) 
•	The quality of the Images on the content (ImageLevel)
•	The time of the week when the content is read (isWeekend)
•	The quality of the Videos in the content (Videos) 
•	The length of the title of the content (titleCount)
•	The time it takes to read the content(readTime)

B- Explaining the Output of the Decision Tree
The output of the decision tree shows that most important factor that determines if the content would be shared is the Relevancy of the content to the Reader.
If the content is Relevant to the reader, it has a high chance of being shared regardless of whether the Images on the content are of a High, Low or Blurred quality.
However, if the content is not relevant the Reader is still likely to share the content If the Image level of the content is High or Low. Irrelevant content with blurred images are less likely to be shared by the readers.
Also, if the content is read on a Weekday, it has a higher chance of being shared than content read on a Weekend.

Recommendations for Digital Designs Inc.
Based on these results of the Decision Tree, Digital Designs should do the following when designing content:
•	Focus on identifying the needs and interests of their audience and creating relevant content that meet those needs and interests
•	Enhance the quality and visual appeal of the images used in their content
•	Time the promotion of their content to weekdays rather than weekends so the audience have a higher chance of reading it during the weekdays

C - Most Important Factors
Based on the output, the most important factors in determining if a content will be shared are:
•	Relevancy:
o	The relevancy of the Content to the reader has an importance score of 1.000 which indicates that it is the most important feature with the highest impact on determining if the content will be shared or not
•	ImageLevel: 
o	The quality of the Images on the content has an importance score of 0.7309 which indicates that it is the second most important feature in determining if the content will be shared or not
•	isWeekend:
o	The time of the week when the content is read has an importance score o 0.4082 which indicates that it has a significant impact on if the reader will share the content or not

D – Gini Split Criteria
Gini split is a method for splitting the nodes when the target variable is categorical in a decision tree. The Gini split criteria quantifies the degree of heterogeneity or unpredictability of the target variable's classes within a particular split. The Gini Impurity value is calculated for each split and the split with the lowest value of Gini Impurity is selected.
Computing the Gini split for the first split from the root node.
Gini Split Formula:
Gini (p) = 1 - ∑p^2
	= 1 – [(P+) ^2 + (P-)^2]
Left Split (No, Maybe)
	= 1 – [(0.4488) ^2 + (0.5512) ^2]
	= 1 – [0.201421 + 0.303821]
	= 1 - 0.505242
	= 0.494758
Right Split (Yes or Missing)
	= 1 – [(0.0658) ^2 + (0.9342) ^2]
	= 1 – [0.00433 + 0.87273]
	= 1 - 0.87706
	= 0.12294
This Gini Split result implies that the Left Split (No, Maybe) is less pure than the Right Split (Yes or Missing), as indicated by the higher Gini index value of the Left Split.
In this case, the Gini index value of the Left Split (No, Maybe)  is 0.494758, which is closer to 0.5 than 0, indicating that the samples in this subset are less pure and more mixed than the samples in the Right Split (Yes or Missing). 
The Gini index value of the Right Split is 0.12294, which is closer to 0 than 0.5, suggesting that the samples in this subset are more pure and easier to classify.
Overall, this Gini Split result suggests that the Right Split (Yes or Missing) is a better split for this node in the decision tree, as it creates more homogeneous subsets of samples that are easier to classify.




E – Logistic Regression

![image](https://user-images.githubusercontent.com/114897374/232611203-11e9832d-dabd-4950-811d-8b94a6069b85.png)


E(a) - Comparing the decision tree and Logistic Regression models

![image](https://user-images.githubusercontent.com/114897374/232611269-7d5952bd-34b7-402a-ac0e-e37574253519.png)





Accuracy
(TP+TN/(TP+TN+FP+FN)	
Logistic Regression Model	
=  (985+5707)/(985+5707+397+934)
=  0.8341	

Decision Tree Model 
=   (959+5702)/(959+5702+402+960)
=   0.8302

Precision
TP/(TP+FP)	

Logistic Regression
=    985/ (985+397)
=    0.7127	

Decision Tree
=     959/ (959+402)
=     0.7046


Recall
TP/(TP+FN)	

Logistic Regression
=    985/(985+934)
=    0.5133	

Decision Tree
=     959/(95+960)
=     0.4997

E(b) - Recommendation

a.	Based on the comparison of the 2 models in Table above, the best model for Digital Designs Inc is the Logistic Regression model because:
i.	it has the higher Accuracy at 83.41% against the Decision Tree’s 83.02%
ii.	it has a higher Precision at 71.27% against the Decision Tree’s 70.46%

  
