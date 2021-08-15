# Minecraft Server Template
Dockerを用いたMinecraftサーバのテンプレート

## 動作要件
- `docker`, `docker-compose` コマンドを実行できる環境

## 設定
`docker-compose.yml` を編集する。
設定方法は [https://github.com/itzg/docker-minecraft-server](https://github.com/itzg/docker-minecraft-server) を参照。

## 操作
### 起動
```bash
docker-compose up -d
```

### 停止
```bash
docker-compose down
```

### コンテナ内でコマンド実行
```bash
docker exec -it mc sh
```

### サーバとインタラクト
```bash
docker exec -i mc rcon-cli
```

## 注意
Windowsの場合、Firewallで弾かれる場合がある。
受信の規則の `com.docker.backend` の通信を許可することで外部からアクセス可能になる可能性がある。
