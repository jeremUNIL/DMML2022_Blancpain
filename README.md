# Data Mining and Machine Learning - Project
### Detecting Difficulty Level of French Texts
This project aims to build a model that can predict the difficulty level of a French text for English speakers. The difficulty level is based on the Common European Framework of Reference for Languages (CEFR) scale, which ranges from A1 to C2. The goal is to use this model in a recommendation system to suggest texts that are appropriate for a given language level. For example, if someone is at an A1 French level, it would not be helpful to recommend a text at a B2 level, as it would likely be too difficult for them to understand. On the other hand, a text that is slightly above their current level and contains some unknown words can help them improve their language skills. 

The aim of this classifier can be to enable a recommendation system to choose sentences suitable for a user's language proficiency or to enable a language assessment tool. It may also be utilized to generate databases of sentences of varying difficulty levels for language learning or for creating language exams.

## Approach
The model will be trained on a [dataset](https://github.com/jeremUNIL/DMML2022_Blancpain/blob/main/data/training_data.csv) of French texts with their corresponding difficulty levels, and it will use this data to predict the difficulty level of [new sentences](https://github.com/jeremUNIL/DMML2022_Blancpain/blob/main/data/unlabelled_test_data.csv). Below is a sample of the training data: 


| ID | sentence | difficulty |
| --- | --- | --- |
| 1 | Tu mangeas les petits fruits dès que tu les eus cueillis. | C2 |
| 2 | Voilà une autre histoire que j'ai beaucoup aimée. | A2 |
| 3 | Bonjour et bonne année. | A1 |
| 4 | Ces tanières se fondent dans la nature pour être quasiment invisibles. | C1 |
| 5 | Vous ferez de la randonnée ? | B1 |
| 6 | Ce phénomène, c'est l'apparition d'une génération inédite. | B2 |


In order to categorize the difficulty of texts within the project, we utilized sentence vectorization techniques, such as TF-IDF, to train basic multiclass classification models, such as :
* Logistic Regression 
* KNN & Hyperparameter Optimisation 
* Decision Tree Classifier & Hyperparameter Optimisation 
* Random Forests Classifier 

Once the previous models have been trained, we will try to increase the prediction accuracy by using other techniques. The results obtained are summarised in the table below. A video presenting all the solutions is also available under the "Video link" section.
 
 The additional models used are as follows: 
 The Multinomial Naive Bayes model is a binary classification model commonly used in classification tasks. It uses a "naive" approach by assuming that all independent variables are independent of each other, which can simplify the modelling process. However, this assumption may not always be true in reality, which may result in a lower performance of this model compared to other classification models.

Translated with www.DeepL.com/Translator (free version)

## Summary of results table

|| Logistic Regression | Knn | Decision Tree | Random Forests | Multinomial | FlauBERT & Log. reg. |
| --- | --- | --- | --- | --- | --- | --- |
| Accuracy | 0.4667| 0.3594 | 0.3156 | 0.4031 | 0.4823 | 0.4292 |
| Precision | 0.4645 | 0.4163 | 0.3194 | 0.4048 | 0.5014 | 0.4338 |
| Recall | 0.4677 | 0.3600 | 0.3198 | 0.4059 | 0.4839 | 0.4273 |
| F1-Score | 0.4640 | 0.3488 | 0.3011 | 0.3884 | 0.4795 | 0.4317 |

The best performing model was the multinomial model, followed closely by the logistic regression model. These models were found to be the best performing models for this type of work.

The use of the pre-treatment model with logistic regression did not achieve the desired results. As mentioned in the video, some parameters had to be minimised to avoid RAM problems during the execution of the code.

Indeed, the choice and optimisation of hyperparameters can have a significant impact on the performance of machine learning models, as can the quality and quantity of the data used for training.

Batch size and maximum sequence length (max_seq_length) can impact on model performance in several ways:
1.	Batch size can influence the learning speed of the model and the quality of its predictions. In general, a larger batch size can speed up the learning of the model, but can also lead to overlearning if it is too large. On the other hand, a smaller batch size may result in slower learning but can help prevent overfitting.
2.	The maximum sequence length can affect the amount of context the model can take into account when making predictions. If the maximum sequence length is too small, the model may not have enough context to make accurate predictions and may therefore perform worse. On the other hand, if the maximum sequence length is too large, the model may have difficulty processing the sequences and extracting relevant features, which may also negatively affect its performance.

It is therefore important to find a good balance between batch size and maximum sequence length to achieve optimal model performance. This may require manual adjustment of hyperparameters and trial and error to find the values that best suit the data and the model used


## Video link



[![OpenAI Logo](https://www.youtube.com/watch?v=PTvTLvkiAbI&t=131s)]



## Authors
Jérémy Jungo  
* Bsc in Industrial Engineering and Management - Major in Supply Chain Management  
* MSc in Information Systems and Digital Innovation at HEC Lausanne  

[Vincent Nieto](https://www.linkedin.com/in/vincent-nieto-4bb207214/)  
* Bsc in Industrial Engineering and Management - Major in Supply Chain Management
* MSc in Information Systems and Digital Innovation at HEC Lausanne







## Acknowledgments

Inspiration, code snippets, etc.
* [Hugging Face doc](https://huggingface.co/models?sort=downloads&search=flaubert)
* [Multinomial NB doc](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)
