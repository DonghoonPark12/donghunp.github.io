---
title: Stacked Hourglass Networks
comments: true
categories: research
tags: object detection
---

컨볼루션을 반복해서 수행하고 작아지는 size를 다시 디컨볼루션으로 키워가며 만들기 때문에 Hourglass(?)라 부른다.  

본 네트워크로 FLIC, MPII 대회에서 우수한 성능을 보임.

단순 deconv가 아니라 nn-upsampling을 했다. 여러 스케일 정보를 모두 취합하겠다는 의도.

Houglass Module을 여러번 반복하게(Stacked) 되면 정확도가 향상됨을 보임.


<center><img src="/assets/191017_Stacked_HourGlass_Network/Hourglass.jpg" width="60%"></center>  
  
전체 네트워크 구조는 다음과 같고,
<center><img src="/assets/191017_Stacked_HourGlass_Network/Hourglass_network.png" width="60%"></center>  

각 블록은 Residual 모듈 형태이다. 모든 Residual 모듈의 Output Channel은 크기가 256이다.
<center><img src="/assets/191017_Stacked_HourGlass_Network/Rasidual_module.png" width="60%"></center>    

해당 네트워크로 모든 어려운 상황을 다 다룰 수는 없지만, Heavy Occulusion이나 다수의 사람이 근점하여 존재하는 상황(Multiple people in close proximity)에서 강인한 성능을 보였다는 것으로 마무리한다.  
  
  
휴먼 자세 예측(Human Pose Estimation)에서 17년도에 제안된 논문이지만, 본 논문에서 사용된 Hourglass Network 이후 AnchorFree Detection에서 사용되기 시작한다(CornerNet, ExtremeNet). 

[Refenrence]  
http://openresearch.ai/t/stacked-hourglass-networks-for-human-pose-estimation/68  
https://curt-park.github.io/2018-07-03/stacked-hourglass-networks-for-human-pose-estimation/
https://www.slideshare.net/yuhuang/anchor-free-object-detection-by-deep-learning

