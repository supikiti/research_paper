# Investigating GAN based Speech Dereverberation for Robust Speech Recognition
[Investigating GAN based Speech Dereverberation for Robust Speech Recognition]()

 <img src = "画像リンク" width=1000>

## どんなもの？
GANをASR前段階としての残響抑圧に関する調査をまとめた論文.具体的には以下の点について言及されている.

1. 異なる残響抑圧モデルの効果の比較.また, 従来のフィードフォワードモデルと比較するLSTMモデルの効果
1. residual接続(Resnetと同じ構造)を導入することにより, LSTMの性能が向上
1. GANの学習中は, 生成器と判別器を同じミニバッチデータで更新するのが重要である. 
 
また, GANによるASRの前段階における残響抑圧は, 従来のベースラインDNNと比較して, 14% ~ 19%のCERが減少した. 

## 先行研究と比べてどこがすごい？


## 技術と手法のキモはどこ？


## どうやって有効だと検証した？


## 議論はある？


## 次に読むべき論文
[Speech Dereverberation Using Non-Negative
Convolutive Transfer Function and
Spectro-Temporal Modeling](https://uol.de/fileadmin/user_upload/mediphysik/ag/sigproc/download/papers/SP2015_28.pdf)

[Time-Frequency Masking in the Complex Domain
for Speech Dereverberation and Denoising](https://web.cse.ohio-state.edu/~wang.77/papers/Williamson-Wang.taslp17.pdf)

- こいつは絶対に読むべき（MSE誤差について)
[Mean Squared
Error: Love It
or Leave It?](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4775883)
