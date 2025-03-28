**Toxic Comment Classification**

**Project Overview**

This project involves building two machine learning models to classify whether a given social media comment is toxic or not. The classification was performed using:
	•	Fine-tuned BERT model
	•	Support Vector Machine (SVM)

The models were trained on a dataset containing 4,000 comments collected from Reddit, Twitter/X, and YouTube.

**Datasets**

**Training Dataset (z639_training.json)**

The training dataset consists of social media comments annotated for toxicity. Each entry in the dataset includes:
	•	text: The comment text to be classified.
	•	parent_comment: The comment this text is replying to (null if it has no parent).
	•	article_title: The news article associated with the comment.
	•	article_url: URL of the news article.
	•	platform: The social media platform where the comment was posted (Reddit, Twitter/X, or YouTube).
	•	platform_id: The unique identifier of the comment on the platform.
	•	composite_toxic: A list of five human annotations indicating whether the comment is toxic (true) or not (false).

**Test Dataset (z639_test.json)**

The test dataset has the same structure as the training dataset except for the composite_toxic field, which is not provided. The trained models predict whether each comment is toxic or not.

**Models Used**
	1.	Fine-tuned BERT
	•	Utilized a pre-trained BERT (Bidirectional Encoder Representations from Transformers) model.
	•	Fine-tuned on the dataset to capture contextual understanding of toxicity in comments.
	2.	Support Vector Machine (SVM)
	•	Used TF-IDF (Term Frequency-Inverse Document Frequency) vectorization for text feature extraction.
	•	Trained an SVM classifier to identify toxic comments based on extracted features.

Evaluation 
	•	Model evaluation: The models were assessed based on accuracy, precision, recall, and F1-score.
	•	A CSV file containing predictions (platform_id, prediction) was saved.
    
