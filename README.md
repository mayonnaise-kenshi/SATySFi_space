# SATySFiのベースのdevcontainer
です．

## 使い方
forkしてください．

[Container Image (latest)](https://github.com/mayonnaise-kenshi/SATySFi_space/pkgs/container/satysfi-space)

## memo

 - [ベースイメージ](https://github.com/amutake/docker-satysfi)
 - [D論書いた人](https://qiita.com/shoudai7856/items/2f7a19f7bc56a49ed3ee)
 - [SATySFiベストプラクティス](https://zenn.dev/monaqa/articles/2022-04-27-satysfi-bestpractice)

[opamでインストールしたアプリにPATHを通す](https://github.com/ocaml/opam/issues/3648)

## 記法memo

[SATySFiのコマンド記法](https://zenn.dev/monaqa/articles/2020-12-10-satysfi-for-beginner-command-syntax)
コマンド自体はLaTeX互換だから基本的にはLaTeXのコマンド見ればよい．

## パッケージ

 - [azmath](https://github.com/monaqa/satysfi-azmath) [参考](https://zenn.dev/monaqa/articles/2020-12-24-satysfi-2020-plugins)
 - [figbox](https://zenn.dev/monaqa/articles/2022-04-27-satysfi-bestpractice#%E5%9B%B3%E3%81%AE%E6%8C%BF%E5%85%A5)
 - [easytable](https://zenn.dev/monaqa/articles/2022-04-27-satysfi-bestpractice#%E8%A1%A8%E3%81%AE%E6%8C%BF%E5%85%A5)
 - [BiByFi](https://zenn.dev/monaqa/articles/2022-04-27-satysfi-bestpractice#%E5%8F%82%E8%80%83%E6%96%87%E7%8C%AE%E3%81%AE%E6%8C%BF%E5%85%A5) 
 
## その他アプリ

 - [.bibからBiByFiの形式に変換するソフト](https://github.com/puripuri2100/BibSATySFi/blob/master/doc/doc-ja.md)←ビルドできないので後で...
 - [SATySFi LSP](https://zenn.dev/monaqa/articles/2021-12-10-satysfi-language-server)
 - fish

https://community.forallsecure.com/t/error-buildx-call-failed-with-error-denied-installation-not-allowed-to-write-organization-package/354
### LSPのマルチステージビルド
busterのイメージなら，.soが同じなので，あまり気にせずバイナリを持ってきていいみたい．[Rustでマルチステージビルドしてる例](https://zenn.dev/ucwork/articles/acec204571362b)

[Cargoでバイナリを指定場所にインストールする方法](https://maku77.github.io/p/owbo2dp/)

### pdfのプレビュー
```tomoki1207.pdf```をローカルのVSCodeに入れる．(ブラウザ上だと動かないので，ローカルのVSCodeから繋ぐ)

## Actions
[リポジトリをpull→build→ghcr.ioにpush](https://zenn.dev/515hikaru/articles/migrate-to-ghcr)
[イメージをghcr.ioに上げる場合，リポジトリのActionsにwrite権限を付与する必要がある](https://community.forallsecure.com/t/error-buildx-call-failed-with-error-denied-installation-not-allowed-to-write-organization-package/354)
