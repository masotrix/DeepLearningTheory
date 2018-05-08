## Deep Learning Evolution

### Alexnet 2012
- First Convolutional
- Techniques
  * Data augmentation (Regularization)
  * Dropout (Regularization)
- Specific Arch Details:
  * LRN: Local response normalization (Better generalization)
  * Overlapping Pooling: stride smaller than size (gener+regu)
- Overall Arch
  * 5 Conv + 3 FC (8 wlayers)
- Results
  * ILSVRC-2012: 15.3% top-5, 36.7% top-1
- Problems solved:
  * Lack of a priori structure:
    * **Solution**: Use of convolution layers


### VGG 2014
- Very deep + small receptive fields
- Techniques
  * L2 regularization
- Specific Arch Details:
  * Multi-scale training and testing
  * Multi-crop evaluation
  * Dense evaluation: Full conv
- Overall Arch:
  * 16 Conv + 3 FC (19 wlayers)
- Results:
  * ILSVRC-2014: 6.8% top-5, 23.7% top-1
- Problems solved:
  * Shallow depth:
    * **Solution**: Use of smaller receptive fields

  
### Resnet 2015
- Ultra deep + residual functions
- New techniques
  * Residual Functions
  * Bottleneck layers
  * Dense evaluation: Full convolutional
- Standard Techniques
  * Learning annealing 0.1 -> 0.001 (when error plateaus)
  * Momentum 0.9
  * 60xe+4 iterations
  * No dropout
  * L2 norm: weight decay e-4
  * Color Data augmentation (Regularization)
  * Batch Normalization, after conv and before activ
- Specific Arch Details:
  * Multi-scale training (256,480)
  * 224x224 random crop
  * Per-pixel mean substraction
  * Average Multi-scale test evaluation (224, 640)
  * 10-Crop testing
  * Dense testing evaluation: Full conv
- Overall Arch:
  * (152 wlayers)
  * 256 minibatch
- Results:
  * ILSVRC-2015: 3.6% top-5, 19.8% top-1
  * CIFAR-100: 27.22% test
  * CIFAR-10: 6.41% test
- Problems solved
  * New kind of vanishing gradient
    * **Solution**: Residual Functions
  * Increased complexity
    * **Solution**: Bottleneck design
    
### DenseNet 2018
- Extremely deep layers + dense connectivety
- New techniques
  * Reduced feature map growth
  * Dense blocks
  * Transition Layers (BN+1x1Conv+Avg pooling)
- Standard Techniques (Used mainly in ImageNet-2012)
  * Learning annealing 0.1 -> 0.01 -> 0.001 (30,60 epochs)
  * Nesterov momentum 0.9 with dampening
  * 90 epochs
  * No dropout
  * Dense evaluation: Full convolutional
  * L2 norm: weight decay e-4
  * Color Data augmentation (Regularization)
  * Bottleneck layers
  * Batch Normalization, after conv and before activ
- Overall Arch:
  * (264 wlayers)
  * 256 minibatch
- Results:
  * ILSVRC-2012: 5.3% top-5, 20.8% top-1
  * CIFAR-100: 17.18%
  * CIFAR-10: 3.46% 
- Problems solved
  * Increased parameters, overfitting and train time
    * **Solution**: Dense connectivety
  
  
  


### Notes
1. Techniques: Permanent general improvements
1. Specific Arch Details: Temporal specific improvements
1. ILSVRC: Imagenet Large scale visual recognition challenge
