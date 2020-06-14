# 概要
Kaggleの「Titanic: Machine Learning from Disaster」というCompetitionに参加し, 公開されているデータセットを用いて生存者予測を行った.

# 必要なPythonライブラリ
- sklearn
- pandas
- numpy
- matplotlib
- seaborn
- xgboost
- lightGgbm

# ファイルの確認方法
gitgub上でクリックして確認可能.<p>

# ローカルで実行する場合
titanic01 ~ 10はjupyter notebookで実行, この時, csvファイルは同じディレクトリに置く.<p>
titanic11 ~ 15はGoogle Colaboratoryで実行, この時, csvファイルをGoogle Driveの"Colab Notebooks"/titanicに置き、一つ目のセルを実行し, ドライブをマウント.<p>

# csvファイルの説明
train.csv: トレーニングデータ.<p>
test.csv: テストデータ.<p>
expand.csv: 80.86%を出したファイル, トレーニングデータの拡張に利用.<p>

# ipynbファイルの説明
titanic01.ipynb: Votingを利用. (76%)<p>
titanic02.ipynb: 「titanic.ipynb」のそれぞれのモデルをグリッドサーチを用いてチューニング. (77.5%)<p>
titanic03.ipynb: 特徴量"Sex", "Embarked"をワンホットエンコーディング. (77.99%)<p>
titanic04.ipynb: AdaBoost, ExtraTrees, GradientBoost, RandomForestを何も考えずに使ってみた. (77.5%)<p>
titanic05.ipynb: 特徴の重要度に着目し, 重要度の低い特徴を除去してみた. (77.5%)<p>
titanic06.ipynb: もう一度特徴量と向き合い, 自分で新たな特徴量を増やした. (77.99)<p>
titanic07.ipynb: 78%を超えるまで試行錯誤, 特徴量の剪定や, 過学習の検出によって目標達成. (80.86%)<p>
titanic08.ipynb: 標準化や正規化を利用しMLPも追加した, しかし, 78%と, 少し下がってしまった. (78%)<p>
titanic09.ipynb: XgboostとLightGBMを使ってみた. (76%)<p>
titanic10.ipynb: スタッキングの実装. (実装途中でtitanic11.ipynbに移行)<p>
titanic11.ipynb: Google Colaboratoryにてスタッキングの実装続き.<p>
titanic12.ipynb: スタッキングに使うそれぞれのモデルをチューニング. (79.42%)<p>
titanic13.ipynb: 特徴量の追加, トレーニングデータの拡張, スタッキングを利用. (80.86)<p>
titanic14.ipynb: 拡張したトレーニングデータを使って, Votingを利用. (80.38)<p>
titanic15.ipynb: 分類の際の閾値を調整. (80.86%)<p>