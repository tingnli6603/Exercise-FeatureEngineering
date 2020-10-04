# 特徵工程練習

藉由「特徵工程不再難:資料科學新手也能輕鬆搞定!」一書的範例做練習，加上自己理解後的註解。

書本提供的程式檔案與資料集:
https://github.com/PacktPublishing/Feature-Engineering-Made-Easy

__pima_predict.ipynb__ 實作一套資料分析流程，從探索式資料分析、遺漏值填補、分類模型選擇、特徵選取到特徵轉換，並比較不同方法之間的好壞。

1.Feature Understanding
==
__-描述性統計__: 藉由pandas理解資料內容與實作描述性統計。

__-資料視覺化__: 藉由matplotlib則是將數據資料做圖形化觀察，如長條圖、直方圖、盒鬚圖等。

__-尺度理解__: 數據資料分成nominal、ordinal、interval與ratio四種尺度，尺度間使用的統計與圖形有所差異。

2.Feature Improvement
==
__-探索式資料分析__: 描述性統計、直方圖繪製、null accuracy(隨便猜時的正確率)與相關分析。

__-metric遺漏值__: 遺漏值觀察、遺漏值轉換、遺漏值處理(刪除法、平均值填補或中位數填補)。填補方法可以手動填補，也透過scikit-learn的impute方法填補。再搭配機器學習分類模型觀察填補前後之成效差異。

__-機器學習管線(Pipeline)__: 建立scikit-learn的Pipeline，讓資料依照我們設定的管線做處理及完成任務，並利用scikit-learn的GridSearch方法找尋最佳參數模型。

__-標準化與常態化__: 透過標準化與常態化將數據尺度不一的資料做轉換，在同樣的比例下比較，不因數值的大小有所差異。包含Z-score方法、最大最小縮放與列常態化。皆使用scikit-learn preprocessing套件。


3.Feature Constuction
==
__-nonmetric遺漏值__: 以出現次數最多的數值填補。

__-自定Pipeline的方法__: 透過繼承scikit-learn的TransformerMixin物件，就可以建立想要針對數據的處理方法。

__-編碼變數__:將nominal與ordinal的內容轉換成數值形式，而ordinal要保留順序上的差異。

__-metric變數分箱__: 將具有連續性的數值轉換成ordinal尺度可能是有意義的。

__-多項式特徵建立__: 藉由原始特徵之間的乘積建立新特徵，去觀察特徵之間的互動情形，再利用相關係數觀察特徵間的互動關係是否與反應變數有關。

__-文本特徵建構__: 詞袋模型與TF-IDF方法結合

4.Feature Selection
==
__-定義特徵選擇好壞__:包含轉換/擬合時間、預測新實例時間、正確率等。

__-挑選適合的機器學習方法__:先用原特徵挑選最佳分類成效的機器學習方法。

__-基於統計的特徵選取__: 包含Pearson相關係數與假設檢定方法(ANOVA)。

__-基於機器學習的特徵選取__:包含決策樹(資訊熵)和線性模型與正規化(L1與L2正規化)。

5.Feature Transformation
==
__-Principle Component Analysis__: 主成分分析將原始特徵降維，利用特徵量(eigenvalue)決定主成分數量，並利用特徵向量(eigenvector)將原始數據轉換。

__-Linear Discriminant Analysis__: 相較於PCA，LDA屬於監督式的降維，透過反應變數的分類做監督降維。

__-將transformation加入到pipeline內__: 透過降維方法觀察分類成效。

6.Feature Learning
==
__-Restricted Boltzmann Machine__:運用淺層神經網絡學習原始特徵的離散程度，進而建立新特徵。

__-Word2Vec__:基於淺層神經網絡，學習文本中字詞在鄰近距離的機率，進而生成代表文字意義的向量。可針對向量做計算，是有語意上的意義。
