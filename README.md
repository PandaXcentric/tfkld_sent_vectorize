# tfkld_sent_vectorize
Use tf-kld to vectorize sentences.  Use PCA to compress the vector to a reasonable size while maintaining accuracy. Utility functions to use the vector.


I used the code from this repo https://github.com/smujjiga/tfkld for tfkld.  I've included the tfkld file in this repository as well as the fe_quora file.
You can get the test and training datasets from here https://www.kaggle.com/c/quora-question-pairs


For the PCA Reduction you'll need a large text corpus. I used https://github.com/attardi/wikiextractor to get clean text from wikipedia articles.

# Utility Functions Explained
I've writtend some utility functions that allow you to use the sentence vectors in the same way you would use word2vec, so I've made a get_similar call.  I've also made a call that allows you to create the sentence vectors and grow the size of it.  All of the functions are documented in the notebook, but a quick list of them are

1. vectorize_document_list(documents, sentence_dict={}) -  This will take a list of text and convert it into a sentence vector
2. increase_sentence_vector(sentences, sentence_dict={}) - Takes a list of sentences and adds them to the sentence dictionary
3. mean_sentences_vector(sentences) - Creates a vector that is the mean of the vectors of all of the passed sentences
4. get_most_similar_sentences(sentence_dict, sentence, tnum=5) -  Get the sentences whose cosine similarity is closest to the passed sentence
5. get_most_similar_sentences_to_vector(sentence_dict, mean_vector, tnum=5) - Gets the sentences that are closest to the passed vector.

I've also made some utility functions if you decide to use tfidf instead of tfkld to vectorize your sentences.

# How to use
You'll need to run the notebooks in this order, the pca depends on the tfkld, and once both are done you can use the utility functions.

1. Run the train_tfkld notebook.
2. Run the pca_reduction_tfkld notebook.

You can now use the utility functions!
