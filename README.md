# Cancer-Diagnosis
Data Overview:
Source: https://www.kaggle.com/c/msk-redefining-cancer-treatment/data
We have two data files: one conatins the information about the genetic mutations and the other contains the clinical evidence (text) that human experts/pathologists use to classify the genetic mutations.
Both these data files are have a common column called ID
Data file's information:

training_variants (ID , Gene, Variations, Class)
training_text (ID, Text)

ID : the id of the row used to link the mutation to the clinical evidence
Gene : the gene where this genetic mutation is located
Variation : the aminoacid change for this mutations
Class : 1-9 the class this genetic mutation has been classified on

Problem statement : 
Classify the given genetic variations/mutations based on evidence from text-based clinical literature.


Featuraization:
Two ways to featurize Categorical Data : 1) One hot encoding 2) Responce Encoding
For text feature : Instread of Word2Vec we use Countvectorizer(BOW)

Moodels:
 Tried different models among them following works best.
 1) Logistic Regression with onne hot encoding + balancing
 2) Voting (Logistic regression, SVM, RF) (but intrepretability is lost in this)
