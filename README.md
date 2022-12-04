# Model_Interpretability_DT_XGBoost_AutoML


1. Fit a linear model and interpret the regression ?
      Answer. When the variable "species" is increased, there is increase in culmen_length_mm by more than 4x (i.e. 4.213). In contrast, as "body_mass_g" concentration rises, there is increase in culmen_length_mm by only 0.83 .


2. Fit a tree-based model and interpret the nodes ?
Answer. The XGBoost algorithm was used to plot the first tree, which is shown in the plot. This plot interprets all nodes (root, leaf, and intermediate). The model's final judgments and the number of splits required to get there are shown in this figure. The root node in the plot shown is "SPECIES." the tree diagrams of the first three trees' node interpretability is shown in tree section.



3. Use auto ml to find the best model ?
      Answer. Pycaret is Used to perform MultiClass classification and best model is selcted by the compare_model() method.


4. Run SHAP analysis on the models from steps 1, 2, and 3, interpret the SHAP values and compare them with the other model interpretability methods?
      Answer:After running SHAP analysis on model 1 (i.e. Linear Regression), we have found that 'species' is the top feature in the dataset impacting the model’s output as represented in the beeswarm and summary plots whereas 'body_mass_g' is the least important feature. According to beeswarm plot, higher value of 'species' (2) leads higher culmen length. Lower value of 'species' leads to lower culmen length. Similarly, culmen depth , sex, island and flipper length have positive impact on model output.
model 2 (i.e. XGBoost) 'culmen_length_mm' and 'sex' are the most and least significant features respectively contributing towards prediction of species. According to summary plot, higher value of 'culmen_length_mm' leads to proper classification of species. 'sex' does not contribute to prediction.
model 3 by referring the above shap summary plot, 'flipper_legth_mm' is the most important and dominant feature in the model to predict target variable. Where as, 'culmen_depth_mm' is less important.the model does feature selection while creation so on 3 coloumns are used which are dominant 'flipper_length_mm' being the most dominant among them.
