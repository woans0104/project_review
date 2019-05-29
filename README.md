# project_review

---------------------------------------

### 01. coordconv solution

---------------------------------------

https://arxiv.org/abs/1807.03247



#### idea 


![Alt text](/img/coord1.png)
![Alt text](/img/coord2.png)



---------------------------------------

### 01-1. AUTOMATED SEGMENTATION OF PULMONARY LOBES USING

---------------------------------------

https://arxiv.org/abs/1904.09106


#### task  
* propose an automated segmentation of pulmonary lobes using coordination-guided deep neural networks from chest CT images

![Alt text](/img/coord4.png)


#### dataset

![Alt text](/img/coord3.png)

* 343 chest CT scans
* size : 256×256×128
* target : five target lobar classes


#### model

![Alt text](/img/vnet.png)


* fully end-to-end 3D deep learning approach
* unet 구조와 유사한데 큰 차이점은 skip connection 사용
* coordconv 적용 : last transition in the decoding path


#### evaluation

![Alt text](/img/coord5.png)



---------------------------------------

### 02. Focal loss

---------------------------------------

#### idea 


![Alt text](/img/focalloss.png)

* 분류 잘못 , pt 작을때 : factor는 1에 가까운 값을 가지며 loss에 거의 영향 없음
* 반면 pt 1이면 factor가 0에 가까워지며 잘 분류된 샘플에 대해서 loss의 가중치가 작아짐




---------------------------------------

### 02-1. A NOVEL FOCAL TVERSKY LOSS FUNCTION WITH IMPROVED ATTENTION U-NET FOR LESION SEGMENTATION

---------------------------------------




















