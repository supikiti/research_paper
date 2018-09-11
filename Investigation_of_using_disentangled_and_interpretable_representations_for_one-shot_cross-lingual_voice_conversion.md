# Investigation of using disentangled and interpretable representations for one-shot cross-lingual voice conversion
[Investigation of using disentangled and interpretable representations for one-shot cross-lingual voice conversion](https://arxiv.org/abs/1808.05294)

<div align="center"><img src = "https://user-images.githubusercontent.com/37444351/45349526-71be3400-b5ec-11e8-8ef4-ccb3d73197ae.png" width=500></div>

## どんなもの?
FHVAEモデルで, ノンパラレルでクロスリンガルな上, 各音素に対応する学習データが一つしかない(one shot)状態での声質変換を試みた論文. 10文以下で提案手法がベースラインを超え, 重複する音素がないデータでも十分な性能が得られることが確認できた.

## 先行研究と比べてどこがすごい？
従来では１つの言語間の変換だったが, 変換元話者と変換先話者が違う言語を話す場合の声質変換を試みた. https://shamidreza.github.io/is18samples/, ここでデモ音声がきくことができる.

## 技術と手法のキモはどこ？
従来のFHVAEのモデルを用いているため, とくに変化はなし.

## どうやって有効だと検証した？
潜在空間の可視化を行い, speker/languageで独立したクラスタが形成されていることが確認された. 変換された音声と従来手法とで, 音声品質と話者類似性をMOSでテストし, どちらにおいても従来手法を上回った. 

## 議論はある？
とくになし

## 次に読むべき論文


