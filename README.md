# Graph-LDA: Graph Structure Priors to Improve the Accuracy in Few-Shot Classification

This repository contains the code of the experiments performed in the following paper

Graph-LDA: Graph Structure Priors to Improve the Accuracy in Few-Shot Classification

by Myriam Bontonou, Nicolas Farrugia and Vincent Gripon

## Abstract
It is very common to face classification problems where the number of available labeled samples is small compared to their dimension. These conditions are likely to cause underdetermined settings, with high risk of overfitting. To improve the generalization ability of trained classifiers, common solutions include using priors about the data distribution. Among many options, data structure priors, often represented through graphs, are increasingly popular in the field. In this paper, we introduce a generic model where observed class signals are supposed to be deteriorated with two sources of noise, one independent of the underlying graph structure and isotropic, and the other colored by a known graph operator. Under this model, we derive an optimal methodology to classify such signals. Interestingly, this methodology includes a single parameter, making it particularly suitable for cases where available data is scarce. Using various real datasets, we showcase the ability of the proposed model to be implemented in real world scenarios, resulting in increased generalization accuracy compared to popular alternatives.

## Usage
### 1. Dependencies
- Python >= 3.6
- Pytorch >= 1.3

### 2. Download Datasets
Our experiments are performed on a a neuroimaging dataset and a few-shot image classification dataset.

The neuroimaging dataset is based on the IBC dataset (releases 1 and 2) [2], which is accessible on NeuroVault [3] (collection 6618). The dataset can be downloaded by executing `Adapt_IBC_dataset.ipynb`. The splits and the graph structure [4] must be downloaded from https://drive.google.com/drive/folders/19a5se0l6MC-F1FTF5ittxFutkKHiWKgL?usp=sharing. For more information about the neuroimaging dataset, have a look at this [git](https://github.com/mbonto/fewshot_neuroimaging_classification).

The few-shot image classification dataset contains representations of the mini-Imagenet [1] images obtained at the output of the backbone pretrained in [Charting the Right Manifold: Manifold Mixup for Few-shot Learning](https://openaccess.thecvf.com/content_WACV_2020/papers/Mangla_Charting_the_Right_Manifold_Manifold_Mixup_for_Few-shot_Learning_WACV_2020_paper.pdf). The representations of the images can be downloaded from https://drive.google.com/drive/folders/1Ol-W0IvYkEuadkiDTgYp-0GUU2V2yENA?usp=sharing.

### 3. Perform Experiments
First experiments on simulated datasets are described in `Simulated_datasets.ipynb`.

The experiment on the neuroimaging dataset are accessible in `Neuroimaging_dataset.ipynb` and the one on the few-shot image classification dataset in `Image_dataset.ipynb`.

## References
[1] [Vinyals, O. et al. (2016) Matching networks for one shot learning.](https://proceedings.neurips.cc/paper/2016/file/90e1357833654983612fb05e3ec9148c-Paper.pdf)

[2] [Pinho, A.L. et al. (2020) Individual Brain Charting dataset extension, second release of high-resolution fMRI data for cognitive mapping.](https://project.inria.fr/IBC/ibc-in-a-nutshell/)

[3] [Gorgolewski, K.J. et al. (2015) NeuroVault.org: a web-based repository for collecting and sharing unthresholded statistical maps of the brain.](https://neurovault.org/)

[4] [Preti, M. G. et al. (2019) Decoupling of brain function from structure reveals regional behavioral specialization in humans.](https://www.nature.com/articles/s41467-019-12765-7)

## Contact
Please contact us if there are any problems.

Myriam Bontonou (myriam.bontonou@imt-atlantique.fr)
