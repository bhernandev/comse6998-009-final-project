# Benchmarking the Wide & Deep and Deep & Cross models for recommendation systems
**Brian Hernandez (bmh2168) | Emad Dehkordy (em3578)**  
**COMSE6998 009 Final Project**

### Overview

In this project we aim to benchmark and compare two similar models to recommendation systems, the Wide & Deep model and the Deep & Cross model. Both of these approaches involve the combination of a DNN component and a component to capture feature interactions. To benchmark these models, we tested their performance on the MovieLens - Small dataset. This dataset is comprised of movie ratings by users in addition to various features pertaining to the user's background. With this dataset and through various experiments we hoped to shed light on some of the tradeoffs and overall performance of these models.

In this repository we have two notebook files. Each should be able to run end to end without any issues -- one can upload the notebook to any Jupyter Notebook server or to Google Colab and can simply use the Run All command from there to reproduce our results.

*Original Hardware Used: K80 GPU*

### Project Structure
* README.md
* Recommendation_experiments.ipynb
  * Notebook file containing all of the experiments we performed as a part of our project -- results summarized below
* Recommendation_demo.ipynb 
  * Notebook file containing the code for our project demo

### Results & Observations

**Model Complexity:**
![image](https://user-images.githubusercontent.com/11566480/167333277-6d556095-f12b-4a31-b155-c0f3289a7935.png)

There is an inflection point with respect to Total Units included in the DNN component of both models whereby the Deep & Cross model begins to outperform the Wide & Deep model as it has more Total Units to work with. With respect to the depth of the DNN component, there doesn't seem to be any improvements at all as we increase the depth. This might be an artifact of the dataset itself which was a smaller representative version of that provided by Movielens (~100k records). These results might be indicative of future experiments and research to be done to fully conclude / confirm.


**Overall Performance:**
![image](https://user-images.githubusercontent.com/11566480/167333572-dafb0fc6-3c18-4bd3-9262-92e0553d02df.png)

Overall, the Wide and Deep model seems to outperform the Deep & Cross model with respect to RMSE, however the Wide and Deep model seems to take longer to train. As one might expect this suggests a tradeoff between performance and training time.

**Sources:** 
- https://www.tensorflow.org/tutorials/load_data/pandas_dataframe
- https://www.tensorflow.org/recommenders/examples/dcn 
- https://keras.io/examples/structured_data/wide_deep_cross_networks/ 
