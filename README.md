# MSCS_634_Lab_2

# Lab Assignment 2: Classification Using KNN and RNN Algorithms

*Author*: Murali Krishna Chintha  
*Course*: MSCS-634-M40 - Advanced Big Data and Data Mining  

## 📌 Purpose
The goal of this lab is to apply two supervised machine learning algorithms—K-Nearest Neighbors (KNN) and Radius Neighbors (RNN)—on the Wine dataset from ⁠ sklearn ⁠. This assignment demonstrates how different values of ⁠ k ⁠ and ⁠ radius ⁠ affect classification accuracy, and helps understand the practical differences between these two neighbor-based methods.

## 📊 Key Insights
•⁠  ⁠*KNN*:
  - Accuracy improved from ⁠ k=1 ⁠ to ⁠ k=11 ⁠ but started to drop slightly beyond that.
  - A moderate value of ⁠ k=5 ⁠ or ⁠ k=11 ⁠ yielded the best balance between bias and variance.

•⁠  ⁠*RNN*:
  - Performance was highly sensitive to the radius value.
  - Too small a radius led to poor coverage (some test samples had no neighbors and were not classified).
  - Mid-range values like ⁠ radius=450 ⁠ gave better and more stable results.

•⁠  ⁠*Comparison*:
  - KNN consistently classified all test samples, making it more reliable for smaller datasets.
  - RNN showed potential but required careful tuning of the radius and could result in unclassified samples.

## ⚙️ Challenges and Decisions
•⁠  ⁠RNN's performance depended heavily on the selected radius. Initially, many predictions returned ⁠ -1 ⁠ (unclassified), so we added logic to filter these out during evaluation.
•⁠  ⁠Selecting appropriate values for ⁠ k ⁠ and ⁠ radius ⁠ required iterative testing. We chose commonly used benchmark values for demonstration.
•⁠  ⁠The wine dataset’s small size made it ideal for quick experimentation but also required careful handling to avoid overfitting.
