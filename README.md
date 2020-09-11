# 特徵工程練習

這是藉由「特徵工程不再難:資料科學新手也能輕鬆搞定!」一書的範例做練習，加上自己理解後的註解。

書本提供的程式檔案與資料集:
https://github.com/PacktPublishing/Feature-Engineering-Made-Easy

### 1. Feature Understanding
藉由pandas理解資料內容與實作描述性統計。matplotlib則是將數據資料做圖形化觀察。依照資料的四種尺度做描述性統計與各式圖表繪製。

### 2. Feature Improvement
__-探索式資料分析__: 描述性統計、直方圖繪製、null accuracy(隨便猜時的正確率)與相關分析。

__-metric遺漏值__: 遺漏值觀察、遺漏值轉換、遺漏值處理(刪除法、平均值填補或中位數填補)。填補方法可以手動填補，也透過scikit-learn的impute方法填補。再搭配機器學習分類模型觀察填補前後之成效差異。

__-機器學習管線(Pipeline)__: 建立scikit-learn的Pipeline，讓資料依照我們設定的管線做處理及完成任務，並利用scikit-learn的GridSearch方法找尋最佳參數模型。

__-標準化與常態化__: 透過標準化與常態化將數據尺度不一的資料做轉換，在同樣的比例下比較，不因數值的大小有所差異。包含Z-score方法、最大最小縮放與列常態化。皆使用scikit-learn preprocessing套件。

### 3. Feature Constuction
__-nonmetric遺漏值__: 以出現次數最多的數值填補。

__-自定Pipeline的方法__: 透過繼承scikit-learn的TransformerMixin物件，就可以建立想要針對數據的處理方法。

__-編碼變數__:將nominal與ordinal的內容轉換成數值形式，而ordinal要保留順序上的差異。

__-metric變數分箱__: 將具有連續性的數值轉換成ordinal尺度可能是有意義的。

__-多項式特徵建立__: 藉由原始特徵之間的乘積建立新特徵，去觀察特徵之間的互動情形，再利用相關係數觀察特徵間的互動關係是否與反應變數有關。

__-文本特徵建構__: 詞袋模型與TF-IDF方法結合
