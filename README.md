中文情緒字典（Chinese Sentiment Lexicon）
===
# 功能
利用 `PMI` 和 `SOC-PMI` 等語言統計分析算法，從現有文章中標記一些seed words，通過半監督式學習找出段落中隱含的其他情緒詞匯，從而建立起完整的情緒字典。

情緒字典的覆蓋範圍包括 `名詞` 、 `動詞` 和 `形容詞` 等部分，每個詞都會有一個正向分數（positive）和一個負向分數（negative）。兩個分數的高低可以判斷這個詞的情緒分布狀況。

# 必要配置

- `Python2`
- `JDK`
- `jieba`

# 使用流程

- 將預設的Seed Word（也就是自行標記的幾個情緒面向詞匯）放入 `SentimentLexicon/data/input/Seedwords.txt`  中。

![](https://i.imgur.com/3KEOqCF.png)

- 將需要提取情緒詞匯的訓練文章放入 `SentimentLexicon/data/input/Corpus.txt` 中。

![](https://i.imgur.com/nGJWyIO.png)

- 運行 `SL.jar` 文件即可開始訓練過程：

```
java -jar 'SL.jar'
```

# 測試結果

- 得到的結果會儲存在 `SentimentLexicon/data/Propagation/FinalMatrix.csv` 文件中。 

![](https://i.imgur.com/Ugyr8cq.png)

可以看出在比較詞的正負向上能夠取得比較可觀的結果。

# KeyWords

###### tags: `Sentiment Lexicon` `NLP` `PMI`
