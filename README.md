

# Net2Brain 🧠

<img src="docs/source/Net2Brain_Logo.png" alt="Net2Brain Logo" width="50%"/>


Welcome to [__Net2Brain__](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2025.1515873/full), a powerful toolbox designed to facilitate the comparison of human brain activity patterns with the activations of Deep Neural Networks (DNNs). With over 600 pre-trained DNNs available, Net2Brain empowers neuroscientists to explore and analyze the relationships between artificial and biological neural representations.

Net2Brain is a collaborative effort between CVAI and Radek Cichy's lab, aimed at providing a user-friendly toolbox for neural research with deep neural networks. 

**All-in-One Solution**: 
Net2Brain offers an all-in-one solution by providing access to over 600 pretrained neural networks, specifically trained for various visual tasks. This extensive collection allows researchers to extract features from a diverse range of models, including pretrained and random architectures. Moreover, Net2Brain offers flexibility by allowing users to integrate their own models, thereby expanding the scope of experiments that can be conducted to evaluate brain responses.

**Bridging Neural and AI Research**:
One of the primary objectives of Net2Brain is to facilitate the collaboration between neural and AI research. By providing a user-friendly toolbox, we aim to bridge the gap and empower non-computer scientists to leverage the benefits of deep neural networks in their neuroscientific investigations.

