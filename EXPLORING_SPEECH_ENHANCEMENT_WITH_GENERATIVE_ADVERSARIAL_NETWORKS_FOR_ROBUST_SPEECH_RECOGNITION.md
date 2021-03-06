# EXPLORING SPEECH ENHANCEMENT WITH GENERATIVE ADVERSARIAL NETWORKS FOR ROBUST SPEECH RECOGNITION
[EXPLORING SPEECH ENHANCEMENT WITH GENERATIVE ADVERSARIAL NETWORKS FOR ROBUST SPEECH RECOGNITION](https://arxiv.org/pdf/1711.05747.pdf)

 <div align="center"><img src = "https://user-images.githubusercontent.com/37444351/45405959-b8209b00-b69f-11e8-9c09-68f4edce1bf8.png" width=600></div>

## どんなもの？
従来のGANによるノイズ除去は, 生音声データを直接用いるものであったが(SEGAN), 本論文ではログメルフィルタバンクを用いる手法を提案している. 提案手法により付加されたノイズ及び反響音が除去され, MTR手法より7%,WER精度が向上した.

## 先行研究と比べてどこがすごい？
従来法であるSEGANではノイズが付与された生音声データから直接ノイズを除去できたが, 反響が存在している場合, ASRの精度が著しく低下する問題点があった. 提案法では, 生音声データをもちいるのではなく, メルフィルタバンクの２次元データ直接, ノイズなしの２次元メルフィルタバンクへ変換できる. 

## 技術と手法のキモはどこ？
ノイズデータで学習させたASRモデルに対し, ノイズデータをtestしWERが20.3％になった. これに対し, 同モデルにFSEGANの出力を入力したところ25.4%になってしまった. これを改善する手法としてノイズデータを学習したASRを再度, ノイズデータ+FSEGANの出力したクリーンなデータで再学習させる方法が提案された(testの際は, ノイズデータに対しFSEGANでクリーンにした後, ASRに入力される). この提案手法により, WERが17.1%まで減少させることに成功した.  

## どうやって有効だと検証した？
省略

## 議論はある？
なし

## 次に読むべき論文
元のSEGAN

[SEGAN: Speech Enhancement Generative Adversarial Network](https://arxiv.org/abs/1703.09452)

ノイズデータをデータセットに加えたときの効果

[JOINT NOISE ADAPTIVE TRAINING FOR ROBUST AUTOMATIC SPEECH RECOGNITION](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=6854051)

