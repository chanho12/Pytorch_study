# 파이썬 딥러닝 파이토치

## 1강 정리

데이터 구성은 scalar, vector, matrix, tensor가 있다. NLP 에서 사용하는 텍스트 단위는 전부 matrix로 차원 간의 계산을 잘 알아야 한다. 

### tensor 기본

기본 단위 : torch.tensor()

### 단순 계산

torch.add(tensor1, tensor2)

torch.sub(tensor1, tensor2)

torch.mul(tensor1, tensor2) #multiwise 곱

torch.div(tensor1, tensor2)

### 행렬 곱 계산

torch.matmul(mat1, mat2)

mat1.mm(mat2) ## 이 구조가 제일 간단하기에 사용하는 법을 자세히 알아야 한다. 

torch.matmul(tensor1, tensor2)

### 내적

torch.dot(vector1, vector2)