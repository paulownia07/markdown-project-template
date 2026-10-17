# Markdown Project Template

## 概要

Markdown文書を中心に作成・管理するプロジェクト向けのGitHubテンプレートです。Dev ContainerとVS CodeのMarkdown編集環境をあらかじめ用意し、ドキュメント作成をすぐに始められます。

## 主な機能

- Dev ContainerによるUbuntuベースの開発環境
- VS CodeのMarkdown編集・プレビュー・整形用拡張機能
- GitHub Issue／Pull Requestテンプレート
- GitHub Copilot向けのリポジトリ指示とスキル

このテンプレートには、uv、pytest、RuffなどのPython開発ツールや設定は含まれていません。Pythonを扱う場合は、必要に応じて「[カスタマイズ方法](#カスタマイズ方法)」の手順で追加してください。

## 前提条件

- Git
- Docker Desktopなど、Dev Containerを実行できるDocker環境
- Visual Studio Code
- VS Code拡張機能「Dev Containers」
- テンプレートからリポジトリを作成する場合は、GitHubアカウント

## 使用方法

1. GitHubでこのリポジトリを開き、**Use this template** を選択します。
2. 新しいリポジトリ名や公開範囲を指定して、**Create repository from template** を選択します。
3. 作成したリポジトリをローカルにクローンします。

   ```sh
   git clone <作成したリポジトリのURL>
   ```

4. VS Codeでクローンしたフォルダーを開きます。
5. 表示された案内、またはコマンドパレットの **Dev Containers: Reopen in Container** からコンテナを起動します。

## ディレクトリ構成

```text
.
├── .devcontainer/
│   ├── Dockerfile          # 開発コンテナのベースイメージと環境
│   └── devcontainer.json   # コンテナ起動設定とVS Code拡張機能・設定
├── .github/
│   ├── ISSUE_TEMPLATE/     # Issueの種類別テンプレート
│   ├── skills/             # Copilot向けの作業スキル
│   ├── copilot-instructions.md　# リポジトリ共通のCopilot向け指示          
│   └── pull_request_template.md　# Pull Requestテンプレート
│ 
├── docs/
│   └── sample.md           # 文書作成用のサンプル
├── .gitignore              # Gitの追跡対象外にするファイル
└── README.md               # プロジェクトの説明と開発手順
```

## カスタマイズ方法

- **プロジェクト名や説明**: このREADMEのタイトルと「概要」を、作成するプロジェクトに合わせて変更します。
- **文書**: `docs/`にMarkdownファイルを追加し、`docs/sample.md`は必要に応じて編集または削除します。
- **VS Code環境**: `.devcontainer/devcontainer.json`で拡張機能やエディター設定を、`.devcontainer/Dockerfile`で開発環境を変更します。
- **Python依存関係**: Python開発を行う場合は、開発手順の例を参考にuv、pytest、Ruffを追加し、`pyproject.toml`の設定をプロジェクトに合わせます。
- **GitHubの運用**: `.github/ISSUE_TEMPLATE/`、`.github/pull_request_template.md`、`.github/copilot-instructions.md`をチームの運用に合わせて変更します。
