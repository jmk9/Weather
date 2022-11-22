# Weather

Predict tomorrow weather by using model related to RNN.   
RNN, LSTM, GRU 등의 RNN 계열 model로 kaggle에서 제공하는 날씨 데이터를 갖고 다음날 mean temperature를 예측  



다음 링크의 dataset 사용   
> https://www.kaggle.com/datasets/thedevastator/weather-prediction   
   
<br/>
   
   
data는 csv format이고 2000.1.1 ~ 2010.1.1까지의 날씨 정보가 담겨있음.   
총 18개의 도시가 존재하고, 각 도시마다 날씨 정보를 담고있는 8~10개의 column을 가짐.   
dataset split은 다음과 같음.   
- train dataset: 2000.01.01 ~ 2007.12.31   
- validation dataset: 2008.01.01 ~ 2008.12.31   
- test dataset: 2009.01.01 ~ 2009.12.31   
   
   
   
   
총 두 가지 방법으로 project를 진행해보았음.   
1. 18개의 도시를 각각 input으로 넣어 weight을 달리하거나 model을 달리하여 predict   
2. 18개의 도시를 한 번에 input으로 넣어 predict   
   
   
   
   
2번의 경우가 훨씬 간단하고 편했으나 1번의 경우 도시 별로 알맞은 weight을 가져 더 좋은 성능을 낼 것이라고 생각했으나, 각 column들의 correlation을 확인해보니 각 도시들의 온도가 서로 연관성이 있어 2번의 경우를 선택함.   
