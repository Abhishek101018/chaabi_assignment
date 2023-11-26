# chaabi_assignment
1.Import necessary libraries such as pandas, numpy, torch, faiss, and transformers.<br>
2.Specify the path to your CSV file.Use pandas to read the CSV file and load it into a DataFrame (df).<br>
3.Load Pre-trained Language Model and Tokenizer(like BertTokenizer, BertModel in our case).<br>
4.Define a function ('encode_text') to tokenize and encode text using the pre-trained language model.Apply this function to each text column in the DataFrame, creating embeddings for each.<br>
5. Use StandardScaler from scikit-learn to normalize the text embeddings for each text column.<br>
6. Determine the dimensionality (d) of the embeddings.Create a Faiss index (IndexFlatL2) and add the combined embeddings to the index.<br>
7.Define a function ('query_llm') that takes a query text and performs the following steps:<br>
(a). Encode the query text using the same encode_text function.<br>
(b). Normalize the query text embedding.<br>
(c)Use Faiss index to perform a similarity search and retrieve the indices of nearest neighbors.<br>
8. Perform a sample query using the query_llm function, providing a query text .<br>
9.Print the results of the query, such description by the nearest neighbour.<br>
