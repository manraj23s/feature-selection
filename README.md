Data Visualization, Imputation, & Feature Selection: MNIST Case Study

This project explores the application of dimensionality reduction and neural network modeling on the MNIST dataset, a classic benchmark for handwritten digit recognition. The MNIST dataset consists of 70,000 grayscale images (60,000 for training and 10,000 for testing), each of size 28x28 pixels, representing digits from 0 to 9.

---

## Dimensionality Reduction & Visualization

High-dimensional data such as MNIST (each image is a 784-dimensional vector) is challenging to visualize and analyze directly. To address this, we employed several dimensionality reduction techniques:

- **PCA (Principal Component Analysis):** A linear method projecting data onto principal components to reduce dimensionality for visualization and pattern discovery.
- **t-SNE (t-Distributed Stochastic Neighbor Embedding):** A nonlinear method that preserves local relationships, making it effective for visualizing clusters and local structure.
- **UMAP (Uniform Manifold Approximation and Projection):** Another nonlinear technique, particularly adept at retaining both local and some global structure, and able to distinctly separate digit classes in visualization.

Applying these techniques enabled intuitive 2D/3D visualizations, revealing meaningful clusters, potential outliers, and the underlying structure of the dataset.

---

## Neural Network Modeling

After visual exploration, we developed a **Multilayer Perceptron (MLP)** using TensorFlow and Keras to classify the handwritten digits.

**Key Steps:**
- **Data Preparation:**  
  - Normalized pixel values to the [0, 1] range by dividing by 255.  
  - Ensured training and test sets were properly formatted and stratified.
- **Model Architecture:**  
  - Input layer flattens the 28x28 images.
  - Two hidden layers with 200 and 100 neurons, using sigmoid activations.
  - Output layer with 10 neurons (one for each digit class).
- **Training:**  
  - Used the Adam optimizer for efficient training.
  - Employed sparse categorical cross-entropy loss due to integer labels and multi-class output.
  - Trained for 20 epochs with a batch size of 2,000 samples.

**Results:**  
- Achieved a final test accuracy of **94.05%**, indicating robust performance in classifying handwritten digits.
- Further tuning of epochs and batch size may yield even higher accuracy.

---

## Key Learnings & Impact

- **Dimensionality reduction** (PCA, t-SNE, UMAP) is invaluable for visualizing complex, high-dimensional datasets, making it easier to identify clusters, patterns, and anomalies.
- A well-designed **MLP neural network** can achieve high accuracy on image classification tasks, even with relatively straightforward architectures.
- The workflow of visualizing data, understanding its structure, and then modeling leads to more interpretable machine learning solutions and better performance.

---

**Instructor:** IE 7860  
**Author:** Manraj Singh  
**Contact:** [manraj23singh@gmail.com](mailto:manraj23singh@gmail.com)
