# Azure Quantum を知る（2026/10版）

量子コンピュータを初めて学ぶ方が、基礎概念から Azure Quantum、最適化、金融、材料計算、Azure HPC 連携までを段階的に学ぶための教材です。

## Azure Quantum を一言で言うと

最初に、最も誤解されやすい点をお伝えします。

> **Azure Quantum は「Microsoft製の量子コンピュータ」ではありません。**
> **複数の量子コンピュータ企業のマシンへ、Azureという共通の窓口からアクセスできるサービスです。**

| よくある疑問 | 答え |
|---|---|
| ゲート方式？アニーリング？ | 使える実機は**ゲート方式が中心**。アニーリング専用機（D-Waveなど）は含まれない |
| マシンはMicrosoft製？ | いいえ。**IonQ、Quantinuum、Rigetti、Pasqal** という他社のマシン |
| Microsoftの役割は？ | 開発ツール（Q#/QDK）、シミュレーター、見積もりツール、Azureの認証・課金・権限管理 |
| Majoranaチップは使える？ | 研究開発段階。2026年10月時点で一般提供の実行先ではない |
| 最適化の専用サービスは？ | 旧QIOは2023年6月に終了。自分で定式化して実行先を選ぶ |
| 無料で学べる？ | **学べます。** シミュレーターとQDKだけなら料金はかかりません |

