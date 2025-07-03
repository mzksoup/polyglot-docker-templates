# 🐳 Python Docker Template

VS Code Dev Containers + Docker Compose を活用した Python 開発環境テンプレートです。

## 📦 セットアップ方法

### 方法 ①：VS Code Dev Containers（推奨）

1. 拡張機能「Dev Containers」をインストール
2. このフォルダを VS Code で開く
3. `Reopen in Container` を実行
4. 初回起動で `main.py` が実行されます

### 方法 ②：Docker Compose

```bash
docker compose up --build
```

## Structure
```
python/  
├── .devcontainer/  
│ └── devcontainer.json  
├── Dockerfile  
├── requirements.txt  
├── main.py  
└── .gitignore
```
