# Scalable Factorized Hierarchical Variational Autoencoder Training
[Scalable Factorized Hierarchical Variational Autoencoder Training](https://arxiv.org/abs/1804.03201)

 <img src = "https://user-images.githubusercontent.com/37444351/45342243-50534d00-b5d8-11e8-83f1-8b09042be715.png" width=1000>

## どんなもの？
膨大なデータを学習する際に, ランタイムやメモリー, ハイパーパラメータ最適化の問題を改善するFHVAEにおける学習アルゴリズム手法.
潜在空間可視化のためのアプローチの提案とFHVAEの潜在変数の可視化.

## 先行研究と比べてどこがすごい？
従来の[FHVAE](https://github.com/supikiti/research_paper/blob/master/Unsupervised_Learning_of_Disentangled_and_Interpretable_Representations_from_Sequential_Data.md)の学習アルゴリズムは数千時間に及ぶデータセットに対応できなかった. そこで, 階層的サンプリング学習アルゴリズムにより, ランタイム&メモリー&ハイパーパラメータ最適化, の３つの問題を改善した. 3~1000時間で音声収録環境やノイズタイプを含むデータセットで提案手法を評価した. また, 定性的に性能を評価するための新たな可視化手法を提案する.
　従来のFHVAEは, 100000文を学習させると8GBのGPUメモリを使い切ってしまう欠点があり, 学習データとしてAMIやLibriSpeechを用いることは困難であった. 提案手法ではこの問題を改善した.

## 技術と手法のキモはどこ？
キャッシュサイズと対数尤度の分母の合計を制御するアルゴリズムをもちいることで, キャッシュサイズをデータサイズMからバッチサイズKに減らすことができる.

## どうやって有効だと検証した？
TIMIT(3696utterances, 3hours), Aurora-4(4620utterances, 10hours), AMI(200000utterances, 100hours), LibriSpeech(1000hours)で評価を行なった. 

## 議論はある？
バッチサイズを上げることで最適化の処理時間も悪くなった. バッチサイズが2000以上になると, 処理時間がバッチサイズに比例して悪くなった. 

## 次に読むべき論文
[Investigation of using disentangled and interpretable representations for one-shot cross-lingual voice conversion](https://arxiv.org/abs/1808.05294)


