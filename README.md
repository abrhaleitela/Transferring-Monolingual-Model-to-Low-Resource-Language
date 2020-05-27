# Transferring Monolingual Model to Low-Resource Language: The Case Of Tigrinya:


Documenation is coming soon with full code!

## Proposed Method:
<img src="data/dim-reduction.png" height = "230" width ="460" >




## Main files:
 - Train.ipynb : Fine-tunes XLNet (mono-lingual transformer) on new target language (Tigrinya)
 - Test.ipynb : Evaluates the fine-tuned model on test data 
 - Word2Vec_token_embeddings_for_xlnet.ipynb : Trains a word2vec token embeddings for Tigrinya language to be used for XLNet embeddings
 - Text_processing_for_language_identification.ipynb : Extracts Tigrinya comments from mixed language contents
 - YouTube_comment_downloader.ipynb : Download all avaialble comments from a YouTube channel (Channel ID as input)
 - auto_labelling.ipynb : Automatically labels Tigrinya comments in to positive or negative sentiments 
 
 All files are IPython Notebook files which can be run simply in Google Colab
 ## 
 
