This project focuses on the curation and exploratory data analysis of an agricultural computer vision dataset designed for plant health classification. The objective is to establish a validated data foundation for training and evaluating deep learning models—particularly lightweight neural network architectures—to automatically identify foliar diseases and physical conditions.

**Dataset Overview**
The core dataset contains 3,355 verified images categorized into six distinct classes representing various states of plant health:

* **Healthy** (831 images, ~24.8%) and **Anthracnose** (773 images, ~23.0%) make up the majority of the dataset.
* **Sooty Mould** (529 images), **Senescence** (510 images), and **Insect Infestation** (441 images) provide substantial mid-tier representation.
* **Dried** (271 images, ~8.1%) represents the minority class, introducing a moderate class imbalance that can be addressed via targeted sampling or loss-weighting strategies during training.

**Data Quality and Preprocessing**
To ensure the integrity of the data pipeline for downstream machine learning tasks, an automated preprocessing script was executed. It successfully parsed the dataset to confirm there are zero corrupted files and isolated only a single duplicate image.

A key characteristic of this dataset is its high degree of spatial scale variance. Image resolutions range from a minimum of 512x512 to a maximum of 4000x3000, with a mean dimension of 515x514. This significant variance in input resolution makes the dataset an excellent testbed for evaluating models designed to handle resolution-based domain shifts, or for benchmarking the effectiveness of multi-scale feature fusion modules under varying real-world capture conditions. The exploratory analysis concludes by generating class distribution bar charts and sample image grids to visually validate the data before progressing to PyTorch model training and evaluation.
