


## Quantization:
It is a crucial technique for several reasons, especially in the context of Deep Neural Networks for optimizing the model efficiency, reducing computational requirements, and making them more suitable for resource-constraint environments. This choice is primarily due to its balance between performance and memory efficiency.

**Reduced model size:**  
'float-32' is the most commonly used precision. However, converting the weights of a model from 'float-32' to 'int-8' reduces the model's size by a factor of four. This makes the model suitable to run on devices with limited memory and storage capacity and at the same time results in reduced cost associated with transmission and storage space.  

**Faster inference:**  
Mathematical operations with lower precision are generally faster than those with higher precision. With less bandwidth requirement the transmission of time between memory and processor is further reduced. Moreover, certain AI accelerators are optimized for low-precision operations.

**Maintaining Accuracy levels:**  
Although there is a trade-off between model accuracy with quantization, however, certain methods like Quantization Aware Training result in minimal accuracy loss making quantized models a viable option where accuracy and speed are both critical.

Quantization results in reducing the precision of both weights and activations (output from the activation layer that receives a weighted sum of inputs)
