# Paper reading notes for efficient machine learning models
- **BinaryConnect: Training Deep Neural Networks with binary weights during propagations.** (NIPS'2015)
    - *weight constrained to binary value -1 or 1*
        - *binarize to +1 with probability p=σ(weight)*
        - *binarize to -1 with probability p=1-σ(weight)*
    - *binary weights will bring great benefits to hardware by replacing many multiply-accumulate operations by simple accumulation*
    - *forward and backward pass use wb, but only the real value weight w are updated*

- **Regularization of Neural Networks using DropConnect**
    - *randomly subset of activations are set to zero when training with dropout, DropConnect instead set subset of weights to zero*
