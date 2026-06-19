# NucoNekoSan

> 業務改善・データ活用・AI 支援開発を軸に、**実務で使える仕組みづくり**に取り組んでいます。
> 要件整理、スペック駆動開発、AI コーディングエージェント活用、Docker 運用、ドキュメント整備、保守しやすい改善サイクルを重視しています。

📍 Sapporo, Hokkaido / 🐍 Python / 🧭 Spec-driven Development / 🤖 AI Coding Agents / 🐳 Docker

---

## 👋 About me

業務改善や個人開発を通じて、日々の運用で実際に使えるアプリケーションを作っています。

特に、以下のような領域に関心があります。

- 現場の作業を整理し、入力・集計・確認・レポート化までつなげる業務アプリ設計
- 個人情報や金融データを扱う前提でのセキュリティ、バックアップ、復旧、運用設計
- AI コーディングエージェントを活用した Web アプリの実装・検証・改善
- README、運用手順、ADR、引継ぎ文書を含めた再現性のある開発
- AI の出力をそのまま採用せず、要件・動作確認・品質担保を人間側で管理する開発フロー

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
- 技術: Python, Django, django CMS, PostgreSQL, Tailwind CSS, Docker Compose, Nginx, Gunicorn
- 重視点: CMS 運用、Docker 化、本番想定の設定分離、ドキュメント整備

### **BudgetBook** — 個人利用中の家計・税務補助アプリ

公開版 `budgetbook-demo` の元になっている個人運用プロジェクトです。
月次締め、家計分析、確定申告補助、PWA 化、AI 分析補助などを継続改善しています。

- 月次締め、残高照合、支出分析、確定申告補助の運用フローを整備
- 技術: Python, Django, HTMX, SQLite, PWA, Docker, Cloudflare Tunnel / Access
- 個人金融データを扱う前提で、バックアップ・復旧・安全な公開範囲を重視

### **BookForge** — Obsidian 連携型の読書学習・蔵書管理アプリ

FastAPI + Next.js + PostgreSQL + Docker Compose で構築している、読書を知識・人生・仕事の資産に変えるための個人利用アプリです。
蔵書管理だけでなく、読了後の問いへの回答、章ノート、Obsidian への保存までを一連の読書学習フローとして扱います。

- 北極星: 読み終わった本を「要約・学び・アクション」の 3 つの問いで整理し、Obsidian に知識資産として保存
- 技術: Python, FastAPI, Next.js, TypeScript, PostgreSQL, Alembic, Docker Compose
- Obsidian の手書き部分を壊さない managed marker / 非破壊更新 / 回帰テストを重視
- API / Web / DB を分離し、バックアップ、マイグレーション、引継ぎ文書を整備

### **Local-BI-Tool** — ローカル完結型 BI / 診断メモ基盤

中小企業の売上・粗利・顧客・商品データを、ローカル環境で分析するための BI ツールです。
AI がなくても、取込・検証・分析・診断メモ・レポート下書きが成立する設計を目指しています。

- Backend: ASP.NET Core / .NET
- Frontend: Next.js + TypeScript（技術前提。README 上の現在実装範囲では未着手）
- Analysis Service: Python + FastAPI + pandas
- DB: PostgreSQL / DuckDB optional
- 方針: クライアント実データ、秘密情報、DB、exports、ログを Git 管理しない

---

## 🎯 経験・取り組み領域

**業務改善・運用設計**
- 業務フロー整理、入力設計、集計、レポート化
- Excel を使ったデータ整理・集計・業務補助
- 手順書、運用ルール、引継ぎ文書、復旧手順の整備

**AI コーディング / エージェント活用**
- スペック駆動開発: 要件、仕様、受け入れ条件、実装順序を文書化してから進める
- AI コーディングエージェントの利用: タスク分解、実装、調査、リファクタリング、検証の指示設計
- Skill / agentic workflow の活用: 作業ごとに適切なツール・手順・検証観点を切り替える
- 生成コードのレビュー: 動作確認、エラー調査、ログ確認、差分確認、修正方針の判断
- 運用前チェック: Docker 起動確認、ポート衝突確認、ヘルスチェック、バックアップ・復旧手順確認

**プロジェクトで採用・検証している技術**
- Python / Django / Django CMS / FastAPI
- TypeScript / Next.js
- ASP.NET Core / .NET
- PostgreSQL / SQLite / DuckDB
- HTML / CSS / HTMX / PWA / Tailwind CSS
- Docker / Docker Compose / Nginx / Gunicorn / Cloudflare Tunnel / Cloudflare Access

**現在深掘りしているテーマ**
- AI 支援開発の進め方: spec、agent、skill、検証手順の組み立て
- ローカル BI: データ取込、検証、分析、診断メモ、レポート下書きの設計
- 個人情報・金融データ・クライアントデータを扱うアプリの安全な運用設計
- Access / PowerApps / Power Automate

---

## 💭 仕事の進め方

- まず動くものを作り、運用しながら改善する
- AI の提案を前提にしつつ、要件・安全性・動作確認は自分で検証する
- 技術そのものを過大に見せず、実際に担った要件整理・検証・運用改善を明確にする
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
