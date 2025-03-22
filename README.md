# intercept-booster-2

[![Node.js CI](https://github.com/k2works/intercept-booster-2-sample/actions/workflows/node.js.yml/badge.svg)](https://github.com/k2works/intercept-booster-2-sample/actions/workflows/node.js.yml)
[![Deploy Documentation to GitHub Pages](https://github.com/k2works/intercept-booster-2-sample/actions/workflows/deploy-docs.yml/badge.svg)](https://github.com/k2works/intercept-booster-2-sample/actions/workflows/deploy-docs.yml)

## 概要

[ガイドライン](./docs/slides/PITCHME.md)

### 目的

### 前提

| ソフトウェア | バージョン | 備考 |
| :----------- |:------| :--- |
| nodejs       | 20.x  |      |

### Quick Start

```bash
npm install
npm start
```
## 構成

- [要件](./docs/req.adoc)
- [開発](./docs/dev.adoc)
- [構築](./docs/build.adoc)
- [配置](./docs/ship.adoc)
- [運用](./docs/run.adoc)

## Wiki

プロジェクトのドキュメントはWiki.jsとMkDocsを使用して管理・公開されています。

### ローカルでのWikiセットアップ手順

#### 前提条件

- Docker と Docker Compose がインストールされていること
- Git がインストールされていること

#### セットアップ手順

1. リポジトリをクローンする
   ```bash
   git clone https://github.com/k2works/intercept-booster-2-sample.git
   cd intercept-booster-2-sample
   ```

2. Wikiリポジトリをクローンする
   ```bash
   mkdir -p docs/wiki
   git clone https://github.com/k2works/intercept-booster-2-sample.wiki.git docs/wiki
   ```

3. Dockerサービスを起動する
   ```bash
   # Wiki.js、データベース、PlantUML、MkDocsのすべてのサービスを起動
   docker compose up -d wiki_db wiki plantuml mkdocs

   # MkDocsのみを起動する場合
   docker compose up -d plantuml mkdocs
   ```

#### Wikiの利用方法

1. **Wiki.jsにアクセスする**
   - ブラウザで http://localhost にアクセス
   - 初回アクセス時は管理者アカウントの設定が必要

2. **MkDocsでドキュメントを閲覧する**
   - ブラウザで http://localhost:8000 にアクセス
   - MkDocsはWikiの内容を静的サイトとして表示

3. **コンテンツの編集**
   - Wiki.js UIを使用して直接編集
   - または `docs/wiki` ディレクトリ内のMarkdownファイルを直接編集

4. **変更の反映**
   - Wiki.jsで編集した内容は自動的にMkDocsに反映されます
   - ファイルを直接編集した場合は、変更をWikiリポジトリにプッシュする必要があります

詳細については [Wiki README](/docs/wiki/README.md) を参照してください。

## 参照

- [Conventional Commits 1.0.0](https://www.conventionalcommits.org/ja/v1.0.0/)
- [@k2works/intercept-booster-2](https://www.npmjs.com/package/@k2works/intercept-booster-2)
- [@k2works/full-stack-lab](https://www.npmjs.com/package/@k2works/full-stack-lab)
- [@k2works/adr](https://www.npmjs.com/package/@k2works/adr)
- [Gulp](https://gulpjs.com/docs/en/getting-started/quick-start)
- [Asciidoctor](https://asciidoctor.org/)
- [Browsersync](https://browsersync.io/)
- [Marp](https://marp.app/)
- [Wiki.js](https://js.wiki/)
- [MkDocs](https://www.mkdocs.org/)
