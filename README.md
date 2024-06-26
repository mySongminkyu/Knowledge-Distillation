# Knowledge-Distillation
Distilling the Knowledge in a Neural Network


- Abstract
  - 기존의 machine learning algorithm의 성능을 향상시키는 간단한 방법은 ensemble을 이용하는 것이지만, 이는 번거로우며 cost가 많이 발생한다.
    또한 individual model이 large neural net일 경우 배포에 어려움이 있다. 다른 연구에서 ensemble에 있는 knowledge를 배포하기 훨씬 쉬운 single model로 압축하는 것이 가능하다는 것을 보여줬으며,
    본 논문에서는 다른 압축 기술을 사용하여 이를 더욱 개발하였다.

    이는 MNIST dataset에서 향상된 결과를 얻었으며, model ensemble에 있는 knowledge를 single model로 distillation하여 많이 사용되는 상용 시스템의 acoustic model을 크게 개선할 수 있음을 보였다.
    또한 하나 이상의 full model과 full model이 혼동하는 세분화된 class를 구별하는 방법을 배우는 많은 experts model로 구성된 새로운 유형의 ensemble을 소개한다. experts가 혼합된 것과 달리 이런 experts
    model은 빠르고 병렬적으로 훈련이 가능하다.

    -> 지식을 증류하는 방법으로 model의 ensemble 효과를 하나의 model로 전이할 수 있고 MoE와 달리, specialist model(student model)은 빠르고 병렬적으로 학습이 가능하다.

- Introduction
  - 지금까지 대규모 machine learning은 training stage와 deployment stage에서 다른 요구 사항일지라도 유사한 model을 사용했다. 이러면 학습시에 거대한 중복 dataset에서 structure를 추출하는 방향을 택하지만
    
