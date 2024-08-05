


## Quantization:
It is a crucial technique for several reasons, especially in the context of Deep Neural Networks for optimizing the model efficiency, reducing computational requirements, and making them more suitable for resource-constraint environments. This choice is primarily due to its balance between performance and memory efficiency.

**Reduced model size:**  
'float-32' is the most commonly used precision. However, converting the weights of a model from 'float-32' to 'int-8' reduces the model's size by a factor of four. This makes the model suitable to run on devices with limited memory and storage capacity and at the same time results in reduced cost associated with transmission and storage space.  

**Faster inference:**  
Mathematical operations with lower precision are generally faster than those with higher precision. With less bandwidth requirement the transmission of time between memory and processor is further reduced. Moreover, certain AI accelerators are optimized for low-precision operations.

**Maintaining Accuracy levels:**  
Although there is a trade-off between model accuracy with quantization, however, certain methods like Quantization Aware Training result in minimal accuracy loss making quantized models a viable option where accuracy and speed are both critical.

Quantization results in reducing the precision of both weights and activations (output from the activation layer that receives a weighted sum of inputs). There are four different techniques:  
1. Post Training Quantization  
   Converts a pre-trained model to a lower precision format. This results in a lightweight model although with a loss of accuracy. The process involves creating a representative dataset of the training dataset and determining the scale and zero-point values by calibrating the range of weights and activations.
3. Quantization Aware Training
   During the training process the model uses a lower precision format in the forward pass that introduces noise but in backward propagation full precision is used for optimization. This way the model is light and natively optimized for better accuracy with quantization.
5. Dynamic Quantization
   The model is trained with full precision but during inference time the quantization parameters are computed dynamically to convert weights and activations to a lower precision format.
7. Static Quantization
  With a careful calibration of a representative dataset, the quantization parameters are computed beforehand to reduce the precision of weights and activations.
