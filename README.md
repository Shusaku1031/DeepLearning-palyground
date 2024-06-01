# 概要
Pythonの深層学習フレームワークKerasで画像分類モデルを学習/評価を試すために作ったリポジトリ。  
Cifar10の10クラス分類モデルを作り、テストデータの分類と簡易な評価を行った。

# 実行環境の構築
実行のプラットフォームにJupyter notebookを使うため以下のコマンドでインストール
```
pip install jupyter
```
その他以下ライブラリのインストールも同様にpipで行う。  
※kerasの前にtensorflowのインストールが必要
- tensorflow
- keras
- scikit-learn
- pandas
- numpy
- pandas
- matplotlib
- seaborn

# 実行手順
本リポジトリをclone
```
git clone https://github.com/Shusaku1031/DeepLearning-palyground.git
```
ターミナルでcloneしたDeepLearning-palygroundの直下まで移動し、次のコマンドでjupyter notebookを起動。
```
jupyter notebook
```
起動するとブラウザが展開されるので`image-classification.ipynb`のノートブックを開く。  
ノートブック内は以下の構成になっているため、Step1~3を順に実行。
- Step1.各種必要なライブラリのインポート
- Step2.学習用/テスト用データの準備から深層学習モデルの準備
  - データセット(cifar10)の読み込みと整形
  - imagenet学習済みモデルの読み込みと全結合層/出力層の形状の調整
  - モデルをcifar10で再学習
- Step3.テストデータに対する推論処理と結果表示
  - テストデータに対して学習済みモデルで推論
  - 推論結果の内訳を混同行列で表示
  - 評価指標(適合率,再現率,F1値)を計算