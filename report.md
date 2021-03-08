# Garbage Classification

Deepest Season 9. Quest 1: Vision

### Framework & Code reference

TensorFlow 2를 사용하여 본 프로젝트를 수행했습니다. 코드 reference는 notebook에 정리해두었습니다.

### CNN Model

다음과 같은 Convolutional Neural Network를 구성하였습니다. 학습한 parameter는 총 977,958개로 1M보다 적습니다.

<img src="https://user-images.githubusercontent.com/13795717/110299104-a59d3780-8038-11eb-833c-519238e57e98.png" width=400/>

### Data augmentation

Data augmentation은 아래의 방법들을 이용했습니다.

- `RandomFlip()`
- `RandomRotation()`
- `RandomZoom()`
- `RandomTranslation()`
- `RandomContrast()`
- cutmix
- mixup

### Hyperparameters

Name | Value | Detail
---- | ---- | ----
Optimizer | Adam | beta_1 = 0.9<br>beta_2 = 0.999 <br>epsilon = 1e-7<br>amsgrad = False
learning rate| 0.001 | -
batch size | 32 | -
epochs | 400 | - 

### Loss and Accuracy

학습 진행에 따른 Training, Validation loss와 accuracy는 아래와 같습니다.


<img src="https://user-images.githubusercontent.com/13795717/110299580-2e1bd800-8039-11eb-9a1c-8d57616dd8fd.png" width=400/>


### Evaluation

Test set에 대해 model을 evaluate한 결과는 아래와 같습니다.

Loss | Accuracy
---- | ----
0.6191 | 0.7888
