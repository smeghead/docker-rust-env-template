を作る# DockerでRustの開発環境のテンプレート #

https://qiita.com/toully/items/1b652bec2048eefd3130

## ビルド ##

Dockerfile を配置してビルドする。

```bash
docker build -t rust-env .
```

## カレントディレクトリをマウントしてログインする ##

```bash
docker run --rm -e USER=$USER -it -v $(pwd):/project -w /project rust-env
```

## プロジェクト作成 ##

```bash
cargo new <project-name> --bin
```

## コンパイルと実行 ##

```bash
cd <project-name>
cargo run
```
