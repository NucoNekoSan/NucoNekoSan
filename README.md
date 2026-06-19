# NucoNekoSan

> 業務改善・データ活用・Web アプリ開発を軸に、**実務で使える仕組みづくり**に取り組んでいます。
> 要件整理から実装、Docker 運用、ドキュメント整備、保守しやすい改善サイクルまでを重視しています。

📍 Sapporo, Hokkaido / 🐍 Python / 🌐 Django + HTMX / ⚙️ FastAPI + Next.js / 🐳 Docker

---

## 👋 About me

業務改善や個人開発を通じて、日々の運用で実際に使えるアプリケーションを作っています。

特に、以下のような領域に関心があります。

- 現場の作業を整理し、入力・集計・確認・レポート化までつなげる業務アプリ開発
- 個人情報や金融データを扱う前提でのセキュリティ、バックアップ、復旧、運用設計
- Django / FastAPI / PostgreSQL / Docker を使った自己ホスト型 Web アプリ構築
- README、運用手順、ADR、引継ぎ文書を含めた再現性のある開発
- AI を補助的に活用しながら、最終判断・検証・品質担保は人間が行う開発フロー

---

## 🚀 公開プロジェクト

### [**budgetbook-demo**](https://github.com/NucoNekoSan/budgetbook-demo) — 家計簿 + 個人 B/S + 確定申告レポート

Django + HTMX + PWA 製の自己ホスト型ファイナンスアプリ。**日次家計簿、個人バランスシート、月次締め、確定申告レポート**を統合しています。

- 🌐 **ライブデモ**: https://budgetbook-demo-static.nuconekosan.workers.dev/  
  Cloudflare 配信の静的スナップショットとして公開。Django ランタイムは公開せず、攻撃面を抑えたデモ構成です。
- Tech: Django 5.2, HTMX, SQLite WAL, Gunicorn + Nginx, Docker, PWA
- Tests: 545+ passing
- License: MIT
- 設計判断: [docs/TECH_SPEC.md](https://github.com/NucoNekoSan/budgetbook-demo/blob/master/docs/TECH_SPEC.md) / [docs/SECURITY.md](https://github.com/NucoNekoSan/budgetbook-demo/blob/master/docs/SECURITY.md)

### [**budgetbook-demo-static**](https://github.com/NucoNekoSan/budgetbook-demo-static) — ライブデモの静的化基盤

`budgetbook-demo` から静的 HTML を生成し、Cloudflare で 24/7 公開する仕組みです。**公開デモは静的化し、動的アプリ本体は公開しない**という設計で、セキュリティと見やすさを両立しています。

---

## 🛠 現在取り組んでいるプロジェクト

### **nuconeko-garden** — Django CMS ベースの個人メディア基盤

Django CMS / PostgreSQL / Docker / Nginx / Gunicorn を使った個人ブログ・情報発信基盤です。
開発環境での主要実装は完了し、本番サーバー準備待ちの状態です。

- 目的: メンタルヘルス、キャリア、技術学習、書評などを継続発信するメディア基盤
- 重視点: CMS 運用、Docker 化、本番想定の設定分離、ドキュメント整備

### **BudgetBook** — 個人利用中の家計・税務補助アプリ

公開版 `budgetbook-demo` の元になっている個人運用プロジェクトです。
月次締め、家計分析、確定申告補助、PWA 化、AI 分析補助などを継続改善しています。

- 2026-05 月締め済み
- PWA / Docker / Host 設定 / ポート管理 / 運用前チェックを整備
- 個人金融データを扱う前提で、バックアップ・復旧・安全な公開範囲を重視

### **BookForge** — 読書・蔵書管理アプリ

FastAPI + Next.js + PostgreSQL + Docker Compose で構築している個人利用中の読書管理アプリです。
ISBN 検索、蔵書管理、読書状態、タグ、メモ、外部 API 連携、運用手順の整備を進めています。

- 個人利用で運用中
- API / Web / DB を Docker Compose で分離
- ポート衝突回避、DB バックアップ、マイグレーション、引継ぎ文書を整備

### **Local-BI-Tool** — ローカル完結型 BI / 診断メモ基盤

中小企業の売上・粗利・顧客・商品データを、ローカル環境で分析するための BI ツールです。
AI がなくても、取込・検証・分析・診断メモ・レポート下書きが成立する設計を目指しています。

- Backend: ASP.NET Core
- Frontend: Next.js + TypeScript
- Analysis Service: FastAPI + pandas
- DB: PostgreSQL / DuckDB optional
- 方針: クライアント実データ、秘密情報、DB、exports、ログを Git 管理しない

---

## 🎯 スキル・経験領域

**業務改善・運用設計**
- 業務フロー整理、入力設計、集計、レポート化
- Excel を使ったデータ整理・集計・業務補助
- 手順書、運用ルール、引継ぎ文書、復旧手順の整備

**Web アプリ開発**
- Python / Django / Django CMS / FastAPI
- PostgreSQL / SQLite / DuckDB
- HTML / CSS / HTMX / PWA
- Docker / Docker Compose / Nginx / Gunicorn

**学習・拡張中**
- Access / PowerApps / Power Automate
- TypeScript / Next.js
- ASP.NET Core / .NET
- Tailwind CSS
- ローカル BI、データ分析、AI 補助ワークフロー

---

## 💭 仕事の進め方

- まず動くものを作り、運用しながら改善する
- 過度な抽象化より、**シンプルで保守しやすい構成**を優先する
- README、手順書、設定、検証コマンドを残し、**再現性を確保**する
- セキュリティ、個人情報、秘密情報、バックアップを最初から設計に含める
- エラーや失敗を記録し、次の運用改善につなげる

---

## 📊 Current status

- 就職活動に向けて、公開ポートフォリオと運用中プロジェクトを整理中
- `nuconeko-garden` は本番サーバー準備待ち
- `BudgetBook` と `BookForge` は個人利用を続けながら改善中
- `Local-BI-Tool` はローカル完結型 BI として段階的に実装中
