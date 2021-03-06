# Project_3
CS 504 Project 3
## Methodology
	1. Data Preprocessing
		a. Convert dataframe into numpy arrays
		b. Split Train/Test data at 75%/25%
		c. Trial 1
			i. Deal with missing values
			ii. Deal with garbage values
			iii. Run without any preprocessing
		d. Trial 2
			i. Check for outliers (Remove extreme values)
		e. Trial 3
			i. Scale the data (Maybe normalize or standardize it)
			ii. Use some sort of feature selection
	2. Analysis Techniques
		a. Decision Tree
			i. Simple Tree
				1) Split Train/Test data at 75%/25%
				2) Use tree.DecisionTreeClassifier to train model
				3) Use score on test model to calculate accuracy
				4) No need to visualize tree
			ii. Perform 10-Fold Cross Validation
				1) use model_selection.cross_val_score and mean to calculate mean accuracy
				2) Find accuracy of best tree model
		b. Random Forest
			i. Simple forest
				1) Use ensemble.RandomForestClassifier with n_estimators=10 to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
			ii. Compare with Decision Tree
		c. KNN
			i. Simple K=10
				1) Use neighbors.KNeighborsClassifier with n_neighbors=10 to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
			ii. for loop with K ranging from 1 to 50
				1) Use neighbors.KNeighborsClassifier to train model
				2) Perform 10-Fold Cross Validation
				3) Compare with Accuracy with K values
			iii. Compare best K accuracy with Decision Tree and Random Forest
		d. Naïve Bayes
			i. MultinomialNB
				1) Use naive_bayes.MultinomailNB to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
			ii. GaussianNB
				1) Use naive_bayes.GaussianNB to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
				3) Compare with MultinomialNB
			iii. Compare with KNN, Random Forest and Decision Tree
		e. SVM (extra credit)
			i. Simple Model
				1) Use svm.SVC to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
			ii. for loop to run svm with linear, sigmoid, and poly kernels
				1) Use svm.SVC to train model
				2) Perform 10-Fold Cross Validation and find mean accuracy
				3) Compare kernel accuracies
			iii. Compare with Naïve Bayes, KNN, Random Forest and Decision Tree
		f. Create a dataframe to store accuracies for each model and visualize.
			- Decision Tree
			- Decision Tree 10-CV
			- Random Forest
			- Random Forest 10-CV
			- Extreme Random Forest 10-CV
			- KNN 10-CV
			- KNN (0-50) 10-CV
			- MNB 10-CV
			- GNM 10-CV
			- SVM RBF 10-CV
			- SVM linear 10-CV
			- SVM sigmoid 10-CV
			- SVM poly 10-CV
		
