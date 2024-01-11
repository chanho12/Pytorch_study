# 2강 정리

### 모델 학습 순서 정리

### Hyperparameter

- CUDA 설정
- hyperparameter 설정하기

### data preparation

- 데이터 불러오기 및 dataloader를 활용하여 batch에 맞게 데이터 설정해주기.
- 사이즈 확인해서 모델 돌리는 과정 알아보기

### Making Model

- init 설정
    - `nn.Module`을 이용하여 상속해서 이전 메서드 받아오기
    - `super(model name, self).__init__()`을 통해 `nn.Module` 내에 있는 메서드 상속받아 이용
- forward 설정
    - 내가 모델에서 굴릴 구조를 실제로 넣는 구간

### Optimizer, Objective Function

- 모델을 킨다.
- 무슨 optimizer, objective function을 사용할 것인지 정하기.

### Making training func

- `model.train()` 을 통해 모델을 학습 상태로 지정한다.
- 학습할 데이터는 loader에서 불러오고, 이를 DEVICE 로 바꾸어 GPU로 바꾸어 준다.
- `optimizer.zero_grad()`를 활용해서 optimizer의 Gradient를 초기화해준다.
- critierion을 통해 loss 계산 후 `loss.backward()`를 이용해서 update할 gradient를 파라미터에 할당시켜준다.
- `optimizer.step()` 각 파라미터에 할당된 Gradient 값을 업데이트한다.

### Making evaluate func

- `model.eval()` 을 이용해서 모델을 평가 상태로 지정한다.
- `with torch.no_grad()` 를 이용하여 eval 과정에서는 기울기가 변하지 않기 때문에 사용해준다.

### Making training procedure

- `Epoch`을 돌리면서 `train`을 시켜준다.
- 이후 `evaluate`로 나온 `test` 결과를 통해서 결과를 보여준다.
- 매번 바뀌는 결과를 `print` 해준다.