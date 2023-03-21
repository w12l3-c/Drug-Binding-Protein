# Drug-Binding-Protein

<a target="_blank" href="https://colab.research.google.com/github/w12l3-c/Drug-Binding-Protein/blob/main/Protein_binding.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

A ML model build base on the dataset provided by AlphaFold about protein 3D structure to determine which part of the protein is able to bind to pharmaceutical drugs

In the Notebook, I have compared multiple models such as XGBoost, LightBGM and K-Nearest. Since this is an extremely unbalanced dataset, classifying the as much true positive is more important so false positive > false negative is preferred.

In this unbalanced datatse, there are multiple ways to solve this. After a lot of testing base on the accuracy report in sklearn (F1 score and Precision), using class weights is better than using Oversampling or Undersampling method like SMOTE, SVMSMOTE, and NearMiss. With a F1 score of positive class of 37% while negative class of 98%. The ROC is less important in the usage of class weights because the datatset is imbalanced.

After all the training and evaluation of model's performance. There is another datatset without labels and will let the model predict their compatibility with drug binding. 

Dataset:

https://drive.google.com/file/d/1H6oqtp9buAjO8NKQEW_jDzRd-4-qgQPF/view?usp=sharing

https://drive.google.com/file/d/1pr2_xiH7gEOnPtg8yqSevZDF_l0ak387/view?usp=sharing

