# NucoNekoSan

> 業務改善とデータ活用を軸に、**実務で使える仕組みづくり**に取り組んでいます。
> 再現性のあるワークフロー設計と、分かりやすいドキュメント整備を重視しています。

📍 Sapporo, Hokkaido / 🐍 Python / 🌐 Django + HTMX

---

## 🚀 公開プロジェクト

### [**budgetbook-demo**](https://github.com/NucoNekoSan/budgetbook-demo) — 家計簿 + 確定申告レポート

Django + HTMX + PWA 製の自己ホスト型ファイナンスアプリ。**日次家計簿 + 個人 B/S + 確定申告レポート (国税庁様式)** を統合。サラリーマン世帯の確定申告（医療費控除・生命保険料控除・地震保険料控除・寄附金）の補助を 1 画面で完結できる設計。

- Tech: Django 5.2, HTMX, SQLite (WAL), Gunicorn + Nginx, Docker, PWA
- Tests: 500 件 (全 pass)
- License: MIT
- 設計判断: [docs/TECH_SPEC.md](https://github.com/NucoNekoSan/budgetbook-demo/blob/master/docs/TECH_SPEC.md) / [docs/SECURITY.md](https://github.com/NucoNekoSan/budgetbook-demo/blob/master/docs/SECURITY.md)

### [**dev-environment**](https://github.com/NucoNekoSan/dev-environment) — Python 開発環境ノート

Windows / macOS 両対応の **再現可能な Python 開発環境**構築手順。venv / PyCharm / pylint の運用方針をドキュメント化。

---

## 🛠 取り組んでいること

- **読書管理ツール**
  PowerApps・Power Automate・Excel・Access を用いて構築中。
  入力・管理・集計を業務ツールとしてまず成立させた上で、将来的にデータベース設計や分析機能を段階的に発展させていく予定です。

- **家計管理ツール** ([budgetbook-demo](https://github.com/NucoNekoSan/budgetbook-demo))
  Django・HTMX を用いて構築。月次集計や支出分析・確定申告レポートに使える形で整理し、段階的に設計を進めています。

※ 既存ツールで業務設計と要件整理を行い、必要に応じて技術移行していく方針を取っています。

---

## 🎯 スキル・経験領域

**業務系**
- 業務改善・運用設計
- PowerApps / Power Automate / Excel / Access

**開発系**
- Python / Django / Django CMS / FastAPI
- データ設計・集計・可視化
- HTML / CSS / HTMX
- Git / ドキュメント整備

**学習中**
- TypeScript / Next.js / Astro
- Tailwind CSS

※ 個人開発を通じて、必要に応じて段階的に習得していく方針です。

---

## 💭 仕事の進め方

- 過度な設計より、**シンプルで保守しやすい構成**を重視
- README・手順書・設定を整備し、**再現性を確保**
- 判断やプロセスを記録し、**属人化を避ける**運用
- セキュリティ・データ保護を最上位制約とする（個人金融データを扱う家計簿アプリの設計でも徹底）

---

## 📊 Status

- 個人プロジェクトを継続的に開発・学習中
- 2026 年は確定申告対応 (家計簿アプリ) と公開ポートフォリオ整備が中心