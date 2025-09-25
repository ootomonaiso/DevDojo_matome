# GitHub Copilot Instructions

## Project Overview
このリポジトリは、Docusaurusを使用して構築されたドキュメントサイトテンプレートです。
人に配布するためのテンプレートプロジェクトとして設計されており、簡単にカスタマイズできるように設定されています。

## Technical Specifications
- 使用言語: TypeScript, Markdown
- フレームワーク: Docusaurus 3.8.1 (React 18.0 上に構築)
- buildツール: Node.js v20.11.0
- デプロイ: GitHubActionsでビルドしてGitHubPagesに自動デプロイ
- 文字エンコーディング: UTF-8
- 国際化: 日本語 (ja) デフォルト

## Project Structure
```
devdojo-practice/              # Docusaurusメインプロジェクト
├── docs/                      # ドキュメントMarkdownファイル
├── blog/                      # ブログ記事Markdownファイル
├── src/components/            # Reactカスタムコンポーネント
├── src/css/                   # カスタムCSS
├── src/pages/                 # カスタムページ
├── static/img/                # 静的画像ファイル
├── docusaurus.config.ts       # メイン設定ファイル（カスタマイズ必須）
├── sidebars.ts               # サイドバー構成設定
└── package.json              # 依存関係管理

.github/workflows/deploy.yml   # GitHubActions自動デプロイ設定
README.md                     # 使用者向けドキュメント
```

## Development Guidelines
### ファイル編集時の注意点
- ファイル編集時は必ず3-5行の前後コンテキストを含める
- パス指定は必ず `devdojo-practice/` から開始する
- 設定変更時は `docusaurus.config.ts` の関連コメントを確認する

### 主要カスタマイズポイント
1. **docusaurus.config.ts** - サイト設定、URL設定、GitHubリンク設定
2. **docs/intro.md** - メインドキュメントのエントリーポイント
3. **blog/** - ブログ記事コンテンツ
4. **src/components/HomepageFeatures/** - ホームページのフィーチャー表示
5. **src/css/custom.css** - サイト全体のスタイルカスタマイズ

### GitHubPages対応設定
- url: `https://ユーザー名.github.io`
- baseUrl: `/リポジトリ名/`
- organizationName: GitHubユーザー名
- projectName: GitHubリポジトリ名
- editUrl: 実際のリポジトリの編集URL

## Coding Conventions
- 使用言語: TypeScript, Markdown
- 日本語でコメント文を記述
- 絵文字の使用禁止（コード内、コメント内、回答内すべて）
- クラス、関数、コンポーネントごとにコメント文を記述
- インデントはスペース2つ
- セミコロン必須

## 回答について
- 回答は日本語を使用
- 絵文字は一切使用しない
- 技術用語は適切な日本語訳を使用
- コード例には詳細なコメントを含める
- ファイルパスは絶対パスで記述

## Development Workflow
1. `cd devdojo-practice && npm start` でローカル開発サーバー起動
2. `http://localhost:3000` でプレビュー確認
3. `mainブランチ` へのプッシュで自動デプロイ実行
4. `https://ユーザー名.github.io/リポジトリ名/` で公開サイト確認

## Common File Patterns
- 設定ファイル: `devdojo-practice/docusaurus.config.ts`
- ドキュメント: `devdojo-practice/docs/**/*.md`
- ブログ記事: `devdojo-practice/blog/**/*.md`
- Reactコンポーネント: `devdojo-practice/src/components/**/*.tsx`
- スタイルシート: `devdojo-practice/src/css/custom.css`
- 静的ファイル: `devdojo-practice/static/**/*`

## Important Notes
- このプロジェクトは配布用テンプレートです
- 各ユーザーが自分の環境に合わせてカスタマイズする前提
- GitHubPages用のURL設定は必須変更項目
- 自動デプロイは `devdojo-practice/` フォルダ変更時のみ実行
- Markdownファイルは日本語文字化け対策済み

