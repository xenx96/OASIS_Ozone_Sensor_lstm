# OASIS_Ozone_Sensor_lstm
Pytorch_lstm 을 활용한 오존 센서 측정 project 입니다.

- GPU를 사용하였으며, 해당 GPU는 Colab에서 제공된 GPU를 활용 하였습니다..
- Data는 실제 공간(280x135x110)의 공간에서 오존센서를 갖고 측정하였습니다..
- Data 전처리는 R로 진행하였으며, R파일은 현재 올라와있지 않고, 추후 업로딩 예정.

# Function
- create_sequences로 Data의 Sequence의 갯수를 필요에 맞게 만들수 있습니다.

- personal_data_set은 추후 다른데이터 사용시, 필요에 맞게 function을 수정하여 사용하면 Data를 수정 할 수 있습니다.

- data_set은 DeepLearning(LSTM)을 위한 Scaling 및 create_sequences를 활용한 Sequences 생성, GPU를 활용한 Tensor 변환을 할 수 있습니다.

# Class

- OASIS_LSTM은 LSTM모델로 Linear(선형) 모델입니다. 
- 해당 LSTM은 GPU를 활용하였으며, 해당 GPU는 Tensor에 활용된 GPU와 동일 GPU 입니다.


## Last Update
- 2021.02.09

# 결과
- 데이터 양이 매우작아 학습자체에 문제가 있어 OverSampling 및 ML을 고려하였음.
- ML은 비교적 가벼운 SVM모델을 사용하였으며, SVM은 R로 구현하였기에 현재 코드 없음.
- Data가 매우작기때문에 Lstm보다 SVM이 더 좋은 성능지표를 나타내었음
- 대표님 요청사항으로 LSTM을 만들었으나, 해당 모델은 보류하고 추후, 제주 카센터에서 센서로 측정한 데이터를 불러오면 다시 모델링 하기로함.
  + 제주카센터에서 데이터로 모델링 요청 취소.(데이터 수집이 불가)

# 요청사항
- 2월 15일 ~ 2월 19일 까지 제주 출장에서 받아오는 오존센서 데이터로, 차량의 크기 예측(Modeling)을 원함 : 1차(필수사항)
- 추후 차량의 크기에 따라 센서 한개의 값으로, 소독에 걸리는 시간또한 예측하여, 하드웨어에 담기길 원하심 : 2차(보류사항)
