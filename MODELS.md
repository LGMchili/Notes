# Paper reading notes for efficient machine learning models
- **BinaryConnect: Training Deep Neural Networks with binary weights during propagations.** (NIPS'2015)
    - *weight constrained to binary value -1 or 1*
        - *binarize to +1 with probability p=σ(weight)*
        - *binarize to -1 with probability p=1-σ(weight)*
    - *binary weights will bring great benefits to hardware by replacing many multiply-accumulate operations by simple accumulation*
    - *forward and backward pass use wb, but only the real value weight w are updated*

- **Regularization of Neural Networks using DropConnect**
    - *randomly subset of activations are set to zero when training with dropout, DropConnect instead set subset of weights to zero*

- **XNOR-Net: ImageNet Classification Using Binary Convolutional Neural Networks**
    - *two approximations of CNN were proposed*
        - *In Binary-Weight-Networks all the weight values are approximated with binary values*.
            - *32x memory and 2x computation saving, accuracy of 56.8% on ImageNet*
        - *In XNOR-Networks, both the filters and the input to convolutional layers are binary.*
            - *32x memory and 58x computation saving, accuracy of 44.2% on ImageNet*

- **SQUEEZENET: ALEXNET-LEVEL ACCURACY WITH 50X FEWER PARAMETERS AND <0.5MB MODEL SIZE** (ICLR 2017)
    - *identify CNN that have few parameters while maintain the accuracy. 3 strategies(employ by fire module):*
        - *replace 3x3 filter with 1x1 filter*
        - *decrease the number of input channels to 3x3 filters*
        - *downsample late in the network to gain accuracy*
    - *50x reduction (higher than deep compression)*
        - *510x reduction when further compress by deep compression*
    - *microarchitecture design space*
        - *squeeze ratio: number of filters squeeze layers / number of filters in expand layers*
        - *trade off between 1x1 and 3x3 filters: repalce some 3x3 filters with 1x1 filters*
    - *macroarchitecture design space*
        - *add bypass connect, using complex bypass (with 1x1 conv) when number of input and output output channels are different*
            - *alleviate the representational bottleneck introduced by squeeze layers*
            - *accuracy improvement*
