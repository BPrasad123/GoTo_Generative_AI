


## Quantization:
It is a crucial technique for several reasons, especially in the context of Deep Neural Networks for optimizing the model efficiency, reducing computational requirements, and making them more suitable for resource-constraint environments. This choice is primarily due to its balance between performance and memory efficiency.

**Reduced model size:**  
'float-32' is the most commonly used precision. However, converting the weights of a model from 'float-32' to 'int-8' reduces the model's size by a factor of four. This makes the model suitable to run on devices with limited memory and storage capacity and at the same time results in reduced cost associated with transmission and storage space.  

**Faster inference:**  
Mathematical operations with lower precision are generally faster than those with higher precision. Moreover, with less bandwidth requirement the transmission time between memory and processor is further reduced. Certain AI accelerators are also optimized for low-precision operations.

**Maintaining Accuracy levels:**  
Although there is a trade-off between model accuracy and quantization, however, certain methods like Quantization Aware Training result in minimal accuracy loss making quantized models a viable option where accuracy and speed are both critical.

Quantization results in reducing the precision of both weights and activations (output from the activation layer that receives a weighted sum of inputs). There are four different techniques:  
1. Post Training Quantization  
   Converts a pre-trained model to a lower precision format. This results in a lightweight model although with a loss of accuracy. The process involves creating a representative dataset of the training dataset and determining the scale and zero-point values by calibrating the range of weights and activations.
3. Quantization Aware Training
   During the training process the model uses a lower precision format in the forward pass that introduces noise but in backward propagation full precision is used for optimization. This way the model is light and natively optimized for better accuracy with quantization.
5. Dynamic Quantization
   The model is trained with full precision but during inference time the quantization parameters are computed dynamically to convert weights and activations to a lower precision format.
7. Static Quantization
  With a careful calibration of a representative dataset, the quantization parameters are computed beforehand to reduce the precision of weights and activations.


More on quantization on [HuggingFace](https://huggingface.co/docs/optimum/en/concept_guides/quantization#quantization)


## BM25
Best Matching 25 (BM25) is one of the bag-of-words models to measure the rank of documents in search results for a given query. It is a modified version of tf-idf taking frequency threshold and document length into account.  

BM25 considers word frequency in a document to understand its frequency but at the same time, it dilutes its importance if the word is frequent across all the documents. Moreover, a long document with fewer repetitions of certain words results in lower importance for the word. BM25 considers all these three factors to generate a score that is ultimately used for ranking documents.  

On the other hand, tf-idf finds a set of frequent words for each document and their occurrence across the other documents. The frequent words are futher analyzed to find corresponding documents are relevant ones for document search.  

BM25 has been proven more superior to tf-idf in document search and ranking.  

More on BM25 on [Elastic](https://www.elastic.co/blog/practical-bm25-part-2-the-bm25-algorithm-and-its-variables)


