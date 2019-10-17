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

![img](/assets/Hourglass.jpg)

휴먼 자세 예측(Human Pose Estimation)에서 17년도에 제안된 논문이지만, 이후 AnchorFree Detection에서 본 논문에서 사용된 Hourglass Network를
사용하기 시작하였다(CornerNet). 

[Refenrence]  
http://openresearch.ai/t/stacked-hourglass-networks-for-human-pose-estimation/68

