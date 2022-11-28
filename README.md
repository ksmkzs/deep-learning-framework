# deep-learning-frame-work
TensorflowやPytorchなどの外部フレームワークを用いずにdeeplearningのフレームワークを作成しようとしている。 2022年11月27日 ksm.pyにて一応完成
  
オライリー社の出版している『ゼロから作るDeepLearning③ フレームワーク編』を読み、多少の変更を加えながらフレームワークを作成している。
それが1.pyに保存されている
※2022/11/27現在  より深い理解のためにksm.pyでもう一度同じコードを見やすさ重視で書いている
  
2022 11/27 
CBOWモデルを作成した。
[こちら](http://nlp.ist.i.kyoto-u.ac.jp/index.php?日英中基本文データ)からダウンロードしたデータを実行ディレクトリと同じ場所に置く必要がある。
これらの単語は512次元のベクトルに変換され、npzに補完される。
(実行はGPU環境推奨)





※現在は実行されないが#実装の部分の書き換えにより実行可能
((現在は全結合のモデルを再現可能であり、実行することで本書で用意されている「[MNISTデータセット]( http://yann.lecun.com/exdb/mnist/ )」の画像分類をするディープラーニングモデルの学習が実行され、my_mlp.npz上にハイパーパラメータが保存される。
データセットの読み込み方法については、本書で用意されているファイルを転用している。
))

・max epoch = データを何周学習させるか  
・batch size = 一回の処理に何個のデータを使用するか  
・hidden_size = 隠れ層のデータ数  
・accuracy = データの精度(100%が最大)  
    
また、ReLU関数とSigmoid関数を自由に設定できるほか、Adam、AdaGrad、Momentiumなどの最適化関数も利用でき、dropoutも利用可能。





# Requirement

MeCab
Cupy
Cupyx
Numpy
