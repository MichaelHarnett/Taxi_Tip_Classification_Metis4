# Metis Classification Module
<hr>
This repository was created as a project for metis, to learn different classification models and their appropriate metrics. I chose to use public data available on NYC.gov to try and predict if a taxi ride will result in a tip or not
<br><br>
# Description of Jupyter Notebooks
<hr></hr>
This is a working notebook, and has not been fully cleaned and organized. Some files have been moved into different folders, so file paths for calling different csv's may not represent their current path. The data used for this project in particular was very large, so CSV files were added to my .gitignore file. The files will be listed in order of creation, to illustrate workflow.
<br>
<b>prelim</b> - This notebook was the first notebook I downloaded the data with, performed preliminary EDA and basline modeling for just yellow cars<br>
<b>green_eda</b> - Using prelim as a launching pad I downloaded and cleaned the green taxi information in this notebook, and organized it with headers<br>
<b>yellow_eda2</b> - I then re-cleaned the yellow cab informaion, following the same format as green_eda for uniformity<br>
<b>merging_modeling1</b> - I used this notebook to concatenate the two dataframes, and dive into hyperperameters for the baseline logistic regression I was working with. <br>
<b>Trees</b> - I used this notebook to baseline decision trees and random forest regressions, on an early version of my dataframe<br>
<b>Trees-Copy1</b> - Ran through the notebook again with my concatenated dataframe
<b>XGB</b> - This notebook took the final dataframe and started testing extreme gradient boost models
<br><br><br><br><br><br>
# Abstract<hr></hr>
New York City being one of the worlds most populated cities. Taxi cabs pull in over $100 million in revenue every month. Naturally, this makes the market very competitive. Drivers need every advantage they can to increase their profits. The purpose of this project, was to predict which rides are more likely to result in a tip, helping drivers maximize their earnings. <br>

# Data
<hr></hr>
Originally I hoped to use a full year of data for this projcet, but I underestimated how large and challenging the data was. Yellow cars alone for the 2019 calendar year had 83 million observations. The data set was bout 9GB. For Hire vehicles (such as Uber) also had to be removed from the classification. While they do have data online, they do not report on the features I used to build my model. For these reasons, I built a model using just yellow and green taxi data from January of 2019. When  trying to one-hot-encode all categorical features, the dataset had 5.9 million observations and 606 features. This caused both kernal crashes and computer crashes, so zone features were removed(specific regions like Astoria or Midtown). After this edit, features dropped to 86.<br>
