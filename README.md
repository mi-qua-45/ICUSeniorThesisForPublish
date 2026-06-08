掲載物
- 解析ファイル（卒業研究2(k_mer&hyp調整).ipynb）
- 卒論本文（Additive Effects of Fixed-Length Sequences in Promoting DNA Demethylation）

研究概要
DNAの塩基配列データから、対象領域のメチル化状態を予測する2値分類モデルを構築しました。

データ
染色体位置情報およびDNA塩基配列（総673件：維持396件、脱メチル化277件）

手法

- 特徴量抽出：CountVectorizerによるk-mer解析（k = 3〜8を網羅的に検証）
- アルゴリズム：ランダムフォレスト、ロジスティック回帰
- 評価：5-fold cross validation、混同行列、特徴量重要度の可視化
- 使用技術：Python、scikit-learn、pandas、matplotlib、seaborn

成果

- 初期モデル（k=4、ランダムフォレスト）の精度79.26%から、k=6のロジスティック回帰で86.78%まで向上
- モデルの係数分析により、先行研究で知られるZFP57関連モチーフなどの重要配列が予測に寄与していることを定量的に確認し、説明可能性と予測精度を両立した。
