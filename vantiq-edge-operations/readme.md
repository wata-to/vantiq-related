## 目的

こちらの手順は、コンテナ版のVantiq Edgeを本番環境にて動作させるための手順として案内します。JAR形式でのご提供もございますので、必要に応じて担当者にご相談下さい。


## 本番環境向け

こちらの手順は、本番環境にて動作させるための手順としてDocker Engineをインストールする手順を案内します。

- [Install Docker Engine](https://docs.docker.com/engine/install/)

> **注意**
> Docker DesktopはDocker社の有償プランの対象となります。

## テスト目的の方向け

様々な環境にてお試し頂けます。

- [Windows 10/11](https://github.com/fujitake/vantiq-related/blob/main/vantiq-introduction/infrastructure-cloud/vantiqedge-on-windows/readme.md)
- macOS Intelではpodmanなどを使うことで動作することを確認しております。
- macOS m1にてLimaやpodmanなどではコンテナ版Vantiq edge(amd64)は`動作しない`ことを確認しております。

> **注意**
> Apple Siliconのmacにつきましては、LimaやPodmanを使うことでAMD64コンテナを動作させることができます。しかしながらこの環境ではVantiq Edgeは動作しないことを確認しております。



## Vantiq Edge のインストール手順

- [Vantiq Edgeインストール手順(r1.36まで)](https://community.vantiq.com/wp-content/uploads/2022/06/edge-install-ja-2.html)
- [Vantiq Edgeインストール手順(r1.37以降)](./docs/jp/setup_vantiq_edge_r137_w_LLM.md)

## Vantiq Edge のアップグレード手順

既存の環境をアップグレードする場合は、2つの選択肢がございます。

- ご利用環境の内容を継続して利用する場合: マイナーバージョンごとに、アップグレード作業をご対応頂く必要がございます。
(例: 1.33.1 -> 1.34.1、1.34.1 -> 1.35.1など)
- 既存環境を破棄し、新規でセットアップする場合: 現在の環境とは別のディレクトリにて新しくyamlをご用意頂き、
`docker compose up -d` を実行いただくとシンプルに作業頂けます。

> Vantiqは[セマンティックバージョニング](https://semver.org/lang/ja/)を採用しております。
