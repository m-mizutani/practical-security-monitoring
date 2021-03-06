# セキュリティ監視の高度化

原則として「誰がやっても同じ結果になるもの」はなるべき機械にやらせるようにする

## 分析の自動化

関連情報の収集を自動化する

- 一般公開されている情報
    - VirusTotal, HybridAnalysis, urlscan, X Force Exchange, etc...
    - APIを使って関連するIPアドレス、
- 内部の情報
    - 資産管理ツールを使うことでアクセス元のIPアドレスのデバイス所有者などがわかる
    - 社内のサービスのログを追うことで、当該IPアドレスからどのようなサービスを利用していたかがわかる

## リスク評価の自動化

- 過去に影響なしと判断したものは、未来も同様の基準で影響なしと判断できるはず
    - 同じ入力に対して同じ出力になるならルール化＋自動化する
- 外的変化（例えば新たな脆弱性の発生）によってリスク判断の基準が変わる可能性はもちろんある
    - あるが、それは外的変化をちゃんととらえるべきで、影響のないアラートを延々と見つけることで発見されるべきではない
    - 外的変化があったときに適切にルールを見直すことが大切

## 異常検知

- すべてのカテゴリに対していい感じに異常検出する、は激むずだが、特定のポイントに絞れば無理ではない
- 「定常状態」を正しく定義でいることが必須
- 具体例