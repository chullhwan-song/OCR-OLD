# OCR
## Recognition - SOTA Performance (only unconstrained lexicon-free)
#### Evaluation 
* TTM : Total-Text (multi-oriented) 
* TTC : Total-Text (curved)
* 학습셋
  * SK : Synth90K
  * ST : SynthText
 
| Paper | year | SVT | IIIT5k | IC03 | IC13 | SVTP | CUTE80 | IC15 | TTM | TTC | 비고 | 학습셋 | 
| :--- | :---: | :---: |:---: |:---:|:---: |:---:|:---:|:---:|:---:|:---:|:--- |:--- |
| SOTA| | **91.5** | **94.0** | **96.7** | **95.8**| **86.6** | **88.5** | **79.4** | **76.3** | **66.7** |
| [1] CRNN     | 15.07 | 80.8 |  78.2 | 89.4 |  86.7 | 66.8 | 54.9 | | | | base:CRNN | SK| 
| [10] RARE    | 16.x | 81.9 | 81.9 |  90.1 | 88.6 | 71.8 |  | | | | Rectification | SK| 
| [9] STAR-Net | 16.x | 83.6 | 83.3 | 89.9 | 89.1  | 73.5  |  | | | | Rectification | SK| 
| MY | 17.x | 79.91 | 84.26 | 89.5 | 90.82 | | | | | | Rectification | SK |
| [3] | 18.x | 87.1 | 89.4 | 94.7 | 94.0 | 73.9 | 62.5 | | | | GAN |  
| [4] ASTER | 18.x | 89.5 | 93.4 | 94.5 | 91.8 | 78.5 | 79.5 | 76.1 | | | Rectification |
| [5] AON | 18.03 | 82.8 | 87.0 | 91.5 |  | 73.0 | 76.8 | 68.2 | | |  |
| [6] | 18.05 | 87.5| 88.3 | 94.6 | 94.4  | | | 73.9 |
| [2] | 18.12 |  88.6 | **94.0** | 93.6 | 93.2 |  80.6 | **88.5** | 77.1 | **76.3** | **66.7** |   | SK+ST |
| [7] ESIR| 18.12| 90.2 | 93.3 | | 91.3 | 79.6 |  83.3  | 76.9 | | | Rectification | SK+ST |
| [8] MORAN V1 | 19.01|  88.3 | 91.2  | 95.0 |  92.4 | 76.1 | 77.4 | | | | Rectification | SK+ST |
| [8] MORAN V2 | 19.01|  88.3 | 93.4  | 94.2 |  93.2 | 79.7 | 81.9 | | | | Rectification | SK+ST |
| [11] NRTR | 19.10|**91.5**| 90.1 | 95.4 |  **95.8** | **86.6** | 80.9 | **79.4** | | | Transformer |  |
| [12] SATRN | 19.10| 91.3 | 92.8 | **96.7** |  94.1 | 86.5 | 87.8 | 79.0 | | | Transformer |  |

