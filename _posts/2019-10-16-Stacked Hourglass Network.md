---
layout: post
title:  “Stacked Hourglass Network”
date:   2019-10-16
comments: true
---

컨볼루션을 반복해서 수행하고 작아지는 size를 다시 디컨볼루션으로 키워가며 만들기 때문에 Hourglass(?)라 부른다.  

단순 deconv가 아니라 nn-upsampling을 했다. 여러 스케일 정보를 모두 취합하겠다는 의도.

Houglass Module을 여러번 반복하게 되면 정확도가 향상됨을 보임.

[!img](http://openresearch.ai/uploads/default/original/1X/00b5f6787fb30d6d23887fbe4f6a5b90e535e281.jpg)

[Refenrence]  
http://openresearch.ai/t/stacked-hourglass-networks-for-human-pose-estimation/68
