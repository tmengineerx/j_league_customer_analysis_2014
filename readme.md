## ディレクトリ構成

project_root/
├── data/
│   ├── raw/                # 生データ（ダウンロードしたデータをそのまま保存）
│   ├── processed/          # 前処理済みデータ
│   └── external/           # 外部データ（例: 他のデータセットや補助的なデータ）
├── notebooks/              # Jupyter Notebook ファイル
├── src/                    # Python スクリプト（データ処理や分析用）
│   ├── __init__.py         # Python モジュールとして扱うためのファイル
│   ├── data_processing.py  # データ前処理用スクリプト
│   ├── visualization.py    # 可視化用スクリプト
│   └── modeling.py         # モデル作成・評価用スクリプト
├── outputs/                # 分析結果（グラフ、モデル、レポートなど）
│   ├── figures/            # グラフや可視化結果
│   ├── models/             # 保存したモデル
│   └── reports/            # レポートや結果のまとめ
├── requirements.txt        # 必要なPythonライブラリのリスト
├── README.md               # プロジェクトの概要説明
└── .gitignore              # Gitで無視するファイルやフォルダ

---

## それぞれのデータの情報の整理

### train, train_add columns
- **id** : 試合管理ID
- **y** : 観客動員数(目的変数)
- **year** : 試合の開催年
- **stage** : 所属リーグ(J1, J2)
- **match** : 試合日程情報
- **gameday** : 試合日
- **time** : キックオフ時間
- **home** : ホームチーム(開催スタジアムを本拠地とするチーム)
- **away** : アウェイチーム
- **stadium** : 開催スタジアム名
- **tv** : 試合のLIVE放送サービス

---

### condition, condition_add columns
- **id** : 試合管理ID
- **home_score** : ホームチームのスコア
- **away_score** : アウェイチームのスコア
- **weather** : 天気
- **temperature** : 気温
- **humidity** : 湿度
- **referee** : メイン審判名
- **home_team** : ホームのチーム名
- **home_01~home_11** : ホームチームのスターティングメンバー
- **away_01~away_11** : アウェイチームのスターティングメンバー

---

### stadium columns
- **name** : スタジアム名
- **address** : スタジアムの住所
- **capa** : スタジアムの収容人数