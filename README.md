# ELK docker

## 使用說明

- 修改 `.env`
- `docker compose up -d`
- 重置 `kibana_system` 成 `.env` 設定的密碼（參照下方）
- 重啟 `kibana`

## 重置密碼

```shell
curl -u elastic:password -X PUT "http://localhost:9200/_security/user/kibana_system/_password" -H "Content-Type: application/json" -d '{ "password": "password" }'
```

## 參考資料

- [ELK v9 設定](https://www.ywbj.cc/?p=1544)
- [docker-elk repository](https://github.com/deviantony/docker-elk)
