# 0821_Seminar

## R^2-CNN Fast Tiny Obj Detection in Large-scale REmote Sensing Images

- 네트워크 특징
Self-reinforced architecture   
로스를 디텍터와 분류기가 서로 주고 받으면서 상호작용적으로 학습.    
- 해당 방법을 사용하는 이점?
빈 패치는 분류기에서 걸러줘서 디텍터의 Cost를 줄일 수 있음    
FP는 방대하고 복잡한 배경에 의해 발생되며 이는 부뉼기와 디텍터의 상호작용으로 억제될수있음    
디텍터에 의해 추출된 fine-grained featyre가 주어지면 통합된 Classifier는 패치 안에 단 하나이=ㅢ 작은 객체만 존재하는 어려운 상황도 구별함    

- Tiny-net 사용 이유
보통 사전훈련된 모델을 사용하지만, 일반 객체와는 다르기떄문에 불이익이 있음.    
Heavy parameters를 고려하면 (웨이트가 딥따 많은거) 훈련 샘플이 제한되어있어서 처음부터 훈련하기에는 해당 간결한 네트워크 사용하는게 조음    

- TN 구조
