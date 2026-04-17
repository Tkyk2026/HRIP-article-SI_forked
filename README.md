This page is forked from https://github.com/Article-HRIP/HRIP-article-SI. (Our old GitHub pages)
# HRIP-article-SI
This is the repository to share supporting information of python codes for reviewers. <br>
The models described in this repository can
- predict numerous polymer's refractive index at D line ($n_{D}$) from smaller-data-trained predictive model<br>
- provide specific structures optimized for  miltiple properties (e.g. $n_{D}$ and $\Delta\varepsilon_{HOMO-LUMO}$) via generative approach
# What we provide here
- codes
- data
- other nesisities (license etc. )

# Requirements for MOBO
- (We used different environment on Anaconda to make $n_{D}$ predictor. See repository of nd_predictor.)
* Python (>3.10)
* PyTorch==2.2.0+cu118
* Numpy==1.26.4
* DGL==2.4.0+cu118
* networkx==3.5
* rdkit==2025.9.3
* botorch==0.16.1
* statsmodels==0.14.5

# Quick start of our original $n_{D}$ predictor with Molecule generation through MOBO on Google Colab
1. Upload the jupyter notebook below on Google Colab<br>
`
MOBO_with_original_nD_predictor_and_GPU-assisted_DFT.ipynb
`
2. Connect to a session with GPU (T4 is enough)
3. Install requirements <br>

```python
!pip install -r requirements.txt
```

4. Place two pickle files of $n_{D}$ predictor on \content or directory where currently you are
5. Run the code from scratch
6. You will see generated molecules as SMILES (Simplified Molecular Input Line Entry System, )
7. Download result csv file if you need

## referenced codes
### referenced papers for molecule generation
* https://github.com/slab-it/FRATTVAE
### referenced documentation for bayesian optimization
* https://botorch.org/docs/tutorials/multi_objective_bo/
### referenced github repository for variance inflation factor (VIF)
* https://github.com/Apress/Practical-Explainable-AI-Using-Python

## referenced dataset
### training dataset
* https://github.com/KanHatakeyama/RefractiveIndexGPT/forpub2.csv
### test and validation dataset ->our original (see the paper for more details)

## DFT
* https://github.com/pyscf/gpu4pyscf
