<div align="center">
  
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoPiML.png" alt="drawing" width="314.15926"/>

**An integrated Python toolbox for interpretable machine learning** 

</div>

<div>

  ---

**March 30, 2025 by Dr. Agus Sudjianto**: **Farewell PiML, Hello MoDeVa!**

After three impactful years of empowering model developers and validators, we’re thrilled to introduce the next evolution: MoDeVa – MOdel DEvelopment & VAlidation.

MoDeVa builds on the success of PiML, taking transparency, interpretability, and robustness in machine learning to a whole new level. Whether you’re in a high-stakes regulatory setting or exploring cutting-edge model architectures, MoDeVa is built to support your journey.

Why MoDeVa?

 •	Next-Gen Models: Interpretable ML models like Boosted Trees, Mixture of Experts, and Neural Trees—built for confident decision-making.

 •	Model Hacking Redefined: Tools to uncover failure modes, analyze robustness, reliability and resilience. 

 •	Interactive Statistical Visualizations: Bring models to life with dynamic graphs that go beyond static charts.

 •	Seamless Validation: Effortlessly validate external black-box models using flexible wrappers.

Check it out here: https://modeva.ai/

--- 

<div align="center">

  `pip install PiML`
  
🎄 **Dec 1, 2023:**  V0.6.0 is released with enhanced data handling and model analytics.

:rocket: **May 4, 2023:**  V0.5.0 is released together with PiML user guide.

:rocket: **October 31, 2022:**  V0.4.0 is released with enriched models and enhanced diagnostics.

:rocket: **July 26, 2022:**  V0.3.0 is released with classic statistical models.

:rocket: **June 26, 2022:** V0.2.0 is released with high-code APIs.

:loudspeaker: **May 4, 2022:**  V0.1.0 is launched with low-code UI/UX.
</div>

PiML (or π-ML, /ˈpaɪ·ˈem·ˈel/) is a new Python toolbox for interpretable machine learning model development and validation. Through low-code interface and high-code APIs, PiML supports a growing list of inherently interpretable ML models:

1. **GLM**: Linear/Logistic Regression with L1 ∨ L2 Regularization
2. **GAM**: Generalized Additive Models using B-splines
3. **Tree**: Decision Tree for Classification and Regression
4. **FIGS**: Fast Interpretable Greedy-Tree Sums (Tan, et al. 2022)
5. **XGB1**: Extreme Gradient Boosted Trees of Depth 1, with optimal binning (Chen and Guestrin, 2016; Navas-Palencia, 2020)
6. **XGB2**: Extreme Gradient Boosted Trees of Depth 2, with effect purification (Chen and Guestrin, 2016; Lengerich, et al. 2020)
7. **EBM**: Explainable Boosting Machine (Nori, et al. 2019; Lou, et al. 2013)
8. **GAMI-Net**: Generalized Additive Model with Structured Interactions (Yang, Zhang and Sudjianto, 2021)
9. **ReLU-DNN**: Deep ReLU Networks using Aletheia Unwrapper and Sparsification (Sudjianto, et al. 2020)

PiML also works for arbitrary supervised ML models under regression and binary classification settings. It supports a whole spectrum of outcome testing, including but not limited to the following:

1. **Accuracy**: popular metrics like MSE, MAE for regression tasks and ACC, AUC, Recall, Precision, F1-score for binary classification tasks. 
2. **Explainability**: post-hoc global explainers (PFI, PDP, ALE) and local explainers (LIME, SHAP).
3. **Fairness**: disparity test and segmented analysis by integrating the solas-ai package.
4. **WeakSpot**: identification of weak regions with high residuals by slicing techniques.
5. **Overfit**: identification of overfitting regions according to train-test performance gap.
6. **Reliability**: assessment of prediction uncertainty by split conformal prediction techniques.
7. **Robustness**: evaluation of performance degradation under covariate noise perturbation.
8. **Resilience**: evaluation of performance degradation under different out-of-distribution scenarios.

