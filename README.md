# Personal Management

GitHub + Claude Code による個人タスク管理・日記・ナレッジベース。

## 構成

| 機能 | 仕組み |
|---|---|
| タスク管理 | GitHub Issues + Projects (GTD) |
| 日記・日報 | Issue コメント → Actions で Markdown 自動変換 |
| ナレッジベース | `knowledge/` に Claude Code で整理 |

## フォルダ構成

```
blog/           # GitHub Actions が自動生成（触らない）
knowledge/
  tech/         # 技術メモ
  books/        # 読書メモ
  goals/        # 目標・OKR
  habits/       # 習慣管理
```

## ラベル設計

| ラベル | 用途 |
|---|---|
| `task` | 通常タスク |
| `diary` | 日報Issue（1日1つ） |
| `recurring` | 定期タスク |
| `knowledge` | ナレッジ化対象 |

## 日報の使い方

1. 毎朝「今日の日報」Issueを作成（ラベル: `diary`）
2. iPhoneからコメントで随時メモを追記
3. 毎日0時に Actions が `blog/YYYY/MM/YYYY-MM-DD.md` へ自動変換