To delve deeper into the toolbox, check out our [ReadTheDocs](https://net2brain.readthedocs.io/en/latest/index.html) or our [tutorial notebooks](notebooks), or our latest [paper release](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2025.1515873/full).

# Updates 06/25
1. Added option to return all timepoints in RSA for MEG and EEG

# Updates 03/25
1. Added Centered Kernel Alignment (CKA) and Distributional Comparisons
2. Added Stacked Encoding and Structured Variance Partitioning
3. Added BoldMoments Dataset from [Lahner et al.](https://www.nature.com/articles/s41467-024-50310-3)
4. Added test-split from Things-Dataset from [Hebart et al.](https://elifesciences.org/articles/82580)
5. Added compability for Audio Models [see here](net2brain/architectures/audio_models.py)
6. Added veRSA [Khaligh-Razavi et al.](https://www.nature.com/articles/s41467-024-53147-y) and [Conwwell at al.](https://www.sciencedirect.com/science/article/pii/S0022249616301134)
6. Plotting Bugfixes
7. Making RSA more robust
8. Official [paper release](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2025.1515873/full) in [Frontiers in Neuroinformatics](https://www.frontiersin.org/journals/neuroinformatics)

# Updates 10/24
1. Added Ridge Regression to Linear Encoding
     - Added more flexibility to the code
     - Bugfix: In some cases only the last folds results were returned
2. Added more distance functions to RSA
3. Removed naming conventions for RSA (no fmri/meg needed in file name)


# Updates 07/24
1. Improved Dimensionality Reduction and included PCA next to SRP
2. Fixing Plotting Visualization Errors
3. Added new Workshop Notebooks with Datasets
4. Improved RDM Creation Notebook


# Updates 05/24
Next to minor bug/api fixes these are the main changes:

1. Added fully capabale Large-Language-Model functionality
2. Added new Datasets including helper functions to modify these datasets (NSD subset & Algonauts 2023)
3. Improved Linear Encoding functionalty (Attention: Import Name changed)
4. Improved Plotting functionality
5. Allowing Multimodal input for multimodal models (instead of one modality at once) 
6. Added new [Tutorial Notebook](/notebooks/Workshops/Net2Brain_Introduction_LLM.ipynb)
7. Changed RDM Creator Default back to Pearson Correlation
8. Patch 28.05: Downloading Datasets from different source
9. Patch 04.06: Fixing Plotting & PyVideo Bugs


# Documentation
Net2Brain now has its own [ReadTheDocs](https://net2brain.readthedocs.io/en/latest/index.html) page including tutorials for
- Installation
- Taxonomy, Feature Extraction, RDM Creation, Evaluation
- Adding your own models to the extractor
- Adding your own netset

# Tutorial Notebooks and Datasets

Net2Brain provides a set of [tutorial notebooks](notebooks) that demonstrate the various functionalities of the toolbox. These notebooks are designed to guide users through the process of model taxonomy exploration, feature extraction, RDM creation, and evaluation. 

To further facilitate your exploration, we also offer pre-downloaded datasets that you can use in conjunction with the tutorial notebooks. These datasets allow you to immediately dive into the experimentation process and gain hands-on experience with Net2Brain. Simply follow the instructions provided in the notebooks to access and utilize the datasets effectively.

## Available Datasets:
- The 78Images-Dataset from [Algonauts2019 Challenge Training Set A](http://algonauts.csail.mit.edu/2019/download.html)
- The 92Images-Dataset from [Algonauts2019 Challenge Test Set](http://algonauts.csail.mit.edu/2019/download.html)
- The bonnerpnas2017-Dataset from [Micheal F. Bonner et al.](https://www.pnas.org/doi/full/10.1073/pnas.1618228114)
- The NSD-Dataset (Algonauts Challenge) from [EJ Allen et al.](https://www.nature.com/articles/s41593-021-00962-x)
- A subset of the NSD-Dataset with the 872 images that all participants have seen from [EJ Allen et. al](https://www.nature.com/articles/s41593-021-00962-x)
- The test split of the Things Dataset from [Hebart et al.](https://elifesciences.org/articles/82580), which contains 12 trials for each image in the stimuli for 3 subjects
- A subset of the BoldMoment-Dataset by [Lahner et al.](https://www.nature.com/articles/s41467-024-50310-3)


The NSD-Datasets offers an additional range of functions designed to bridge NSD and COCO, enhancing the utility of the NSD dataset for comprehensive visual studies:

* **Image Downloads**: Access original COCO images directly from the NSD context.
* **ID Conversion**: Switch between NSD and COCO identifiers.
* **Segmentation Masks**: Obtain COCO segmentation masks corresponding to NSD images.
* **Caption Downloads**: Obtain COCO original caption to each downloaded image.
* **Image and Mask Manipulation**: Crop and rename files for consistency with NSD conventions.
* **Visualization**: Display the images along with their segmentaion masks.


| Dataset                              | Regions of Interest (ROIs) |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Algonauts 2019**                   | EVC, IT, whole brain MEG |
| **Algonauts 2021 (Bold Moments)**    | V1, V2, V3, V3ab, V4, 7AL, BA2, BMDgeneral, EBA, FFA, IPS0, IPS1-2-3, LOC, MT, OFA, PPA, PF, PFop, PFt, RSC, STS, TOS, whole brain, hemi-left, hemi-right |
| **Algonauts 2023 (NSD-Subset)**      | V1, V2, V3, hV4, EBA, FBA-1, FBA-2, FFA-1, FFA-2, Mfs-words, OFA, OPA, OWFA, PPA, RSC, VWFA-1, VWFA-2, hemi-left, hemi-right |
| **Algonauts 2023 (872 Subjects Subset)** | V1d, V2d, V3d, V1v, V2v, V3v, hV4, EBA, FBA-1, FBA-2, FFA-1, FFA-2, Mfs-words, OFA, OPA, OWFA, PPA, RSC |
| **THINGS-fMRI**                      | V1, V2, V3, hV4, VO1, VO2, lTOS, rTOS, lLOC, rLOC, lFFA, rFFA, lPPA, rPPA |
| **Bonner et al.**                    | V1d, V1v, V2d, V2v, V3a, V3b, V3d, V3v, hV4, LO1, LO2, PHC1, PHC2, VO1, VO2 |



# Key Functions

The toolbox encompasses several key functions to support comprehensive neural research:

1. __Feature Extraction__: Net2Brain enables the extraction of features from a vast collection of pretrained and random models, catering to a wide range of visual tasks. It also provides the flexibility to extract features from your own custom models, allowing you to tailor the analysis to your specific research needs.

2. __Creation of Representational Dissimilarity Matrices (RDMs)__: Users can generate RDMs to analyze the dissimilarity between neural representations.

3. __Evaluation__: Net2Brain incorporates various evaluation methos to compare neural representations with brain activity patterns, ranging from RSA, to Linar Encoding and Variance Partitioning Analysis.

4. __Plotting__: Net2Brain provides plotting functionalities that allow you to visualize and present your analysis results in a polished manner. The generated plots are designed to be publication-ready, making it easier for you to showcase your findings and share them with the scientific community.



# Compatibility and System Requirements

# Installation

To install Net2Brain and its dependencies, please follow these steps:

1. Install the repository on your machine. You can use the following command in your terminal:

```
pip install -U git+https://github.com/cvai-roig-lab/Net2Brain
```

2. Once the installation is complete, you can import Net2Brain in your Python environment and start utilizing its powerful features for neural research.




# Model Taxonomy

__Net2Brain__ provides a comprehensive model taxonomy system to assist users in selecting the most suitable models for their studies. This taxonomy system classifies models based on attributes such as dataset, training method, and visual task. Let's take a look at an example that showcases the usage of the taxonomy system:

```python
from net2brain.feature_extraction import show_taxonomy
from net2brain.feature_extraction import find_model_by_dataset
from net2brain.feature_extraction import find_model_by_training_method
from net2brain.feature_extraction import find_model_by_visual_task
from net2brain.feature_extraction import find_model_by_custom

# Show the taxonomy
show_taxonomy()

# Find models based on dataset
find_model_by_dataset("Taskonomy")

# Find models based on training method
find_model_by_training_method("SimCLR")

# Find models based on visual task
find_model_by_visual_task("Panoptic Segmentation")

# Find models based on custom attributes
find_model_by_custom(["COCO", "Object Detection"], model_name="fpn")
```

This taxonomy system provides a convenient way to search for models that align with specific research requirements.






# Examples of the Toolbox

## Feature Extraction

> Note: For more detailed instructions and customization options, refer to the provided notebooks and documentation.

Net2Brain allows you to extract features from a variety of pretrained models or your own custom models. This feature extraction process is crucial for analyzing neural network representations and comparing them with human brain activity patterns.

To extract features using Net2Brain, follow these steps:

```python
from net2brain.feature_extraction import FeatureExtractor
fx = FeatureExtractor(model='AlexNet', netset='Standard', device='cpu')

# Extract features from a dataset
fx.extract(data_path=stimuli_path, save_path='AlexNet_Feat')

# Consolidate features per layer (Optional)
fx.consolidate_per_layer()
```
In this example, we use the FeatureExtractor class to extract features from the AlexNet model. The extracted features are saved in a .npz file.

Net2Brain provides flexibility in selecting models, choosing layers for feature extraction, and saving the extracted features.


## Creating RDMs

> Note: For more detailed instructions and customization options, refer to the provided notebooks and documentation.

After feature extraction, the next step is to create Representational Dissimilarity Matrices (RDMs) using Net2Brain's RDM Creator.

To generate RDMs, follow these steps:

```python
from net2brain.rdm_creation import RDMCreator

feat_path = "AlexNet_Feat"
save_path = "AlexNet_RDM"


# Call the Class with the path to the features
creator = RDMCreator(verbose=True, device='cpu') 
save_path = creator.create_rdms(feature_path=feat_path, save_path=save_path, save_format='npz') 

```
In this example, the RDMCreator class is used to create RDMs from previously extracted features using the AlexNet model. The extracted features are located at feat_path, and the resulting RDMs will be saved at save_path.

The RDM Creator calculates dissimilarities between neural representations of different images and generates RDMs with a shape of (#Images, #Images) for each specified layer. These RDMs provide insights into the similarities and differences in neural representations.






## Evaluation: RSA and Plotting
> Note: For more detailed instructions and customization options, refer to the provided notebooks and documentation.

Net2Brain provides powerful evaluation capabilities to analyze and compare the representations of neural networks. One of the key evaluation metrics available is RSA (Representational Similarity Analysis). Additionally, the toolbox offers integrated plotting functionality to visualize evaluation results.
RSA Evaluation

To perform RSA evaluation, follow these steps:

```python
from net2brain.evaluations.rsa import RSA
from net2brain.utils.download_datasets import load_dataset

# Load the ROIs
stimuli_path, roi_path = load_dataset("bonner_pnas2017")

# Define the paths to the model and brain RDMs
model_rdms = "AlexNet_RDM"
brain_rdms = roi_path

# Start RSA evaluation
evaluation_alexnet = RSA(model_rdms, brain_rdms, model_name="AlexNet")

# Evaluate and obtain a pandas DataFrame
dataframe1 = evaluation_alexnet.evaluate()

# Display the results
display(dataframe1)
```

## Plotting RSA Evaluation Results

The integrated plotting functionality of Net2Brain allows you to easily visualize the RSA evaluation results. To plot the data using a single DataFrame, use the following code:

```python
from net2brain.evaluations.plotting import Plotting

# Initialize the plotter with the DataFrame
plotter = Plotting([dataframe1])

# Plot the results
# Optionally, pass metrix='R' if you do not want to lot with R2
results_dataframe = plotter.plot()
```

Refer to the provided notebooks and documentation for detailed instructions on customizing RSA evaluation and exploring additional options offered by Net2Brain


## Other Evaluation methods
`Net2Brain` has the ability to perform a wide range of evaluation methods to evaluate the correlation beetween artifical and biological network responses. Among those are:
1. RSA
2. Weighted RSA
3. Searchlight Evaluation
4. Linear Encoding
5. Variance Partitioning Analysis
6. CKA
7. Distributional Comparisons
8. Stacked Encoding
9. Structured Variance Paritioning

To delve deeper into how they work, check out our [ReadTheDocs](https://net2brain.readthedocs.io/en/latest/index.html) or our [tutorial notebooks](notebooks)





# Contribution and Support

Net2Brain is an open-source project, and we welcome contributions from the community. If you encounter any issues, have suggestions for improvements, or would like to contribute to the project, feel free to write an issue or submit pull requests yourself.

For support, inquiries, or feedback, please reach out to us. You can find our contact information in the repository's documentation.

We hope Net2Brain proves to be a valuable resource in your neuroscientific investigations. Happy exploring!



## Contributors of Net2Brain

- M. Sc. Domenic Bersch
- Dr. Sari Saba-Sadiya
- M. Sc. Martina Vilas
- M. Sc. Timothy Schaumlöffel
- Dr. Kshitij Dwivedi
- M. Sc. Christina Sartzetaki
- Dr. Radoslaw Martin Cichy
- Prof. Dr. Gemma Roig


## Citing Net2Brain
If you use Net2Brain in your research, please don't forget to cite our [paper in Frontiers](https://www.frontiersin.org/journals/neuroinformatics/articles/10.3389/fninf.2025.1515873/full):
```bash
Bersch D, Vilas MG, Saba-Sadiya S, Schaumlöffel T, Dwivedi K, Sartzetaki C, Cichy RM and Roig G (2025) Net2Brain: a toolbox to compare artificial vision models with human brain responses. Front. Neuroinform. 19:1515873. doi: 10.3389/fninf.2025.1515873
```


## References
This toolbox is inspired by the Algonauts Project and contains collections of artificial neural networks from different sources.

- **The Algonauts Project:** Radoslaw Martin Cichy, Gemma Roig, Alex Andonian, Kshitij Dwivedi, Benjamin Lahner, Alex Lascelles, Yalda Mohsenzadeh, Kandan Ramakrishnan, and Aude Oliva. (2019). The Algonauts Project: A Platform for Communication between the Sciences of Biological and Artificial Intelligence. arXiv, arXiv:1905.05675
- **The dataset provided in the library:** Radoslaw M. Cichy, Dimitrios Pantazis and Aude Oliva. (2016). Similarity-Based Fusion of MEG and fMRI Reveals Spatio-Temporal Dynamics in Human Cortex During Visual Object Recognition. Cerebral Cortex, 26 (8): 3563-3579.
- **RSA-Toolbox:** Nikolaus Kriegeskorte, Jörn Diedrichsen, Marieke Mur and Ian Charest (2019) The toolbox replaces the 2013 matlab version the toolbox of rsatoolbox previously at ilogue/rsatoolbox and reflects many of the new methodological developements. Net2Brain uses its functionality to perform "Weighted RSA".
- **PyTorch Models:** https://pytorch.org/vision/0.8/models.html
- **CORnet-Z and CORnet-RT:** Kubilius, J., Schrimpf, M., Nayebi, A., Bear, D., Yamins, D.L.K., DiCarlo, J.J. (2018) CORnet: Modeling the Neural Mechanisms of Core Object Recognition. biorxiv. doi:10.1101/408385
- **CORnet-S:** Kubilius, J., Schrimpf, M., Kar, K., Rajalingham, R., Hong, H., Majaj, N., ... & Dicarlo, J. (2019). Brain-like object recognition with high-performing shallow recurrent ANNs. In Advances in Neural Information Processing Systems (pp. 12785-12796).
- **MoCo:** Kaiming He and Haoqi Fan and Yuxin Wu and Saining Xie and Ross Girshick, Momentum Contrast for Unsupervised Visual Representation Learning (2019), arXiv preprint arXiv:1911.05722
- **SwAv:** Caron, Mathilde and Misra, Ishan and Mairal, Julien and Goyal, Priya and Bojanowski, Piotr and Joulin, Armand ,Unsupervised Learning of Visual Features by Contrasting Cluster Assignments (2020), Proceedings of Advances in Neural Information Processing Systems (NeurIPS)
- **Taskonomy:** Zamir, Amir R and Sax, Alexander and and Shen, William B and Guibas, Leonidas and Malik, Jitendra and Savarese, Silvio, Taskonomy: Disentangling Task Transfer Learning (2018), 2018 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)
- **Image Models:** Ross Wightman, PyTorch Image Models(2019), 10.5281/zenodo.4414861, https://github.com/rwightman/pytorch-image-models
- **SlowFast:** Haoqi Fan and Yanghao Li and Bo Xiong and Wan-Yen Lo and Christoph Feichtenhofer, PySlowFast(2020), https://github.com/facebookresearch/slowfast
- **Torchextractor** https://github.com/antoinebrl/torchextractor

## Funding
This project was funded by the German Research Foundation (DFG)–DFG Research Unit FOR 5368 (GR) awarded to Gemma Roig; DFG (CI241/1-1, CI241/3-1, and CI241/7-1) awarded to Radoslaw M. Cichy and a European Research Council (ERC) starting grant (ERC-2018-STG 803370) awarded to Radoslaw M. Cichy. We are grateful for access to the computing facilities of the Center for Scientific Computing at Goethe University and Freie Universität Berlin.
