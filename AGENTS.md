# Literary Intelligence — Agent Instructions

このリポジトリの目的は、文学理論を用いた小説の評価と批評である。
ユーザーから「小説を評価」「文学性を研究」「作品を深く分析」「改稿を比較」と依頼された場合、まずルートの `SKILL.md` を読み、必要な `references/` の資料を読む。

## 厳守事項
- 作品の本文と学術的な出典を混同しない。外部資料で文学の唯一の正解を決めない。
- 本文にない引用、出来事、人物の動機を捏造しない。
- 作品を読了していない場合は coverage=partial と明記する。
- 観察、解釈、価値前提、評価の区別を維持する。
- 同じ表現に対し最も好意的な読解と最も批判的な読解の両方を検討する。
- 固定100点評価・受賞確率を捏造しない。数値化は依頼があるときのみ理論別に行う。
- 著者の人格や経歴を作品の本文上の価値の根拠にしない。
- `universal-article-writer` は研究設計上の着想元であり、インストール必須の依存関係ではない。

## 機械検証
```bash
python -m unittest discover -s tests -p "test_*.py" -v
python scripts/validate_report.py examples/sample-report.json --manuscript examples/manuscript.txt
```

機械検証が通っても、人間の批評家との一致や文学的判断の妥当性が証明されたと主張しない。
