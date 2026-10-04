# elasticsearch-playground

Elasticsearch と Kibana をローカルの Docker で動かして、使い方を試すためのリポジトリです。

## 構成

| サービス | バージョン | URL |
|---|---|---|
| Elasticsearch | 9.5.4 | http://localhost:9200 |
| Kibana | 9.5.4 | http://localhost:5601 |

- ライセンス: Basic（無料）
- セキュリティ: 無効（ローカル検証用のため認証なし）

## 必要なもの

- Docker（Docker Desktop にメモリを 4GB 以上割り当てる）

## 使い方

起動:

```bash
docker compose up -d
```

停止:

```bash
docker compose down
```

データも含めて削除:

```bash
docker compose down -v
```

## 動作確認

Kibana の Dev Tools で次のリクエストを実行し、`"type": "basic"` になっていることを確認します。

```
GET _license
```

## 注意

- 認証を無効にしているため、信頼できるネットワーク（自宅など）でのみ使う
- 外出先では `docker compose down` で停止しておく
