# Paper reading notes for performance and energy efficient machine learning accelerators

- **Cnvlutin: Ineffectual-Neuron-Free Deep Convolutional Neural Network Computing.** (University of Toronto, University of British Columbia)
    - *A DNN accelerator that can dynamically eliminate most ineffectual multiplications.*
    - *Targets the convolutional layers of DNNs which dominate the execution time*
- **EIE: Efficient Inference Engine on Compressed Deep Neural Network.** (Stanford University, Tsinghua University)
    - *First acclerator for sparse and weight sharing neural networks*
        - *achieves weight sharing by store only index of quantized weights (a shared table between PEs)*
    - *Targets the fully connected layers, to performs inference on compressed models*
    - *Proposed customized sparse matrix multiplication, which exploit both static and dynamic sparsity of the model*
        - *static sparsity: weights stored by variation of CSR (sparsity of weights)*
        - *dynamic sparsity: leading non-zeros detection (sparsity of input vectors)*
    - *Proposed a method of both distributed computation and storage to parallelize sparsified layer across multiple PEs*
        - *FIFO used as activation queue to achieve load balance between multiple PEs*
- **Minerva: Enabling Low-Power, High-Accuracy Deep Neural Network Accelerators.** (Harvard University)
- **Eyeriss: A Spatial Architecture for Energy-Efficient Dataflow for Convolutional Neural Networks.** (MIT, NVIDIA)
    - *Present an energy analysis framework.*
    - *Propose an energy-efficienct dataflow called Row Stationary, which considers three levels of reuse.*
