# TuxKConfig: Linux Kernel Configurations Dataset

Welcome to the `tuxkconfig` repository! This repository complements the **TuxKConfig dataset**, a comprehensive collection of Linux kernel configurations designed for performance and evolution analysis. Spanning seven kernel versions (4.13 to 5.8), it includes over 243,000 configurations with detailed metadata such as binary sizes and compilation times, enabling research in predictive modeling, transfer learning, feature selection, and more.

This dataset is introduced in the datapaper:  
**"Linux Kernel Configurations at Scale: A Dataset for Performance and Evolution Analysis"**  
(Anonymous Author(s), EASE 2025).

## Dataset Overview

TuxKConfig captures the complexity of the Linux kernel's configuration space across multiple versions:
- **Versions**: 4.13, 4.15, 4.20, 5.0, 5.4, 5.7, 5.8
- **Configurations**: 243,861 total (ranging from 23,159 in 5.7 to 92,562 in 4.13)
- **Features**: Over 15,000 binary-encoded options per version (e.g., `CONFIG_PCI`, `CONFIG_HAMACHI`)
- **Metrics**: Binary size (vmlinux, in MB), compilation time (in seconds), and derived features like the count of enabled options
- **Architecture**: x86_64
- **Source**: Generated using TuxML with random sampling via `randconfig`

The dataset is ideal for studying software configurability, evolution, and non-functional properties in a real-world, large-scale system.

## Accessing the Dataset

The TuxKConfig dataset is publicly available on OpenML as a collection of version-specific datasets, plus an aggregator dataset linking all versions:
- **Aggregator Dataset**: [TuxKConfig (ID: 46749)](https://openml.org/d/46749)  
  - Links to individual version datasets are embedded within this entry.
- **Individual Versions**:
  - [4.13 (ID: 46738)](https://openml.org/d/46738)
  - [4.15 (ID: 46739)](https://openml.org/d/46739)
  - [4.20 (ID: 46740)](https://openml.org/d/46740)
  - [5.0 (ID: 46741)](https://openml.org/d/46741)
  - [5.4 (ID: 46742)](https://openml.org/d/46742)
  - [5.7 (ID: 46743)](https://openml.org/d/46743)
  - [5.8 (ID: 46744)](https://openml.org/d/46744)

Each dataset is provided as a CSV file, compressed to approximately 2 GB in total.

## Usage Example

## Notebooks

1. **[Performance Prediction Notebook](notebooks/performance_prediction.ipynb)**  
   - **Purpose**: This notebook uses machine learning techniques to predict the performance (e.g., build time or binary size) of Linux kernel configurations based on historical data. It leverages models trained on configuration features to assist in optimizing kernel builds.

2. **[Build Failure Analysis Notebook](notebooks/build_failure_analysis.ipynb)**  
   - **Purpose**: This notebook analyzes common causes of build failures in Linux kernel configurations. It processes logs and configuration data to identify patterns and suggest potential fixes.

3. **[Configuration Space Exploration Notebook](notebooks/config_space_exploration.ipynb)**  
   - **Purpose**: This notebook explores the vast configuration space of the Linux kernel, visualizing the relationships between configuration options and their impact on system properties like size or resource usage.

4. **[Feature Importance Analysis Notebook](notebooks/feature_importance_analysis.ipynb)**  
   - **Purpose**: This notebook evaluates the importance of individual configuration features (e.g., specific kernel options) in determining outcomes such as binary size or build success, using statistical and ML-based methods.

To run the notebook:
1. Clone this repository: `git clone https://github.com/username/tuxkconfig.git`
2. Install dependencies: `pip install openml scikit-learn pandas numpy jupyter`
3. Open the notebook: `jupyter notebook notebooks/tuxkconfig.ipynb`

  
