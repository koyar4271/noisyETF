# noisyETF

Neural Collapse (NC) 現象におけるラベルノイズとデータ不均衡の影響を解析するためのプロジェクトです。卒業研究の成果物を管理しています。

## 概要
本研究では、学習収束期の幾何学的構造である **Neural Collapse** に着目し、実用的な制約下での挙動を分析しています。

- **解析対象**: Fixed ETF Classifier と Learnable Classifier における $NC_1, NC_2, NC_3, NC_4$ 指標
- **比較項目**: Label Smoothing (LS) vs Cross Entropy (CE)
- **実験設定**: ラベルノイズ混入、およびクラス間不均衡データ

## 独自の貢献 (Original Contributions)
先行研究（[neural_collapse_ls_vs_ce](https://github.com/glbreeze/neural_collapse_ls_vs_ce)）をベースとしつつ、以下の機能を独自に実装しました。

1. **ノイズ・不均衡シミュレータ**: 任意の割合でノイズを注入する実験環境を構築
2. **自動解析ツール**: 学習中の NC 指標をトラッキングし、可視化するスクリプトを統合
3. **リファクタリング**: 実験効率化のため、モデル定義と評価ロジックを分離

## 🛠 クイックスタート
```bash
git clone [https://github.com/koyar4271/noisyETF.git](https://github.com/koyar4271/noisyETF.git)
cd noisyETF
pip install -r requirements.txt
python main.py --loss ls --noise_rate 0.2
