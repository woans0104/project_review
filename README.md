

# project_review

---------------------------------------

### 01. coordconv solution

---------------------------------------

https://arxiv.org/abs/1807.03247



#### idea 


![Alt text](/img/coord1.png)</center>





---------------------------------------

### 01-1. Automatic salt deposits segmentation: A deep learning approach

---------------------------------------
https://arxiv.org/abs/1812.01429

### task & contributions

* salt deposits segmentation problem in seismic image data

### dataset

<p align="left"><img src="/img/salt1.png" width="300" height="300"></p>

* Seismic reflection data
* size 101 × 101
* binary masks of salt deposits

### model

![Alt text](/img/salt2.png)

<p align="left"><img src="/img/salt3.png" width="300" height="300"></p>

---------------------------------------

### 01-2. AUTOMATED SEGMENTATION OF PULMONARY LOBES USING Coordination-Guided Deep Neural Networks

---------------------------------------

https://arxiv.org/abs/1904.09106


### task & contributions
* propose an automated segmentation of pulmonary lobes using coordination-guided deep neural networks from chest CT images

<p align="center"><img src="/img/coord4.png" width="300" height="300"><img src="/img/coord3.png" width="300" height="300"></p>


### dataset



* 343 chest CT scans
* size : 256×256×128
* target : five target lobar classes


### model

![Alt text](/img/vnet.png)




* fully end-to-end 3D deep learning approach
* unet 구조와 유사한데 큰 차이점은 skip connection 사용
* coordconv 적용 : last transition in the decoding path





### evaluation

![Alt text](/img/coord5.png)



---------------------------------------

### 02. Focal loss

---------------------------------------

### idea 


![Alt text](/img/focalloss.png)</center>

* pt가 클 경우 상대적으로 loss가 pt가 적을 때 보다 크게 감소
* 따라서 상대적으로 잘 분류되지 못한 cls에 집중함




---------------------------------------

### 02-1. A NOVEL FOCAL TVERSKY LOSS FUNCTION WITH IMPROVED ATTENTION U-NET FOR LESION SEGMENTATION

---------------------------------------

https://arxiv.org/abs/1810.07842


### task & contributions


* a novel focal Tversky loss function for highly imbalanced data  and small ROI segmentation
* a deeply supervised attention U-Net  improved with a multiscaled input image pyramid for better intermediate feature representations.



### dataset
	
	
* 1.Breast Ultrasound Lesions 2017 dataset B (BUS)
 * 163 ultrasound images of breast lesions from different women
 * average image size is 760 x 570 pixels(resampled to 128 x 128 pixels)
 * a 75-25 train-test split

* 2.ISIC 2018 skin lesion dataset
 * 2,594 RGB images of skin lesion
 * image size of 2166 x 3188 pixels(resampled to 192 x 256 pixels)
 * 75-25 train-test split

    
    
### focal Tversky loss function (FTL)


* The Tversky index is adapted to a loss function (TL)
 
 ![Alt text](/img/focalloss1.png)
 
  
	* pic : cls가 1인 pixel에 대한 확률값
	* pic-: cls가 0인 pixel에 대한 확률값
	* a,b는 하이퍼파라미터


  ![Alt text](/img/focalloss5.PNG)


* focal Tversky loss function (FTL)
  
  ![Alt text](/img/focalloss2.png)
  

    
### model

<p align="center"><img src="/img/attunet.PNG" width="800" height="500"></p>

* attention gate 
* multi scale : avg pooling을 이용해 각 stage의 input으로 추가로 넣어줌
* deep supervision 


<p align="center"><img src="/img/attgate.PNG" width="500" height="300"></p>

* g : 이전 stgage decoder로 부터의 featuremap
* x : 대응되는 stage encoder로 부터의 featuremap
* 0~1 사이의 값을 뱉어 주어서 x와 곱함
 
### evaluation

<p align="center"><img src="/img/focalloss4.PNG" width="800" height="500"></p>