* MY : MY implementation(2017), CRNN(modified networks)+jointly(CTC+Attention)+Rectification
* [1] An End-to-End Trainable Neural Network for Image-based Sequence Recognition and Its Application to Scene Text Recognition
* [2] Recurrent Calibration Network for Irregular Text Recognition
* [3] Synthetically Supervised Feature Learning for Scene Text Recognition : [[paper]](http://openaccess.thecvf.com/content_ECCV_2018/html/Yang_Liu_Synthetically_Supervised_Feature_ECCV_2018_paper.html)[[review]](https://github.com/chullhwan-song/Reading-Paper/issues/60)
* [4] ASTER: An Attentional Scene Text Recognizer with Flexible Rectification # Rectification
* [5] Arbitrarily-oriented text recognition
* [6] Edit Probability for Scene Text Recognition
* [7] ESIR: End-to-end Scene Text Recognition via Iterative Rectification # Rectification
* [8] MORAN: A Multi-Object Rectified Attention Network for Scene Text Recognition # Rectification
* [9] STAR-Net: A SpaTial Attention Residue Network for Scene Text Recognition
* [10] RARE: Robust Scene Text Recognition with Automatic Rectification
* [11] NRTR: A No-Recurrence Sequence-to-Sequence Model For Scene Text Recognition # self attention
* [12] SATRN: On Recognizing Texts of Arbitrary Shapes with 2D Self-attention # self attention

## Detection
#### Papers's training Information : [링크](https://github.com/chullhwan-song/OCR/issues/1)
#### Evaluation
* R : Recall
* P : Precision
* F : F-measure
* MS : MSRA-TD50
* TT : Total-Text
* CT : CTW1500 

| Paper | year |IC13-R |IC13-P |IC13-F| IC15-R |IC15-P |IC15-F|MS-R|MS-P|MS-F|TT-R |TT-P |TT-F| CT-R |CT-P |CT-F| 
|  :---  | :---: | :---: | :---: | :---: |:---: |:---: | :---:  |:---: |:---: | :---:  | :---:  |:---: |:---: | :---: |:---: |:---:  | 
| SOTA| | **95.0** |**97.4**  |**0.925** |  **91.8**| **0.9185**| **0.8984**  | **91.5**|**88.2**| **81.7**| **82.8** | **87.6** | **82.9** | **81.1** |  **86.0** | **80.7** |
| [5]      | 16.04 |0.78 | 0.88 | 0.83 |0.43 | 0.71 |  0.54 |0.67 | 0.83|  0.74 | 
| [1] EAST | 17.07 |87.53 |93.34  | 90.34 | 78.33 | 83.27 |  80.78 | 67.43 |87.28| 76.08 | 36.2 | 50.0|  42.0  | 49.1 | 78.7  | 60.4 |
| [7] | 17.09 |0.86  | 0.88 | 0.87  | 0.73 | 0.80 |  0.77 |
| [3] PixelLink| 18.01 |88.6 | 87.5 |  88.1 | 82.0 | 85.5| 83.7 | 83.0 | 73.2    | 77.8 | 54.41 | 59.89 |  57.02 |
| [8] FOTS | 18.01 |      |      | **0.925** | 0.8792| **0.9185**| **0.8984** |
| [9]      | 18.07 | 87.1 |91.5 |89.2| | | |77.4 |  83.0 | 80.1 | 
| [10]     | 18.08 | **95.0**|88.6 | 91.7 | 91.6 | 81.0|86.0 | | | | 69.0 | 55.0 | 61.3 |
| [6]      |18.11  |90.5 |93.8  |92.1 |  85.8  | 88.7 | 87.2 | | | | **82.8** | 83.0 |  **82.9** | 
| [4] MSR  | 19.01 |88.5 | 91.8 | 90.1 | | | | 76.7 | 87.4 | 81.7 |73.0 | 85.2 | 78.6 |  77.8 |  83.8 | **80.7** |
| [2]      | 19.01 |85.94| 93.18| 89.41 | 79.2 | 86.1 | 82.5 |75.26  | 85.88 | 80.21 | 
| [11]CRAFT| 19.04 | 93.1 |  **97.4** |  | 84.3     | 89.8 | | 78.2 | **88.2** | | 79.9 | **87.6** | | **81.1** | **86.0** |  | 
| [12]     |        |     |           |  | **91.8** | 83.2 | 87.3 | **91.5** |  79.2 |  **84.9** |

* [1] EAST: An Efficient and Accurate Scene Text Detector : [[paper]](https://arxiv.org/abs/1704.03155)[[review]](https://github.com/chullhwan-song/Reading-Paper/issues/73) :  # U-Net
* [2] Detecting Text in the Wild with Deep Character Embedding Network
* [3] PixelLink: Detecting Scene Text via Instance Segmentation : [[paper]](https://arxiv.org/abs/1801.01315)[[review]](https://github.com/chullhwan-song/Reading-Paper/issues/71) : # U-Net
* [4] MSR: Multi-Scale Shape Regression for Scene Text Detection
* [5] Multi-Oriented Text Detection with Fully Convolutional Networks
* [6] Scene Text Detection with Supervised Pyramid Context Network : [[paper]](https://arxiv.org/abs/1811.08605)[[review]](https://github.com/chullhwan-song/Reading-Paper/issues/75): #MASK R-CNN #Multi-Scale
* [7] Single Shot Text Detector with Regional Attention : #SSD
* [8] FOTS: Fast Oriented Text Spotting with a Unified Network : [[paper]](https://arxiv.org/abs/1801.01671)[[review]](https://github.com/chullhwan-song/Reading-Paper/issues/107) 
* [9] Accurate Scene Text Detection through Border Semantics Awareness and Bootstrapping
* [10] Mask TextSpotter: An End-to-End Trainable Neural Network for Spotting Text with Arbitrary Shapes
* [11] CRAFT: Character Region Awareness for Text Detection, # F-Measure대신에 H-Mean으로 표현했다.같은것인지 




