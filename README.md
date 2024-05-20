Pretraining Deep Ultrasound Image Diagnosis Model through Video Contrastive Representation Learning.

#Abstract: Most deep neural networks (DNNs) based ultrasound (US) medical image analysis models use pretrained backbones (e.g., ImageNet) for better model generalization. However, the domain gap between natural and medical images causes an inevitable performance bottleneck. It contains over 23,000 images from four US video sub-datasets. To learn robust features from US-4, we propose an US semi-supervised contrastive learning method, named USCL, for pretraining. In order to avoid high similarities between negative pairs as well as mine abundant visual features from limited US videos, USCL adopts a sample pair generation method to enrich the feature involved in a single step of contrastive optimization. Extensive experiments on several downstream tasks show the superiority of USCL pretraining against ImageNet pretraining and other state-of-the-art (SOTA) pretraining approaches. In particular, USCL pretrained backbone achieves fine-tuning accuracy of over 94% on POCUS dataset, which is 10% higher than 84% of the ImageNet pretrained model. The constructed US-4 dataset and source codes of this work will be made public.




### Quick Start

#### Fine-tune with Pretrained Model
1. Pick a model and its config file, for example, `config.yaml`
2. Download the model `best_model.pth`
3. Download the 5 fold cross validation [POCUS](https://drive.google.com/file/d/111lHpStoY_gYMhCQ-Yt95AreDx0G7-2R/view?usp=sharing) dataset
4. Run the demo with
```
python eval_pretrained_model.py
```

Our pretrained ResNet-18 model on US-4 dataset can be downloaded as following:

Name | epochs | Project head | Classifier | Accuracy | download
---  |:---------:|:---------:|:---------:|:---------:|:---:
ResNet-18 | 300 | Yes | Yes | 94.19 | [model](https://drive.google.com/file/d/1ODH2oeZxZdblmEW725AuZYA51AT9QJH2/view?usp=sharing)


This repository reports the fine-tuning accuracy (%) on [POCUS](https://arxiv.org/abs/2004.12084) dataset.


#### Train Your Own Model
1. Download the Butterfly ([Baidu pan](https://pan.baidu.com/s/1tQtDzoditkTft3LMeDfGqw) Pwd:butt, [Google drive](https://drive.google.com/file/d/1zefZInevopumI-VdX6r7Bj-6pj_WILrr/view?usp=sharing)) dataset 
2. Train the USCL model with
```
python run.py
```


#### Environment
The code is developed with an Intel Xeon Silver 4210R CPU @ 2.4GHz and a single Nvidia Tesla V100 GPU.

The install script has been tested on an Ubuntu 18.04 system.

:cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud::cloud:

### License

Licensed under an MIT license.


Enjoy!
