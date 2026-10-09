# MemNotch releases

MacBook のノッチを使う社内向けアプリ **MemNotch** の配布用リポジトリです。ここにはビルド済みのアプリ（zip）だけを置いています。

MemNotch は [NotchDrop](https://github.com/Lakr233/NotchDrop)（MIT License, Copyright (c) 2024 Lakr Aream）をもとにしています。

## 必要なもの

- macOS 14 以降

## インストール

### Homebrew（おすすめ）

```sh
brew tap mem-shibata/memnotch
brew trust --tap mem-shibata/memnotch   # Homebrew にこの tap を信頼させる設定
brew install --cask memnotch
```

### zip

[Releases](https://github.com/mem-shibata/MemNotch-releases/releases/latest) から `MemNotch-<バージョン>.zip` をダウンロードして展開し、`MemNotch.app` を「アプリケーション」フォルダに入れます。

Apple の公証を受けていないため、最初の起動で「開発元を確認できません」と表示されます。Finder で MemNotch を右クリックし、「開く」を選んでください。

## 更新

新しい版が出ると、MemNotch のノッチの見出しに「新しいバージョンがあります」と表示されます。

```sh
brew upgrade --cask memnotch
```

MemNotch は自動で終了し、更新のあとに起動し直します。zip の場合は、MemNotch を終了してから上書きしてください。どちらの場合も、データ（トレイ・ToDo・メモ・設定）は残ります。

## 通信について

MemNotch が外部と通信するのは、新しい版が出ていないかを確認するとき（起動時と1日1回、このリポジトリの最新リリースを GitHub API に問い合わせる）だけです。トレイのファイル、予定、メモなどの内容を送ることはありません。