[Installation](#Install) | [Examples](#Example) | [Usage](#Usage) | [Citations](#Cite)


## Installation<a name="Install"></a>  

```python
pip install PiML  
```

## Low-code Examples<a name="Example"></a>   
Click the ipynb links to run examples in Google Colab:  
1. BikeSharing data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_BikeSharing.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>  
2. CaliforniaHousing data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_CaliforniaHousing.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>  
3. TaiwanCredit data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_TaiwanCredit.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
4. Fairness_SimuStudy1 data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_Fairness_SimuStudy1.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
5. Fairness_SimuStudy2 data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_Fairness_SimuStudy2.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
6. Upload custom data in two ways: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_CustomDataLoad_Two_Ways.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>    
7. Deal with external models: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_ExternalModels.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>    

Begin your own PiML journey with <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/PiML%20Low-code%20Example%20Run.ipynb">this demo notebook</a>. 


## High-code Examples<a name="Example"></a>   
The same examples can also be run by high-code APIs:  
1. BikeSharing data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_BikeSharing_HighCode.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>  
2. CaliforniaHousing data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_CaliforniaHousing_HighCode.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>  
3. TaiwanCredit data: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_TaiwanCredit_HighCode.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
4. Model saving: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_ModelSaving.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
5. Results return: <a style="text-laign: 'center'" target="_blank" href="https://colab.research.google.com/github/SelfExplainML/PiML-Toolbox/blob/main/examples/Example_ResultsReturn.ipynb"><img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/LogoColab.png" width="20">  ipynb</a>   
## Low-code Usage on Google Colab<a name="Usage"></a>  

### Stage 1:  Initialize an experiment, Load and Prepare data

```python
from piml import Experiment
exp = Experiment()
```

```python
exp.data_loader()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/data_loader.png">

```python
exp.data_summary()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/data_summary.png">

```python
exp.data_prepare()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/data_prepare.png">

```python
exp.data_quality()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/data_quality.png">

```python
exp.feature_select()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/feature_select.png">

```python
exp.eda()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/data_eda.png">

### Stage 2:  Train intepretable models
```python
exp.model_train()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_train.png">

### Stage 3. Explain and Interpret
```python
exp.model_explain()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_explain.png">

```python
exp.model_interpret() 
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_interpret.png">

### Stage 4. Diagnose and Compare
```python
exp.model_diagnose()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_diagnose.png">

```python
exp.model_compare()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_compare.png">

```python
exp.model_fairness()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_fairness.png">

```python
exp.model_fairness_compare()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_fairness_compare.png">


## Arbitrary Black-Box Modeling
For example, train a complex LightGBM with depth 7 and register it to the experiment: 

```python
from lightgbm import LGBMClassifier
exp.model_train(LGBMClassifier(max_depth=7), name='LGBM-7')
```

Then, compare it to inherently interpretable models (e.g. XGB2 and GAMI-Net): 
```python
exp.model_compare()
```
<img src="https://github.com/SelfExplainML/PiML-Toolbox/blob/main/examples/results/model_compare_2.png">



## Citations<a name="Cite"></a>  

<details open>
  <summary><strong>PiML, ReLU-DNN Aletheia and GAMI-Net</strong></summary><hr/>

  "PiML Toolbox for Interpretable Machine Learning Model Development and Diagnostics" (A. Sudjianto, A. Zhang, Z. Yang, Y. Su and N. Zeng, 2023) <a href="https://arxiv.org/abs/2305.04214">arXiv link</a>  

  ```latex
  @article{sudjianto2023piml,
  title={PiML Toolbox for Interpretable Machine Learning Model Development and Diagnostics},
  author={Sudjianto, Agus and Zhang, Aijun and Yang, Zebin and Su, Yu and Zeng, Ningzhou},
  year={2023}
  }
  ```
  
  
  "Designing Inherently Interpretable Machine Learning Models" (A. Sudjianto and A. Zhang, 2021)  <a href="https://arxiv.org/abs/2111.01743">arXiv link</a>  
  
  ```latex
  @article{sudjianto2021designing,
  title={Designing Inherently Interpretable Machine Learning Models},
  author={Sudjianto, Agus and Zhang, Aijun},
  journal={arXiv preprint:2111.01743},
  year={2021}
  }
  ```

  "Unwrapping The Black Box of Deep ReLU Networks: Interpretability, Diagnostics, and Simplification" (A. Sudjianto, W. Knauth, R. Singh, Z. Yang and A. Zhang, 2020) <a href="https://arxiv.org/abs/2011.04041">arXiv link</a>  
  
  ```latex
  @article{sudjianto2020unwrapping,
  title={Unwrapping the black box of deep ReLU networks: interpretability, diagnostics, and simplification},
  author={Sudjianto, Agus and Knauth, William and Singh, Rahul and Yang, Zebin and Zhang, Aijun},
  journal={arXiv preprint:2011.04041},
  year={2020}
  }
  ```

  "GAMI-Net: An Explainable Neural Network based on Generalized Additive Models with Structured Interactions" (Z. Yang, A. Zhang, and A. Sudjianto, 2021) <a href="https://arxiv.org/abs/2003.07132">arXiv link</a>  

  ```latex
  @article{yang2021gami,
  title={GAMI-Net: An explainable neural network based on generalized additive models with structured interactions},
  author={Yang, Zebin and Zhang, Aijun and Sudjianto, Agus},
  journal={Pattern Recognition},
  volume={120},
  pages={108192},
  year={2021}
  }
  ```
</details>  


<details open>
  <summary><strong>Other Interpretable ML Models</strong></summary><hr/>
  
  "Fast Interpretable Greedy-Tree Sums (FIGS)" (Tan, Y.S., Singh, C., Nasseri, K., Agarwal, A. and Yu, B., 2022)  
  
  ```latex
  @article{tan2022fast,
  title={Fast interpretable greedy-tree sums (FIGS)},
  author={Tan, Yan Shuo and Singh, Chandan and Nasseri, Keyan and Agarwal, Abhineet and Yu, Bin},
  journal={arXiv preprint arXiv:2201.11931},
  year={2022}
  }
  ```

  "Accurate intelligible models with pairwise interactions" (Y. Lou, R. Caruana, J. Gehrke, and G. Hooker, 2013)   
  
  ```latex
  @inproceedings{lou2013accurate,
  title={Accurate intelligible models with pairwise interactions},
  author={Lou, Yin and Caruana, Rich and Gehrke, Johannes and Hooker, Giles},
  booktitle={Proceedings of the 19th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining},
  pages={623--631},
  year={2013},
  organization={ACM}
  }  
  ```
  
  "Purifying Interaction Effects with the Functional ANOVA: An Efficient Algorithm for Recovering Identifiable Additive Models" (Lengerich, B., Tan, S., Chang, C.H., Hooker, G. and Caruana, R., 2020)  
  
  ```latex
  @inproceedings{lengerich2020purifying,
  title={Purifying interaction effects with the functional anova: An efficient algorithm for recovering identifiable additive models},
  author={Lengerich, Benjamin and Tan, Sarah and Chang, Chun-Hao and Hooker, Giles and Caruana, Rich},
  booktitle={International Conference on Artificial Intelligence and Statistics},
  pages={2402--2412},
  year={2020},
  organization={PMLR}
  }
  ```
  
  
  "InterpretML: A Unified Framework for Machine Learning Interpretability" (H. Nori, S. Jenkins, P. Koch, and R. Caruana, 2019)  
  
  ```latex
  @article{nori2019interpretml,
  title={InterpretML: A Unified Framework for Machine Learning Interpretability},
  author={Nori, Harsha and Jenkins, Samuel and Koch, Paul and Caruana, Rich},
  journal={arXiv preprint:1909.09223},
  year={2019}
  }
  ```  
</details>
