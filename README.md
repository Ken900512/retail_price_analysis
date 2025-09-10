# **零售價分析與預測**

## **專題介紹**
價格最佳化有助於企業找到有效的定價平衡點，實現盈利目標，同時也滿足客戶需求。本專題主要分析目標變數"unit_price"(零售價)與其他變數的關聯，以及嘗試建立模型來預測價格，並找出重要的變數。

---

## **資料介紹**  
- 資料來源 : [Kaggle](https://www.kaggle.com/datasets/suddharshan/retail-price-optimization/data)    
- 資料時間 : 2017-2018   
- 資料內容 : 共30個變數，676筆資料，包括產品單價、產品的相關資料、運費、競爭對手的相關資料等  

---

## **資料處理**
- 數據集無缺失值
- 去除多餘變數  
- 處理競爭對手資料(取平均)
- 初步整理後剩餘21個變數

---


## **探索式資料分析(EDA)** 
- 目標變數(unit_price)與其他變數分析  
- 相關係數熱力圖  
- 篩選變數 : 取相關係數大於0.1的變數(lag_price除外)  

---

## **模型篩選與重要變數**  
- 檢查變數共線性問題  
- 比較6個模型 : linear、ridge、lasso regression、Decision Tree、Randomforest、XGboost   
- 最終為XGBoost模型MSE為最低  
- XGboost's feature importance Top 2 :  
  - qty : 銷售數量  
  - total_price : 總金額

---

## **結語**
1. 以預測單價而言，兩個集成學習模型相對其他模型較好，最好的是XGboost  
2. 模型覺得最重要的變數為qty、total_price，但這兩個變數大家都知道其重要性，未來，或許可以控制這些變數，以探討其他因素對價格的額外貢獻。

---

## **工具**
- Python
- Machine Learning(regression、Decision Tree、RandomForest、XGboost)
- Feature importance

---

## **結構**
retail_price_analysis  
│── README.md     
│── retail_price_main.pdf # 書面報告     
│── retail_price_code.ipynb # 程式碼      
│── retail_price.csv # 資料集     


