# Deep Propensity Network - Sparse Autoencoder (DPN-SA) - Implementation for real world Jobs dataset

## Description
Official repository of [Deep Propensity Network - Sparse Autoencoder (DPN-SA)](https://academic.oup.com/jamia/advance-article/doi/10.1093/jamia/ocaa346/6139936?guestAccessKey=6d8842f9-78b2-4178-912e-a76faf52c3bd#supplementary-data), Journal of the American Medical Informatics Association.
## Citation

    @article{10.1093/jamia/ocaa346,
            author = {Ghosh, Shantanu and Bian, Jiang and Guo, Yi and Prosperi, Mattia},
            title = "{Deep propensity network using a sparse autoencoder for estimation of treatment effects}",
            journal = {Journal of the American Medical Informatics Association},
            year = {2021},
            month = {02},
            abstract = "{Drawing causal estimates from observational data is problematic, because datasets often contain underlying bias (eg, discrimination in treatment assignment). To examine causal effects, it is important to evaluate what-if scenarios—the so-called “counterfactuals.” We propose a novel deep learning architecture for propensity score matching and counterfactual prediction—the deep propensity network using a sparse autoencoder (DPN-SA)—to tackle the problems of high dimensionality, nonlinear/nonparallel treatment assignment, and residual confounding when estimating treatment effects.We used 2 randomized prospective datasets, a semisynthetic one with nonlinear/nonparallel treatment selection bias and simulated counterfactual outcomes from the Infant Health and Development Program and a real-world dataset from the LaLonde’s employment training program. We compared different configurations of the DPN-SA against logistic regression and LASSO as well as deep counterfactual networks with propensity dropout (DCN-PD). Models’ performances were assessed in terms of average treatment effects, mean squared error in precision on effect’s heterogeneity, and average treatment effect on the treated, over multiple training/test runs.The DPN-SA outperformed logistic regression and LASSO by 36\\%–63\\%, and DCN-PD by 6\\%–10\\% across all datasets. All deep learning architectures yielded average treatment effects close to the true ones with low variance. Results were also robust to noise-injection and addition of correlated variables. Code is publicly available at https://github.com/Shantanu48114860/DPN-SA.Deep sparse autoencoders are particularly suited for treatment effect estimation studies using electronic health records because they can handle high-dimensional covariate sets, large sample sizes, and complex heterogeneity in treatment assignments.}",
            issn = {1527-974X},
            doi = {10.1093/jamia/ocaa346},
            url = {https://doi.org/10.1093/jamia/ocaa346},
            note = {ocaa346},
            eprint = {https://academic.oup.com/jamia/advance-article-pdf/doi/10.1093/jamia/ocaa346/36288828/ocaa346.pdf},
        }



## Objective
Drawing causal estimates from observational data is problematic, because datasets often contain underlying bias, e.g., discrimination in treatment assignment. To examine causal effects, it is important to evaluate what-if scenarios—the so-called counterfactuals. We propose a novel deep learning architecture for propensity score matching (PSM) and counterfactual prediction—the deep propensity network using a sparse autoencoder (DPN-SA)—to tackle the problems of high dimensionality, nonlinear/nonparallel treatment assignment, and residual confounding when estimating treatment effects.

## Materials and methods
We used two randomized prospective datasets, a semi-synthetic one with nonlinear/nonparallel treatment selection bias and simulated counterfactual outcomes from the Infant Health and Development Program (IHDP), and a real-world dataset from the LaLonde’s employment training program. We compared different configurations of the DPN-SA against logistic regression and LASSO, as well as deep counterfactual networks with propensity dropout (DCN-PD). Models’ performance were assessed in terms of average treatment effects (ATE), mean squared error (MSE) in precision on effect’s heterogeneity, and average treatment effect on the treated (ATT), over multiple training/test runs.

## Jobs dataset
The original Jobs dataset will be found at the website:
https://www.fredjo.com/

## Results
The DPN-SA outperformed logistic regression and LASSO by 36-63%, and DCN-PD by 6-10% across all datasets. All deep learning architectures yielded ATE close to the true ones with low variance. Results were also robust to noise-injection and addition of correlated variables.

## Architecture
<img src="https://github.com/Shantanu48114860/DPN-SA/blob/master/Pic.png">

## Contributors
[Shantanu Ghosh](https://www.linkedin.com/in/shantanu-ghosh-b369783a/)

[Jiang Bian](http://jiangbian.me/)

[Yi Guo](https://hobi.med.ufl.edu/profile/guo-yi/)

[Mattia Prosperi](https://epidemiology.phhp.ufl.edu/profile/prosperi-mattia/)

## Requirements and setup
pytorch - 1.3.1 <br/>
numpy - 1.17.2 <br/>
pandas - 0.25.1 <br/>
scikit - 0.21.3 <br/>
matplotlib: 3.1.1 <br/>
python -  3.7.4 <br/>


## Keywords
causal AI, biomedical informatics, deep learning, multitask learning, sparse autoencoder


## Dependencies
[python 3.7.7](https://www.python.org/downloads/release/python-374/)

[pytorch 1.3.1](https://pytorch.org/get-started/previous-versions/)

Update the DCN Model path

## How to run
To reproduce the experiments mentioned in the paper for DCN-PD, Logistic regression, Logistic regression Lasso 
and all the SAE variants of 25-20-10- (greedy and end to end) for both the
original and synthetic dataset, type the following
command: 

<b>python3 main_propensity_dropout.py</b>

## Output
After the run, the outputs will be generated in the following location:

<b>[Jobs](https://github.com/Shantanu48114860/DPN-SA/tree/master/Jobs/MSE)</b>

Consolidated results will be available in textfile in /Details_original.txt and /Details_augmented.txt files.

The details of each run will be avalable in csv files in the following locations:

/MSE/Results_consolidated.csv

## Contact
beinghshantanu2406@gmail.com 

shantanughosh@ufl.edu

## License & copyright
© [DISL](https://epidemiology.phhp.ufl.edu/research/disl), University of Florida

Licensed under the [MIT License](LICENSE)
