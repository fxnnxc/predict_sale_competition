# Predict Sale Competition

https://www.kaggle.com/c/competitive-data-science-predict-future-sales/overview


**WROC**  : Without Referencing others code

**WHOR**  : With the help of reference code

|Ref|Model |RMSE | Rank|
|---|---|---|--- |
|**WROC**| lightBGM|1.17|----|
|**WROC**|LSTM| 0.98340| ----|
|**WHOR**|LightGBM (optuna Tuning)|0.908 |Top 20%|
|**WHOR**|**XGBoost** + Additional Features | 0.88192| Top 2%|

---

## 1. Data Preprocessing
  * Read Data
  * Remove outlier
  * item category, shop name label encoding
  * Add Monthly Features + Lag feature
    * 매월 아이템 수(평균)
    * 매월 아이템별 판매량
    * 매월 가게별 판매량
    * 매월 아이템 카테고리별 판매량
    * 매월 가게 - 아이템 카테고리별 판매량
    * 매월 블록, 가게별 판매량
    * 매월 가게별 하위 카테고리 판매량
    * 매월 도시 판매량
    * 매월 아이템 가격
  
---

## 2. Train
메모리 용량 제한으로 인해서 데이터를 pickle로 저장한 뒤, 

모델 하나씩 훈련, 추론을 진행해야 한다. 

###  LSTM : 
###  LightGBM


### LightGBM KFold
###  XGBoost

---

## References

* Feature Engineering: 데이터 Feature Engineering 

https://www.kaggle.com/dlarionov/feature-engineering-xgboost

* 딥러닝으로 걷는 시계열 예측- 윤영선 지음 : LSTM Model 

http://www.yes24.com/Product/Goods/89019624

* LightGBM + optuna : LightGBM 및 데이터 Feature Engineering

https://www.kaggle.com/dhiiyaur/predict-future-sales-lgbm-hyperparameter-optuna

* XGBoost + Optuna : XGBoost 

https://medium.com/optuna/using-optuna-to-optimize-xgboost-hyperparameters-63bfcdfd3407
https://www.kaggle.com/c/competitive-data-science-predict-future-sales/discussion/170220
