# ERA4-Assignmet5
ERA4/Assignmet5
Total Parameter Count Test – MNIST

This repository contains experiments designed to evaluate the effect of parameter count, Batch Normalization (BN), Dropout, and the choice between Fully Connected (FC) layers and Global Average Pooling (GAP) on model performance.

📊 Parameter Count Summary

The optimized network was designed to stay near 20K trainable parameters.

Total params: 20,282
Trainable params: 20,282
Non-trainable params: 0

🧩 Model Components
1. Batch Normalization

Applied after convolution layers.

Helps stabilize training and improve generalization.

2. Dropout

Applied after most convolution layers.

Reduces overfitting with a dropout rate of 0.1.

3. Fully Connected Layer vs. GAP

FC Layer: Linear(16 → 10)

GAP: AdaptiveAvgPool2d((1,1)) used before the FC layer.

⚡ Training Runtime Logs
Training Configuration

Dataset: MNIST

Optimizer: SGD with momentum (0.9)

Scheduler: StepLR (step_size=5, gamma=0.5)

Target Accuracy: 99.5%

Epochs: 20

🔹 Run Log (with BN + Dropout + GAP + FC)
Epoch 1: loss=0.0499, acc=81.56%
Test  Avg loss: 0.0831, Accuracy: 9751/10000 (97.51%)

Epoch 2: loss=0.0440, acc=96.81%
Test  Avg loss: 0.0446, Accuracy: 9880/10000 (98.80%)

Epoch 3: loss=0.1291, acc=97.48%
Test  Avg loss: 0.0372, Accuracy: 9895/10000 (98.95%)

Epoch 5: loss=0.1698, acc=98.08%
Test  Avg loss: 0.0314, Accuracy: 9903/10000 (99.03%)

Epoch 7: loss=0.0866, acc=98.61%
Test  Avg loss: 0.0247, Accuracy: 9930/10000 (99.30%)

Epoch 11: loss=0.0685, acc=98.93%
Test  Avg loss: 0.0210, Accuracy: 9941/10000 (99.41%)

Epoch 15: loss=0.0063, acc=99.01%
Test  Avg loss: 0.0207, Accuracy: 9934/10000 (99.34%)

Epoch 19: loss=0.2475, acc=99.05%
Test  Avg loss: 0.0181, Accuracy: 9945/10000 (99.45%)

✅ Finished Training. Best accuracy: 99.45%

✅ Observations

The optimized model achieved 99.45% accuracy with ~20K parameters.

Batch Normalization improved stability and speed of convergence.

Dropout helped reduce overfitting.

GAP + small FC maintained parameter efficiency while reaching near-SOTA performance on MNIST.