詳しい解説は [第2章 Azure Quantum 概要](./course.md#2-azure-quantum-概要) にあります。

---

## どこから読めばいい？

### はじめての方は、この順番で

| 順 | 進む先 | 内容 | 目安 |
|---:|---|---|---:|
| 1 | [第0章 最初に知っておくこと](./course.md#0-最初に知っておくこと) | 量子コンピュータへの向き合い方 | 10分 |
| 2 | [第1章 量子コンピュータとは](./course.md#1-量子コンピュータとは) | 量子ビット、方式の種類、提供ベンダー | 40分 |
| 3 | [第2章 Azure Quantum 概要](./course.md#2-azure-quantum-概要) | サービスの正体、特徴、適用分野、他社比較 | 40分 |
| 4 | [第3章 2026年10月時点の最新情報](./course.md#3-2026年10月時点の最新情報) | 提供中の機能と、研究段階の区別 | 15分 |
| 5 | [第4章 使えるようにするまで](./course.md#4-azure-quantum-を使えるようにするまで) | 環境構築、ワークスペース作成 | 30分 |
| 6 | [ハンズオン0 ▶ 量子計算の基礎](./notebooks/00_quantum_basics.ipynb) | 量子ビット、測定、もつれ、Azure送信 | 60分 |
| 7 | [第6章 数理最適化の解説](./course.md#6-ハンズオン2-数理最適化問題を解く) → [ハンズオン1 ▶](./notebooks/01_mathematical_optimization.ipynb) | Max-Cut、QUBO、組合せ爆発 | 60分 |
| 8 | [第7章 ポートフォリオ最適化の解説](./course.md#7-ハンズオン3-ポートフォリオ最適化) → [ハンズオン2 ▶](./notebooks/02_portfolio_optimization.ipynb) | 収益とリスクのトレードオフ | 75分 |
| 9 | [第8章 材料開発の解説](./course.md#8-ハンズオン4-材料開発の問題を解く) → [ハンズオン3 ▶](./notebooks/03_materials_vqe.ipynb) | 基底状態、VQE、量子と古典の二人三脚 | 75分 |
| 10 | [第9章 Azure HPCとのハイブリッド利用](./course.md#9-azure-hpcとのハイブリッド利用) | 量子とHPCの組み合わせ方 | 30分 |
| 11 | [第10章 適用判断テンプレート](./course.md#10-適用判断テンプレート) | PoCの始め方と、やめどき | 20分 |
| 12 | [第11章 将来の展望](./course.md#11-将来の展望) | 短期・中期・長期の見通し | 15分 |

各ハンズオンは、先に講義本文の解説を読んでからNotebookを開くと理解しやすくなります（[第5章](./course.md#5-ハンズオン1-azure-quantum-を使ってみる) がハンズオン0に対応します）。

### 目的別の近道

| やりたいこと | 進む先 |
|---|---|
| とにかく動かしてみたい | [ハンズオン0 ▶](./notebooks/00_quantum_basics.ipynb) |
| 量子コンピュータの種類を知りたい | [第1章](./course.md#1-量子コンピュータとは) |
| 他社サービスと比べたい | [第2章](./course.md#2-azure-quantum-概要) |
| 環境を作りたい | [第4章](./course.md#4-azure-quantum-を使えるようにするまで) |
| 最適化の案件が来ている | [第6章](./course.md#6-ハンズオン2-数理最適化問題を解く) |
| 金融での使い道を知りたい | [第7章](./course.md#7-ハンズオン3-ポートフォリオ最適化) |
| 材料・化学での使い道を知りたい | [第8章](./course.md#8-ハンズオン4-材料開発の問題を解く) |
| PoCをやるべきか判断したい | [第10章](./course.md#10-適用判断テンプレート) |
| 公式ドキュメントを探したい | [第12章](./course.md#12-公式参照資料) |

---

## 教材構成

| ファイル | 内容 | 目安 |
|---|---|---:|
| [course.md](./course.md) | 講義本文、セットアップ、比較、HPC、将来展望 | 4～6時間 |
| [00_quantum_basics.ipynb](./notebooks/00_quantum_basics.ipynb) | 量子ビット、重ね合わせ、測定、Bell状態、Azure送信 | 60分 |
| [01_mathematical_optimization.ipynb](./notebooks/01_mathematical_optimization.ipynb) | Max-Cut、QUBO、全探索、量子向け定式化 | 60分 |
| [02_portfolio_optimization.ipynb](./notebooks/02_portfolio_optimization.ipynb) | 収益・リスク・制約を含む銘柄選択 | 75分 |
| [03_materials_vqe.ipynb](./notebooks/03_materials_vqe.ipynb) | 2準位材料モデル、変分量子固有値法（VQE） | 75分 |

Notebook は標準 Python だけで既定セルを実行できます。Azure Quantum への接続セルは、意図しない課金を防ぐため既定で無効です。

GitHub 上では各 `.ipynb` をそのまま閲覧できます。実際にセルを実行する場合は、リポジトリをクローンしてローカルで開いてください。

## ローカル実行

前提:

- Python 3.10 以上（Microsoft Learn は 3.11 を推奨）
- VS Code
- VS Code の Python、Jupyter 拡張

```bash
python3 -m venv .venv
source .venv/bin/activate       # Windows: .venv\Scripts\activate
python -m pip install jupyterlab
jupyter lab
```

Azure Quantum/Q# も使う場合:

```bash
python -m pip install --upgrade "qdk[azure,jupyter]"
```

材料化学の公式 QDK Learning コースも使う場合:

```bash
python -m pip install "qdk-chemistry>=2.2.0"
```

## 費用と安全上の注意

- ローカルシミュレーターと本教材の既定セルは Azure 課金を発生させません。
- 実機・クラウドシミュレーターの料金、利用可能リージョン、キュー時間はプロバイダーごとに異なります。
- ジョブ送信前に対象、shots、見積料金、キャンセル条件を確認してください。
- 資格情報を Notebook に記述しないでください。対話認証、マネージドID、サービスプリンシパルなど用途に合った認証を使います。
- 量子計算の結果は確率的です。乱数シード、shots、バックエンド、較正情報、日時を実験記録に残します。

## 重要なサービス上の注意

旧 Microsoft Quantum Inspired Optimization（QIO）ソルバーは 2023年6月30日以降 Azure Quantum で利用できません。したがって本教材では、廃止済みAPIではなく、再利用可能な QUBO 定式化、古典ベースライン、量子/量子インスパイアド実行先への移植方法を扱います。

## 参照日

本文の製品情報は **2026年10月5日** を基準にしています。クラウドサービスと研究ロードマップは変化するため、利用前に本文末尾の公式リンクを再確認してください。
