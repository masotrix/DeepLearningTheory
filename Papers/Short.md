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
- Techniques
  * Learning annealing 0.1 -> 0.001 (when error plateaus)
  * Momentum 0.9
  * 60xe+4 iterations
  * No dropout
  * Dense evaluation: Full convolutional
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
  * ILSVRC-2015: 3.6% top-5,
- Problems solved
  * Degradation due exponentially low convergence rates
    * **Solution**: Residual Functions


### Notes
1. Techniques: Permanent general improvements
1. Specific Arch Details: Temporal specific improvements
1. ILSVRC: Imagenet Large scale visual recognition challenge
