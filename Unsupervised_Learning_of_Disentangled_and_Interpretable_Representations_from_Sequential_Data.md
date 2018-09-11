# Unsupervised Learning of Disentangled and Interpretable Representations from Sequential Data
[Unsupervised Learning of Disentangled and Interpretable Representations from Sequential Data](https://arxiv.org/pdf/1709.07902.pdf)

 <img src = "https://user-images.githubusercontent.com/37444351/45338952-f5ffbf80-b5ca-11e8-86b3-67b69443cab2.png" width=1000>

## どんなもの？
教師無しで系列レベル特徴量と区間レベル特徴量を学習できるFHVAEを提案する. 雑音除去や声質変換にも利用することができる.

## 先行研究と比べてどこがすごい？
従来から半教師あり学習や教師なし学習で, 静的なデータからVAEの潜在変数が表現するものを理解する試み(DC-IGN, InfoGAN, β-VAE)などは存在したが, 系列データを利用するものはなかった. 提案手法では,系列データから教師なしで系列依存特徴量と系列非依存特徴量を抽出できる. [SRNN](https://arxiv.org/abs/1506.02216), [VRNN](https://arxiv.org/abs/1605.07571), [neural statistician](https://arxiv.org/abs/1606.02185), [SVAE](https://arxiv.org/pdf/1603.06277.pdf)などの従来手法は, 手作業で調べたりラベルデータを用いなければ潜在空間が解釈不可能であったのに対し, 提案手法ではこれらの問題を解決できた.


## 技術と手法のキモはどこ?
Encoder部分で, 系列データ(x1:T)から系列特徴量を推論する(z2). 推論されたz2を利用して, z2条件付きのもとで系列データから区間特徴量z1を推論する. Decoder部分で, 得られた潜在変数z1, z2からそれぞれ系列データを生成する. Seq2Seqモデルとなっている.  

## どうやって有効だと検証した？
2つの音声コーパスデータ(TIMIT, Aurora-2)を利用し評価された. TIMITコーパスで, 従来手法(i-vector)による話者認証より, FHVAEによる話者認証のほうが, EERが大きく改善した. Aurora-2をもちいた雑音音声認識タスクにおいても, 従来手法であるβ-VAEより大きなWERの改善を見せた.

## 議論はある？
テキストデータや動画などに適用したらおもしろいかも？

## 次に読むべき論文
[Scalable Factorized Hierarchicall Variational Autoencoder Training](https://arxiv.org/abs/1804.03201)

