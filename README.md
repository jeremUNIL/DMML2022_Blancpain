# Data Mining and Machine Learning - Project
### Detecting Difficulty Level of French Texts
This project aims to build a model that can predict the difficulty level of a French text for English speakers. The difficulty level is based on the Common European Framework of Reference for Languages (CEFR) scale, which ranges from A1 to C2. The goal is to use this model in a recommendation system to suggest texts that are appropriate for a given language level. For example, if someone is at an A1 French level, it would not be helpful to recommend a text at a B2 level, as it would likely be too difficult for them to understand. On the other hand, a text that is slightly above their current level and contains some unknown words can help them improve their language skills. 

The aim of this classifier can be to enable a recommendation system to choose sentences suitable for a user's language proficiency or to enable a language assessment tool. It may also be utilized to generate databases of sentences of varying difficulty levels for language learning or for creating language exams.

## Approach
The model will be trained on a [dataset](https://github.com/jeremUNIL/DMML2022_Blancpain/blob/main/data/training_data.csv) of French texts with their corresponding difficulty levels, and it will use this data to predict the difficulty level of new texts. Below is a sample of the training data: 

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

 

## Summary of results table

|| Logistic Regression | Knn | Decision Tree | Random Forests | Any Other Techniques |
| --- | --- | --- | --- | --- | --- |
| Precision | 0.4645 | 0.4154 | 0.3267 | 0.4645 | 0.4334 |
| Recall | 0.4677 | 0.3600 | 0.3244 | 0.4645 | 0.4212 |
| F1-Score | 0.4640 | 0.3489 | 0.3085 | 0.4645 | 0.4092 |
| Accuracy | 0.4667| 0.3594 | 0.3208 | 0.4645 | 0.4188 |




## Video link



[![OpenAI Logo](https://user-images.githubusercontent.com/114933881/208678981-31945b49-81c4-4d0b-9041-d658687ab0ce.png)](https://www.youtube.com/watch?v=PTvTLvkiAbI)



## Authors
Jérémy Jungo  
* Bsc in Industrial Engineering and Management - Major in Supply Chain Management  
* MSc in Information Systems and Digital Innovation at HEC Lausanne  

[Vincent Nieto](https://www.linkedin.com/in/vincent-nieto-4bb207214/)  
* Bsc in Industrial Engineering and Management - Major in Supply Chain Management
* MSc in Information Systems and Digital Innovation at HEC Lausanne







## Acknowledgments

Inspiration, code snippets, etc.
* [Hugging Face](https://huggingface.co/models?sort=downloads&search=flaubert)
