# Transferring Monolingual Model to Low-Resource Language: The Case Of Tigrinya:


Documenation is coming soon with full code!

## Proposed Method:
<img src="data/proposed.png" height = "330" width ="760" >

The proposed method transfers a mono-lingual Transformer model into new target language at lexical level by learning new token embeddings. All implementation in this repo uses XLNet as a source Transformer model, however, other Transformer models can also be used similarly. 


## Main files:
 - Train.ipynb : Fine-tunes XLNet (mono-lingual transformer) on new target language (Tigrinya)
 - Test.ipynb : Evaluates the fine-tuned model on test data 
 - Word2Vec_token_embeddings_for_xlnet.ipynb : Trains a word2vec token embeddings for Tigrinya language to be used for XLNet embeddings
 - Text_processing_for_language_identification.ipynb : Extracts Tigrinya comments from mixed language contents
 - YouTube_comment_downloader.ipynb : Download all avaialble comments from a YouTube channel (Channel ID as input)
 - auto_labelling.ipynb : Automatically labels Tigrinya comments in to positive or negative sentiments based on [Emoji's sentiment](http://kt.ijs.si/data/Emoji_sentiment_ranking/)  
 
 All files are IPython Notebook files which can be excuted simply in Google Colab
 
 ## Evaluation
 
 The proposed method is evaluated using two datasets:
  - A newly created sentiment analysis dataset for low-resorce language (Tigriyna) 
   
  <table>
    <thead>
        <tr>
            <th><sub>Models</sub></th>
            <th><sub>Configuration</sub></th>
            <th><sub>F1-Score</sub></th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=3><sub>BERT</sub></td>
            <td rowspan=1><sub>+Frozen BERT weights</sub></td>
            <td><sub>54.91</sub></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Random embeddings</sub></td>
            <td><sub>74.26</sub></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Frozen token embeddings</sub></td>
            <td><sub>76.35</sub></td>
        </tr>     
        <tr>
            <td rowspan=3><sub>mBERT</sub></td>
            <td rowspan=1><sub>+Frozen mBERT weights</sub></td>
            <td><sub>57.32</sub></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Random embeddings</sub></td>
            <td><sub>76.01</sub></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Frozen token embeddings</sub></td>
            <td><sub>77.51</sub></td>
        </tr>        
        <tr>
            <td rowspan=3><sub>XLNet</sub></td>
            <td rowspan=1><sub>+Frozen XLNet weights</sub></td>
            <td><strong><sub>68.14</sub></strong></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Random embeddings</sub></td>
            <td><strong><sub>77.83</sub></strong></td>
        </tr>
        <tr>
            <td rowspan=1><sub>+Frozen token embeddings</sub></td>
            <td><strong><sub>81.62</sub></strong></td>
        </tr>
    </tbody>
</table>
        
  - Cross-lingual Sentiment dataset ([CLS](https://zenodo.org/record/3251672#.Xs65VzozbIU))
  
 
