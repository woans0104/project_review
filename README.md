


# project_review

---------------------------------------

### 01. coordconv solution

---------------------------------------

https://arxiv.org/abs/1807.03247



#### idea 


![Alt text](/img/coord1.png)</center>



---------------------------------------

### 01-1. AUTOMATED SEGMENTATION OF PULMONARY LOBES USING

---------------------------------------

https://arxiv.org/abs/1904.09106


#### task & contributions
* propose an automated segmentation of pulmonary lobes using coordination-guided deep neural networks from chest CT images

![Alt text](/img/coord4.png)</center>


#### dataset

![Alt text](/img/coord3.png)</center>

* 343 chest CT scans
* size : 256×256×128
* target : five target lobar classes


#### model

![Alt text](/img/vnet.png)</center>


* fully end-to-end 3D deep learning approach
* unet 구조와 유사한데 큰 차이점은 skip connection 사용
* coordconv 적용 : last transition in the decoding path


#### evaluation

![Alt text](/img/coord5.png)</center>



---------------------------------------

### 02. Focal loss

---------------------------------------

#### idea 


![Alt text](/img/focalloss.png)</center>

* 분류 잘못 , pt 작을때 : factor는 1에 가까운 값을 가지며 loss에 거의 영향 없음
* 반면 pt 1이면 factor가 0에 가까워지며 잘 분류된 샘플에 대해서 loss의 가중치가 작아짐




---------------------------------------

### 02-1. A NOVEL FOCAL TVERSKY LOSS FUNCTION WITH IMPROVED ATTENTION U-NET FOR LESION SEGMENTATION

---------------------------------------

https://arxiv.org/abs/1810.07842


#### task & contributions

* a novel focal Tversky loss function for highly imbalanced data  and small ROI segmentation
* a deeply supervised attention U-Net  improved with a multiscaled input image pyramid for better intermediate feature representations.


#### dataset
	
  * 1.Breast Ultrasound Lesions 2017 dataset B (BUS)
		* 163 ultrasound images of breast lesions from different women
		* average image size is 760 x 570 pixels(resampled to 128 x 128 pixels)
		* a 75-25 train-test split

  * 2.ISIC 2018 skin lesion dataset
		* 2,594 RGB images of skin lesion
		* image size of 2166 x 3188 pixels(resampled to 192 x 256 pixels)
    		* 75-25 train-test split
    
    
#### focal Tversky loss function (FTL)

* The Tversky index is adapted to a loss function (TL)
  ![Alt text](/img/focalloss1.png)</center>
  
	* pic : 병이 잇는 클래스 확률
	* pic-: 병없는 클래스 확률
	* a,b는 하이퍼파라미터

  ![Alt text](/img/focalloss5.PNG)

* focal Tversky loss function (FTL)
  
  ![Alt text](/img/focalloss2.png)
  

  
  
#### model

<center><img src="/img/attunet.PNG" width="300" height="300"></center>
<center><img src="/img/attgate.PNG" width="300" height="300"></center>

  
  
 
#### evaluation

<center><img src="/img/focalloss4.PNG" width="900" height="900"></center>














