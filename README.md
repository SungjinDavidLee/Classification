# Classification
여러 Classification 기술들의 개념 및 코드 설명

## VGGnet

1.  논문 원제 : Very Deep Convolutional Networks for Large-Scale Image Recognition, ICLR 2015, Karen Simonyan and Andrew Zisserman (Oxford)
2.  주요 Contribution 
- ConvNet Depth 가 이미지 인식 정확도에 미치는 영향 분석
- ConvNet 구성에 있어 Small Conv Filter (3x3) 의 강력함 발견
- 해당 ConvNet 구성으로 ImageNet 상위 랭킹을 차지하였을 뿐 아니라 다른 dataset 에서도 잘 동작 확인

3.  Architecture
- Input Size : fixed 224x224 RGB image
- Preprocessing : subtracting the mean RGB value
- padding is 1 pixel for 3x3 ConvLayers
- max pooling after ConvLayers : 2x2 pixel window with stride 2
- 3 Fully-Connected (FC) layers at the end of ConvNet : first two 4096 channels, last 1000 channels
- final layer : soft-max
- all hidden layers have ReLU

![Alt text](C:\Users\elfle\OneDrive\사진\머신러닝 이미지\VGGNet.png "VGGNet 구조")
