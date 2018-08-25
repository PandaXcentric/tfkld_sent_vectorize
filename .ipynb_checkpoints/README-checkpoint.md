# tfkld_sent_vectorize
Use tf-kld to vectorize sentences.  Use PCA to compress the vector to a reasonable size while maintaining accuracy. Utility functions to use the vector.


I used the code from this repo https://github.com/smujjiga/tfkld for tfkld.  I've included the tfkld file in this repository as well as the fe_quora file.
You can get the test and training datasets from here https://www.kaggle.com/c/quora-question-pairs


For the PCA Reduction you'll need a large text corpus. I used https://github.com/attardi/wikiextractor to get clean text from wikipedia articles.