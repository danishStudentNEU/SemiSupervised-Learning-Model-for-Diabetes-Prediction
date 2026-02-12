# SemiSupervised-Learning-Model-for-Diabetes-Prediction

Challenge: How do we predict diabetes when we don’t have labeled data

Our Approach : Semi-supervised learning – generate labels using clustering, then train a supervised classifier 

Pipeline Summary:
Preprocess -> Clean and normalize the data
Cluster -> Use K- means to generate labels
Extract Features -> Reduce dimensions with PCA
Classify -> Train a Super Learner (Stacking ensemble)


Final Goal : Deploy the trained pipeline on a new dataset (Employee Leave) to test generalization


_____________________________________________________________________________________________________________________________________________________


What We Achieved:
✓ Built a complete semi-supervised learning pipeline
✓ Generated labels using K-Means clustering
✓ Reduced dimensions with PCA (65.6% variance retained)
✓ Trained a Super Learner with 86.96% accuracy
✓ Successfully deployed on new dataset (84.18% accuracy)

Key Insight:
The pipeline generalizes — same architecture worked on two completely different domains

Limitations:
Cluster-based labels are approximations, not ground truth
PCA retained only 65.6% of variance
Aggressive outlier removal (especially on Employee data)

Future Improvements:
Try different clustering methods (DBSCAN, Hierarchical)
Add more base classifiers (Random Forest, SVM)
