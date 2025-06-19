# ポートフォリオ：大規模株価収益率データを用いた企業ネットワークの推定

このリポジトリは、多変量の株価収益率データから、企業同士の成すネットワークを推定する統計・深層学習モデルを構築・検証した研究の実装例です。

## 📁 ディレクトリ構成
├── data/ # サンプルデータ（例：sample_data.csv）
├── training/ # 各モデルの学習を行うJupyter Notebook
├── weights/ # 学習済みモデルの保存ファイル（.pth, .pklなど）
├── forecast/ # モデルによる予測結果
└── result/ # 予測性能の評価や可視化を行うNotebook

## 🔍 内容の概要

- **提案モデル：**  
  Spatial AutoRegressionモデルを応用したネットワークの重み行列の推定モデルを2種類提案。
- **ベンチマークモデル：**  
  既存の2つの単純な重み行列の推定量（二乗距離、相関ベース）と比較。評価指標は、重み行列を用いたボラティリティ予測モデル（Mattera&Otto, 2024）の予測精度。
- **Notebook構成：**  
  `training/`以下に学習用Notebook、`result/`以下に評価(Diebold-Mariano検定)・ネットワーク可視化用Notebookを配置。
- **学習済みデータ：**  
  実行に時間がかかる部分は事前に学習済み重みや予測値を`weights/`および`forecast/`に保存済み。

## 参考文献
-Raffaele Mattera, Philipp Otto,
Network log-ARCH models for forecasting stock market volatility,
International Journal of Forecasting,
Volume 40, Issue 4,
2024,
Pages 1539-1555,
ISSN 0169-2070,
https://doi.org/10.1016/j.ijforecast.2024.01.002.
