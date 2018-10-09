# 題名
[MTGAN:Speaker Verification through Multitasking Triplet Generative Adversarial Networks](https://arxiv.org/pdf/1803.09059.pdf)

 <div align="center"><img width="772" alt="2018-10-09 16 11 48" src="https://user-images.githubusercontent.com/37444351/46652492-26dd0f80-cbde-11e8-8956-41c22ec6514e.png"></div>

## どんなもの？
話者認証に置ける， エンベディングに置けるエンコードの過程を, GANとマルチタスク最適化により改善するもの. 具体的には, MTGANと呼ばれる, 短い発話において音韻情報を利用しないE2E話者認証システムを提案する. 実験結果により, 従来のi-vectorやtriplet methodを用いる方法より, より低いEER(equal error rate)が得られ, 認識速度も向上した. 

## 先行研究と比べてどこがすごい？
i-vectorを用いた従来手法と異なり, E2EモデルのASVモデルは短い発話で良い性能を発揮する. 

## 技術と手法のキモはどこ？
triplet lossを組み入れたGANに, マルチタスクを組み入れている点. tripletGANは以前から存在した.

## どうやって有効だと検証した？
モデルの学習にはLibriSpeechを用いた. モデルの評価には, 全音素を含んでいるTIMITを用いた. 従来のi-vector/Cosine, i-vector/PLDA, Softmax loss, Triplet lossをベースラインとし, 検証を行った. EER, Accuracy共に, 4つのベースラインを上回った. 

## 議論はある？
なし

## 次に読むべき論文
- 従来手法

[End-to-End Text-Independent Speaker Verification with Triplet Loss on Short
Utterances](https://www.isca-speech.org/archive/Interspeech_2017/pdfs/1608.PDF)

- Triplet lossを組み入れているGAN

[TripletGAN: Training Generative Model with Triplet Loss](https://arxiv.org/pdf/1711.05084.pdf)

[TRAINING TRIPLET
NETWORKS WITH GAN](https://arxiv.org/pdf/1704.02227.pdf)

- triplet手法はサンプリング手法に大きく依存しており, その問題はこちらで議論されている. 

[Sampling Matters in Deep Embedding Learning](https://arxiv.org/pdf/1706.07567.pdf)

### 追記
triplet lossは, クラス内部の距離を最小化すると共に, クラス間距離を最大化する. しかし, データにノイズや反響音がある場合, 話者認証タスクにおいて, triplet lossによる学習では限界がある. 
