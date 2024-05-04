# Hybrid Neural Network (HNN) without Defense Against White-box, Targeted, Compounded Adversarial Attacks

This repository presents a quantum-classical (or hybrid) neural network without defense against white-box, targeted, compounded adversarial attack mechanism. The core libraries employed are `pytket`, `pytket-qiskit`, and `torchattacks`.

## Motivating Articles and Related Works

Bajaj, A., & Vishwakarma, D. K. (2024). A state-of-the-art review on adversarial machine learning in image classification. Multimedia Tools and Applications, 83(3), 9351-9416. https://link.springer.com/article/10.1007/s11042-023-15883-z

Kim, H. (2020). Torchattacks: A pytorch repository for adversarial attacks. arXiv preprint arXiv:2010.01950. https://arxiv.org/abs/2010.01950

https://github.com/Harry24k/adversarial-attacks-pytorch

## HNN Overview

The provided Python script includes:

- Loading and preprocessing the MNIST dataset
- Implementation of a quantum layer using `pytket` for quantum operations
- Creation of a TensorFlow model with the quantum layer
- Conversion of the TensorFlow model to a PyTorch model for adversarial attacks
- Assessment of model performance under adversarial attacks

## Quantinuum

Quantinuum is a leading-edge platform for quantum computing, offering tools and resources to developers and researchers to explore and develop quantum algorithms and applications. With Quantinuum, users can access quantum hardware, simulators, and development environments to accelerate quantum computing research and development.

## pytket Python Library

pytket is a Python library developed by Quantinuum for working with quantum circuits and quantum computing tasks. It provides a high-level interface for constructing, manipulating, and simulating quantum circuits, making it easier for users to experiment with quantum algorithms and protocols. pytket supports various quantum backends and integrates seamlessly with other quantum computing libraries.

## pytket-qiskit Python Library

pytket-qiskit is an extension of pytket that enables seamless integration with Qiskit, IBM's open-source quantum computing framework. By leveraging pytket-qiskit, users can combine the capabilities of pytket with the extensive functionality of Qiskit, including access to IBM Quantum devices, simulators, and quantum algorithms. This integration enhances the versatility and interoperability of both libraries, empowering users to explore and develop quantum applications effectively.

## torchattacks Python Library

torchattacks is a Python library for crafting adversarial attacks on deep neural networks using PyTorch. It provides a comprehensive set of attack algorithms and techniques, including Fast Gradient Sign Method (FGSM), Projected Gradient Descent (PGD), DeepFool, and more. With torchattacks, users can evaluate the robustness of their neural network models against adversarial perturbations, facilitating research and development in adversarial machine learning and security.

## White-box Attacks

White-box attacks are adversarial attacks where the attacker has complete knowledge of the target model, including its architecture, parameters, and gradients. This enables the attacker to craft highly effective adversarial examples tailored to exploit vulnerabilities in the target model.

## Targeted Attacks

Targeted attacks are adversarial attacks aimed at causing the model to misclassify input samples as specific target classes chosen by the attacker. Unlike untargeted attacks, which aim to generate any incorrect output, targeted attacks are more challenging and can be used for specific manipulation of model behavior.

## Compounded Attacks

Compounded attacks combine multiple adversarial attack techniques to increase the effectiveness and stealthiness of the attack. By leveraging a combination of white-box, targeted, and other attack strategies, compounded attacks pose a significant threat to the robustness and security of machine learning models. The use of compounded attacks requires sophisticated techniques and tools, such as those provided by torchattacks, to evaluate and defend against adversarial threats effectively.

The incorporation of white-box, targeted, and compounded attacks using torchattacks enables comprehensive evaluation of model robustness and enhances the understanding of adversarial vulnerabilities in deep neural networks.

## HNN: Quantum Layer

Utilizing `pytket`, the quantum layer encodes classical inputs into a quantum circuit and retrieves output probabilities.

## HNN: TensorFlow Model

Initially, a convolutional neural network (CNN) architecture is constructed using TensorFlow, with a quantum layer inserted before the final dense layer.

## HNN: PyTorch Model

To facilitate adversarial attacks using `torchattacks`, the TensorFlow model is converted to a PyTorch model, maintaining the same architecture.

## HNN:  Adversarial Attacks

Adversarial attacks, including Fast Gradient Sign Method (FGSM), Projected Gradient Descent (PGD), and DeepFool, are applied using `torchattacks`. These attacks aim to perturb input images to mislead model predictions.

### HNN: Attack Types

- **FGSM**: Fast Gradient Sign Method with reduced epsilon for minimized perturbation.
- **PGD**: Projected Gradient Descent with optimized parameters for improved robustness.
- **DeepFool**: Iterative attack with tailored parameters to generate adversarial samples.

## HNN Results

The models are evaluated pre- and post-adversarial attacks to analyze the impact on accuracy and loss metrics.

# Pre-attack Results
![](https://github.com/ericyoc/quantinuum-hnn-compound-adv-attack-poc/blob/main/pre_attack_hnn_mnist.jpg)

# Post Attack Results
![](https://github.com/ericyoc/quantinuum-hnn-compound-adv-attack-poc/blob/main/post_attack_hnn_mnist.jpg)

## Conclusion

The integration of quantum layers with classical neural networks demonstrates potential advancements in robustness against adversarial attacks. By leveraging quantum features within hybrid architectures and employing state-of-the-art adversarial attack techniques, the models exhibit enhanced resilience to input data perturbations.

## Disclaimer
This repository is intended for educational and research purposes.

