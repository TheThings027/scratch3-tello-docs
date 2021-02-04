---
title: 環境構築
weight: 10
---

# 環境構築
Scratch3-Tello は Scratch に用意された拡張機能の仕組みだけでは動作していません。具体的には、Scratch を構成する `scratch-vm`, `scratch-gui`, `scratch-desktop` に変更を加えています。  
`scratch3-tello` リポジトリにはそれらの変更を行った差分がファイル単位で格納されています。そのため、このリポジトリをクローンしただけではビルドすることができません。

## 作業用フォルダの作成
```bash
$ mkdir scratch3-tello
$ cd scratch3-tello
```

## 環境構築用スクリプトをダウンロードする
```bash
$ wget https://raw.githubusercontent.com/kebhr/scratch3-tello/master/build.sh
$ chmod +x build.sh
```

## 環境構築用スクリプトを実行する
```bash
$ ./build.sh
```
`build.sh` を実行することで、自動的に `scratch-vm`, `scratch-gui`, `scratch-desktop` がクローンされ、`scratch3-tello` で管理されている差分のファイルが適用されます。

## Scratch3-Tello の起動
```bash
$ cd scratch-desktop
$ npm run build-gui
$ npm start
```

## パッケージを作成
```bash
$ cd scratch-desktop
$ npm run dist:dir
```