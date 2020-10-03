# Dev Container Guidebook 正誤表

技術書典マーケットプレイス、Booth で電子版をお買い求めの方は、再ダウンロードいただくと修正済みの PDF がダウンロード可能です。

最終更新日 2020/10/04

## 技術書典 9 物理本

とらのあな委託書籍も該当します。

### P.42 Dockerfile

#### 誤

```
# 開発ツールのインストール
USER ${USERNAME}
RUN poetry install
```

#### 正

```
# 開発ツールのインストール
ARG USER_UID=1000
ARG USER_GID=$USER_UID
USER ${USERNAME}
RUN poetry install
```

### P.43 .devcontainer/devcontainer.json

#### 誤

```
    "dockerfile": "../Dockerfil実行e",
```

```
  // 実行ユーザ
  "remoteUser": "app"
```

#### 正

```
    "dockerfile": "../Dockerfile",
```

```
  // 実行ユーザ
  "remoteUser": "app"
```
