# Data Mining and Machine Learning - Project
### Detecting Difficulty Level of French Texts
This project aims to build a model that can predict the difficulty level of a French text for English speakers. The difficulty level is based on the Common European Framework of Reference for Languages (CEFR) scale, which ranges from A1 to C2. The goal is to use this model in a recommendation system to suggest texts that are appropriate for a given language level. For example, if someone is at an A1 French level, it would not be helpful to recommend a text at a B2 level, as it would likely be too difficult for them to understand. On the other hand, a text that is slightly above their current level and contains some unknown words can help them improve their language skills. 

## Getting Started

## Approach
The model will be trained on a dataset of French texts with their corresponding difficulty levels, and it will use this data to predict the difficulty level of new texts. By accurately predicting the difficulty level of French texts, the recommendation system can help English speakers improve their French skills by providing texts that are appropriate for their current language level.

[MONTRER TEXT ENTRAINEMENT A DISPOSITION + 1 PHRASE DE BLABLA]

[AJOUT PHRASE POUR FAIRE LE POND ENTRE LES DONNEES ET LES MODELES EN DESSOUS]


💎 Here are the different models used:. Set the `random_state=0`.
- baseline
- logistic regression with TFidf vectoriser (simple, no data cleaning)
- KNN & hyperparameter optimisation (simple, no data cleaning)
- Decision Tree classifier & hyperparameter optimisation (simple, no data cleaning)
- Random Forests classifier (simple, no data cleaning)
- another technique or combination of techniques of your choice

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
* Bsc in Industrial Engineering and Management, Major in Supply Chain Management  
* MSc in Information Systems and Digital Innovation at HEC Lausanne  

[Vincent Nieto](https://www.linkedin.com/in/vincent-nieto-4bb207214/)  
* Bsc in Industrial Engineering and Management, Major in Supply Chain Management
* MSc in Information Systems and Digital Innovation at HEC Lausanne







## Acknowledgments

Inspiration, code snippets, etc.
* [awesome-readme](https://github.com/matiassingers/awesome-readme)
