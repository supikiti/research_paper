# Investigating GAN based Speech Dereverberation for Robust Speech Recognition
[Investigating GAN based Speech Dereverberation for Robust Speech Recognition]()

 <img src = "画像リンク" width=1000>

## どんなもの？
GANs have benn recently studied for speech enhancement to remove additive noises, but there still lacks of a work to examine their ability in speech dereverberation and the advantages of using GANs have not been fully established. In this paper, we provide deep investigations in the use of GAN-based dereverberation front-end in ASR. 
 1. we study the effectiveness of different dereverberation network, and find that LSTM leads to a significant improvement as compared with feed-forward DNN and CNN in out dataset. 
 2. further adding residual connections in the deep LSTMs can boost the performance as well. 
 3. for the success of GAN, it is important to update the generator and the discriminator using the same mini-batch data during training. 
 
 In summary, out GAN-based dereverberation front-end achieves 14%~19% relative CER reduction as compared to the baseline DNN dereverberation network when tested on a strong multi-condition training acoustic model.

## 先行研究と比べてどこがすごい？


## 技術と手法のキモはどこ？


## どうやって有効だと検証した？


## 議論はある？


## 次に読むべき論文


