# LIFD Machine Learning For Earth Sciences


![LIFD logo](https://raw.githubusercontent.com/cemac/LIFD_ENV_ML_NOTEBOOKS/main/images/LIFDlogo.png)

![cemac logo](https://raw.githubusercontent.com/cemac/cemac_generic/master/Images/cemac.png)


 [![GitHub release](https://img.shields.io/github/release/cemac/LIFD_ENV_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS/releases) [![GitHub top language](https://img.shields.io/github/languages/top/cemac/LIFD_ENV_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS) [![GitHub issues](https://img.shields.io/github/issues/cemac/LIFD_ENV_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS/issues) [![GitHub last commit](https://img.shields.io/github/last-commit/cemac/LIFD_ENV_ML_NOTEBOOKS.svg)](https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS/commits/master) [![GitHub All Releases](https://img.shields.io/github/downloads/cemac/LIFD_ENV_ML_NOTEBOOKS/total.svg)](https://github.com/cemac/LIFD_ENV_ML_NOTEBOOKS/releases) ![GitHub](https://img.shields.io/github/license/cemac/LIFD_ENV_ML_NOTEBOOKS.svg)[![DOI](https://zenodo.org/badge/366734586.svg)](https://zenodo.org/badge/latestdoi/366734586)




[![Twitter Follow](https://img.shields.io/twitter/follow/FluidsLeeds.svg?style=social&label=Follow)](https://twitter.com/FluidsLeeds)

Leeds Institute for Fluid Dynamics (LIFD) has teamed up with the Centre for Environmental Modelling and Computation (CEMAC) team to create Jupyter notebook tutorials on the following topics.

1. [PINNS](#Physics-Informed-Neural-Networks)
2. [Image Seg](#Image-Segmentation)
3. [AE](#Auto-Encoders)
4. [Data driven](#Data-driven-models)
5. [GP](#Gaussian-Processes)

These notebooks are accompanied by taught lectures, however they should also function as standalone tutorials.

## How to Run

These notebooks can run with the resources provided and the Anaconda environment setup. If you are familiar with Anaconda, Jupyter notebooks and GitHub then simply clone this repository and run it within your Jupyter notebook setup. Otherwise, please read the [how to run](howtorun.md) guide. These are designed to run on Leeds linux GPU work stations although can work colab or other GPU enabled platforms, where run times on a single GPU are deemed unacceptable links to pretrained models are provided.

# Physics-Informed Neural Networks

### [1D Heat Equation and Navier Stokes Equation](https://github.com/cemac/LIFD_Torch_PINNS)

Recent developments in machine learning have gone hand in hand with a large growth in available data and computational resources. However, often when analysing complex physical systems, the cost of data acquisition can be prohibitively large. In this small data regime, the usual machine learning techniques lack robustness and do not guarantee convergence.

Fortunately, we do not need to rely exclusively on data when we have prior knowledge about the system at hand. For example, in a fluid flow system, we know that the observational measurements should obey the Navier-Stokes equations, and so we can use this knowledge to augment the limited data we have available. This is the principle behind physics-informed neural networks (PINNs).

These notebooks illustrate using PINNs to explore the 1D heat equation and Navier Stokes Equation.  

![](https://raw.githubusercontent.com/cemac/LIFD_Physics_Informed_Neural_Networks/main/PINNs_1DHeatEquationExample_files/PINNs_1DHeatEquationExample_49_1.png)

![](https://raw.githubusercontent.com/cemac/LIFD_Physics_Informed_Neural_Networks/main/PINNs_NavierStokes_example_files/PINNs_NavierStokes_example_53_2.png)

In the Navier Stokes example notebook, sparse velocity data points (blue dots) are used to infer fluid flow patterns in the wake of a cylinder and unknown velocity and pressure fields are predicted using only a discrete set of measurements of a concentration field c(t,x,y).

These examples are based on work from the following two papers:
* M. Raissi, P. Peridakis, G. Karniadakis, Physics Informed Deep Learning (Part II): Data-driven Discovery of Nonlinear Partial Differential Equations, 2017
* M. Raissi, A. Yazdani, G. Karniadakis, Hidden Fluid Mechanics: A Navier-Stokes Informed Deep Learning Framework for Assimilating Flow Visualization Data, 2018

# Image Segmentation

### [Image Segmentation](https://github.com/cemac/LIFD_ImageSegmentation)

Image segmentation models are designed to tackle the problem of partitioning an image into meaningful segments or regions, each corresponding to different objects or parts of objects within the image. This process is crucial in various applications such as medical imaging, where it helps in identifying and isolating different anatomical structures (e.g. organs or tumours), or in autonomous driving, where it can aid in recognising and distinguishing between pedestrians, vehicles, and road signs. More recently, segmentation models are being applied to weather and climate forecasting applications, where their ability to identify structures in image data makes them ideally suited.

This Jupyter notebook demonstrates how artificial neural networks (ANNs) can be applied to image segmentation problems. We present a simple application to self-driving cars, where we train a U-Net segmentation model to identify important features in dashcam footage, as well as a more complicated example, based on the work of Coney et al. (2023), identifying and characterising trapped lee waves over the UK.

![](assets/qj4592-fig-0008-m.jpg)
*Figure from Coney et al. (2024)*

References:

* Ronneberger, O., Fischer, P., Brox, T. (2015). U-Net: Convolutional Networks for Biomedical Image Segmentation. In: Navab, N., Hornegger, J., Wells, W., Frangi, A. (eds) Medical Image Computing and Computer-Assisted Intervention – MICCAI 2015. MICCAI 2015. Lecture Notes in Computer Science(), vol 9351. Springer, Cham. [https://doi.org/10.1007/978-3-319-24574-4_28](https://doi.org/10.1007/978-3-319-24574-4_28)
*  Coney, J., Denby, L., Ross, A.N., Wang, H., Vosper, S., van Niekerk, A., et al. (2024) Identifying and characterising trapped lee waves using deep learning techniques. Quarterly Journal of the Royal Meteorological Society, 150(758), 213–231. Available from: [https://doi.org/10.1002/qj.4592](https://doi.org/10.1002/qj.4592)
  
# AutoEncoders

[AutoEncoders](https://github.com/cemac/LIFD_TorchAutoEncoders)

*to be filled*

AutoEncoders are unsupervised learning technique that performs data encoding and decoding using feed forward neural networks made of two components:

* **Encoder** translates input data into lower dimensional space. (lower dimensional encoding is referred to as the latent space representation) 	 

* **Decoder** tries to reconstruct the original 	data from the lower dimensional data 	 

References:

# Data Driven Models

*coming soon*

# Gauassian Processes

*comming soon*


# Licence information #

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">LIFD_CDT_NOTEBOOKS</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="http://cemac.leeds.ac.uk/" property="cc:attributionName" rel="cc:attributionURL">CEMAC</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/4.0/">Creative Commons Attribution 4.0 International License</a>.

## Acknowledgements
