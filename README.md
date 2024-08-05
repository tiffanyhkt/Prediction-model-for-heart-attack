### Summary

### 原始 Logistic Regression 模型 (82%)

### Tune 1 - 納入PCA
- Accuracy of Logistic Regression after PCA: 84%

### Tune 2 - 進行性別分群 (建立男女性別各自的 Logistic Regression Model)
不採納 PCA 結果:
- Male Accuracy: 85%
- Female: Accuracy: 94%

採納 PCA 結果:
- Male Accuracy: 75%
- Female Accuracy: 94%

### Tune 3 - 進行 K-means 分群 (建立 2 clusters 各自的 Logistic Regression Model)
不採納 PCA 結果:
- cluster_0 - Accuracy: 82%
- cluster_1 - Accuracy: 92%

採納 PCA 結果:
- cluster_0 - Accuracy: 76%
- cluster_1 - Accuracy: 96%

### 使用 "PCA" 後的模型預測, 精準度從 82% 提升至 84%
### 使用 "性別分群" 後的模型預測,對於 "女性" 有較顯著的提升, 精準度為94%
### 使用 "K-means分群" 後的模型預測, 搭配使用 PCA的cluster_1 精準度可達到96%

備註: 由於原始資料集本身樣本不多(300多筆),在預測準確度上會根據資料數量有較大幅度的變化,
此處的採用男女或K-means分群後再各自進行模型預測,對於某些分群結果有較大的精準度提升.