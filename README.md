  
# 專案：銀行顧客流失分析  
本專案透過資料分析與機器學習模型，識別具流失風險的客戶，並提供具體的商業洞察，協助制定客戶挽留策略。  
  
  
---  

         
 ### **使用資料**    
資料來源: Kaggle   
資料集名稱: Bank Customer Churn Prediction Dataset   
資料集網址: https://www.kaggle.com/datasets/shivan118/churn-modeling-dataset/data   
說明: 原始檔案為 Churn_Modelling.csv，包含顧客基本資料（性別、年齡、國家）、金融狀況（信用分數、存款餘額、產品數量、是否持卡）、帳戶狀態（是否活躍會員、是否流失）等資訊。     
  
  
---  
   
  
### **使用技術**    
- Python (pandas, matplotlib, seaborn, scikit-learn, xgboost)    
- Google Colab   
- 視覺化分析
- 特徵工程     
- 機器學習模型訓練與評估   

          
---   
        
         
 ### **執行步驟**   
1. **資料載入與初探**  
   - 載入 Google Drive 上之 CSV 檔案  
   - 確認欄位型態、缺失值、統計摘要   

  
2. **探索性資料分析 (EDA)**   
   - 顧客流失率分布分析（Pie Chart）     
   - 分析不同顧客屬性（如年齡、信用分數、資產餘額等特徵）與流失率之間的關係。  
     - 德國客戶流失率相對較高。  
     - 女性流失數量略高於男性。  
     - 擁有 2 個產品的顧客流失率最低。  
     - 不活躍顧客的流失率明顯較高。  
     - 中年客戶（40–55 歲）流失率最高。  
     - 餘額越高者，流失較高。  
     - 信用分數與估計薪資與流失未有顯著關係。    
   - 使用 Heatmap 檢視各特徵與流失變數 (Exited) 之關聯性。    
   
  
          
3. **機器學習模型建立**   
   - 特徵工程：數值與類別欄位分開處理 (StandardScaler、OneHotEncoder)  
   - 使用三種模型進行比較：  
     - Logistic Regression  
     - Random Forest  
     - XGBoost  
   - 評估指標：Precision、Recall、F1-score      
    
    
     
4. **結論與商業洞察**   
- 流失高風險顧客特徵：德國、中年、存款餘額高、不活躍。  
- 產品策略：鼓勵單產品顧客升級至霜產品組合。  
- 活躍度提升：針對長期未互動的顧客，設計個人化推播與會員誘因，以提升活躍程度。  
- 預測模型：在 Logistic Regression、Random Forest 與 XGBoost 的比較下，XGBoost 在 Precision 與 Recall 之間達到較佳平衡，因此最終選擇 XGBoost 作為流失預測模型。    
  
  
---  
  
  
### **專案目標**   
  - 協助銀行辨識高風險流失客戶。    
  - 提供留客與銷售策略建議（提升產品數量、會員活躍度） 
  - 展示探索性分析、模型建置與商業洞察的能力
