# README: data-analyst-bankchurners


## Subject: Predicting Credit Card Customer Segmentation

BankChurners =  les désabonnements bancaires

- Résumé : 
  - Cet ensemble de données contient une multitude d'informations sur les clients collectées à partir d'un portefeuille de cartes de crédit grand public, dans le but d'aider les analystes à prévoir l'attrition des clients. 
  - Il comprend des détails démographiques complets tels que l'âge, le sexe, l'état civil et la catégorie de revenu, ainsi qu'un aperçu de la relation de chaque client avec le fournisseur de carte de crédit, comme le type de carte, le nombre de mois sur le livre et les périodes inactives. 
   - En outre, il contient des données clés sur le comportement de dépenses des clients qui se rapprochent de leur décision de désabonnement, telles que le solde renouvelable total, la limite de crédit, le taux moyen d'ouverture à l'achat et des mesures analysables telles que le montant total de changement du trimestre 4 au trimestre 1. 
   - Problèmatique : Existe t'il des facteurs clés identifiables pouvant aider à prédire la fermeture ou la stabilité d'un compte?
   
lien des dataset:  
(https://www.kaggle.com/datasets/thedevastator/predicting-credit-card-customer-attrition-with-m)
Cet jeu de données fournit des informations sur les clients pour prédire l'attrition des clients pour un portefeuille de cartes de crédit grand public


Liens utile pour travailler:
(https://www.kaggle.com/code/selener/prediction-of-credit-card-default)

(https://www.centralbank.ie/statistics/data-and-analysis/credit-and-debit-card-statistics)

(https://www.centralbank.ie/docs/default-source/statistics/data-and-analysis/credit-and-banking-statistics/credit-and-debit-card-statistics/2022_dec_ie_credit_debit_cards.pdf?sfvrsn=bca9981d_3)

(https://www.analyticsvidhya.com/blog/2021/10/credit-card-lead-prediction-complete-project-using-lgbm-classification-model/)

(https://www.hindawi.com/journals/ddns/2021/5080472/)


## Définition des colonnes : 

   - ClientNum (Integer) : 
       - Unique identifier for each customer
   - Attrition_Flag (Boolean): 
       - Flag indicating whether or not the customer has churned out.
       - Indicateur indiquant si le client s'est retiré ou non
   - Customer_Age (Integer): 
       - Age of customer. 
   - Gender (String): 
       - Gender of customer. 
   - Dependent_count (Integer): 
       - Number of dependents that customer has.
       - Nombre de personnes à charge que le client a.
   - Education_Level (String): 
       - Education level of customer. 
   - Marital_Status (String): 
       - Marital status of customer. 
   - Income_Category(String): 
       - Income category of customer. 
   - Card_Category(String): 
       - Type of card held by customer.
   - Months_on_book (Integer): 
       - How long customer has been on the books. 
       - Durée d'enregistrement du client dans les registres
   - Total_Relationship_Count (Integer): 
       - Total number of relationships customer has with the credit card provider. 
       - Nombre total de relations entre le client et le fournisseur de carte de crédit
   - Months_Inactive_12_mon (Integer): 
       - Number of months customer has been inactive in the last twelve months 
       - Nombre de mois sur les douze derniers mois d'innactivités du client.
   - Contacts_Count_12_mon (Integer): 
       - Number of contacts customer has had in the last twelve months 
   - Credit_Limit (Integer): 
       - Credit limit of customer.
   - Total_Revolving_Bal (Integer): 
       - Total revolving balance of customer
       - Total du solde renouvelable du client
   - Avg_Open_To_Buy (Integer): 
       - Average open to buy ratio of customer 
       - taux moyen d'ouverture à l'achat du client, indique le ratio entre les publicités reçu par le client et ceux qu'ils consultent.
         
   - Total_Amt_Chng_Q4_Q1 (Integer): 
       - Total amount changed from quarter 4 to quarter 1 
       - Montant total modifié du trimestre 4 au trimestre 1
   - Total_Trans_Amt (Integer): 
       - Total transaction amount 
       - Montant total de la transaction
   - Total_Trans_Ct (Integer): 
       - Total transaction count
       - Nombre total de transactions
   - Total_Ct_Chng_Q4_Q1 (Integer): 
       - Total count changed from quarter 4 to quarter 1
       - Le décompte total a changé du trimestre 4 au trimestre 1
   - Avg_Utilization_Ratio (Integer): 
       - Average utilization ratio of customer 
       - Taux d'utilisation moyen du client
   Naive_Bayes_Classifier_Attrition_Flag_Card_Category_Contacts_Count_12_mon_Dependent_count_Education_Level_Months_Inactive_12_mon_1: Naive Bayes classifier for predicting whether or not someone will churn based on characteristics such
   
   Ci dessous le calssement des variables par types:
   
   
| N°  | Variables       | Définition      | Types   |  Quantitative?    |  Qualitative?|
| :------------- | :------------- |:-------------| :-----|:-------------| :-------------|
| 1 | **ClientNum**     | Identifiant unique du client | `Integer` | *Continue*| -
| 2 | **Attrition_Flag**      | Indicateur indiquant si le client s'est retiré ou non      |   `Boolean` |  *Discrete*| -
| 3 | **Customer_Age** | Age du client      |    `Integer` | *Discrete*| - 
| 4 | **Gender** | Genre du client      |    `String` | - | *nominal*| 
| 5 | **Dependent_count** | Nombre de personnes à charge que le client a      |  `Integer` | *Discrete*| - 
| 6 | **Education_Level** | Niveau d'étude du client      | `String` | - | *ordinale* |
| 7 | **Marital_Status** | Statut Marital du client   | `String` | - | *nominal* | 
| 8 | **Income_Category** | Catégorie de salaire du client    | `String` | - | *ordinale* | 
| 9 | **Card_Category** | type de carte détenu par le client      | `String` | - | *nominal* | 
| 10 | **Months_on_book** | Durée d'enregistrement du client dans les registres | `Integer` | *Discrete*| - 
| 11 | **Total_Relationship_Count** | Nombre total d'échange de message entre le client et le fournisseur de carte de crédit      |    `Integer` | *Continue*| - 
| 12 | **Months_Inactive_12_mon** | Nombre de mois sur les douze derniers mois d'innactivités du client      |    `Integer` | *Discrete* | - 
| 13 | **Contacts_Count_12_mon** | Nombres de contacts par la banque le client a eu durant les 12 derniers mois |    `Integer` | *Continue* | - 
| 13 | **Credit_Limit** | Limite de crédit du client      |    `Integer` | *Continue* | - 
| 14 | **Total_Revolving_Bal** | Total du solde renouvelable du client  | `Integer` | *Discrete*| - 
| 15 | **Avg_Open_To_Buy** | taux moyen d'ouverture à l'achat du client, indique le ratio entre les publicités reçu par le client et ceux qu'ils consultent | `Integer` | *Continue*| - 
| 16 | **Total_Amt_Chng_Q4_Q1** | Montant total modifié du trimestre 4 au trimestre 1 |    `Integer` | *Continue* | - 
| 17 | **Total_Trans_Amt** | Montant total de la transaction |    `Integer` | *Continue* | - 
| 18 | **Total_Trans_Ct** | Nombre total de transactions |    `Integer` | *Continue* | - 
| 19 | **Total_Ct_Chng_Q4_Q1** | Le décompte total a changé du trimestre 4 au trimestre 1      |    `Integer` | *Continue*| - 
| 20 | **Avg_Utilization_Ratio** | Taux d'utilisation moyen du client      |    `Integer` | *Continue*| - 



## Travaille à faire:

Votre projet de synthese s'organisera sous forme de Jupyter Notebook et devra contenir:

- Au moins 1 diagramme avec données continues, type nuage de point ou histogramme
- Au moins 2 diagrammes avec des données discrètes
- Au moins 3 graphiques avec des données catégoriques
- 1 boîte à moustaches avec filtrage des données aberrantes sur le dataset (si il y en a)
- 1 heat map avec matrice de corrélation (si pertinent)
- Des commentaires clairs et pertinents pour chaque graphiques

une conclusion qui vise a répondre (ou non) à votre problematique

