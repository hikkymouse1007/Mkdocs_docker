# MkDocs_Docker
## ソース
- https://hub.docker.com/r/squidfunk/mkdocs-material
- https://github.com/squidfunk/mkdocs-material
## 使い方
1. 公式docker imageを入手

```
docker pull squidfunk/mkdocs-material:latest
```

2. mkdocs.ymlの編集と*.mdファイルの作成

markdownの構造設定については公式githubのソースを参考に
```
// ディレクトリ構造
── docs
│   ├── index.md
│   ├── page1.md
│   └── page2.md
└── mkdocs.yml
```

3. dockerコマンドでlocalhost立ち上げ or ドキュメントのビルド

```
//localhost:8000
docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material
```

```
//build
docker run --rm -it -v ${PWD}:/docs squidfunk/mkdocs-material build
```



