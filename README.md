# Sparse Autoencoder for Analyzing BrainBERT Embeddings

This repository contains a Jupyter notebook that implements a sparse autoencoder to analyze BrainBERT embeddings, extract hidden layer activations, cluster neuron activations, and generate saliency maps for seizure and non-seizure embeddings.

## Overview

### BrainBERT Embeddings
BrainBERT is a specialized vision transformer model designed to analyze SEEG (stereo-electroencephalography) data. It processes spectrograms—representations of the frequency components of neural signals over time—to generate dense vector embeddings. These embeddings encapsulate complex neural activity patterns, making them useful for distinguishing between seizure and non-seizure states.

### Motivation
This project is motivated by the need to understand how models detect seizures and what features they focus on. By applying interpretability methods to BrainBERT embeddings, the goal is to uncover key biomarkers that can detect (and eventually predict) seizures by linking features to their physiological mechanisms.

## Key Components

- **Sparse Autoencoder**: A custom sparse autoencoder is trained on BrainBERT embeddings to extract hidden layer activations that may reveal underlying neural patterns.
- **Clustering Neurons**: Neuron activations are clustered to hypothesize about the information each cluster might represent, such as brain areas or specific frequency bands.
- **Saliency Maps**: Saliency maps are generated to identify the most influential features for distinguishing between seizure and non-seizure embeddings.
- **Feature Importance Analysis**: The most important features are analyzed based on differences in saliency values, aiming to identify neural patterns responsible for seizure events.

## Usage

1. **Install Necessary Packages**:
    ```bash
    pip install torch scikit-learn numpy matplotlib captum
    ```

2. **Run the Notebook**: Open the notebook and follow the step-by-step instructions to load BrainBERT embeddings, train the sparse autoencoder, and perform the analyses.

3. **Explore Results**: Use the provided visualizations to explore neuron clusters and saliency maps, and analyze the features most important for seizure detection.

## Data and Model Files

You can find the `.pth` file for the sparse autoencoder, as well as the label and embeddings numpy files, at this [link](https://drive.google.com/drive/folders/1TvYJmGmPMLu4m3Viohyg3VN_zrHE6qpb?usp=sharing).

## Future Work
Future analyses aim to further investigate neuron clusters and their potential link to specific brain regions or frequency bands, providing deeper insights into the physiological mechanisms underlying seizures.

## References
- [BrainBERT Paper](#) (link to the original BrainBERT paper for more details on the model)

## License
This project is licensed under the MIT License.
