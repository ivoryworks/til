# アクセストークンを発行する
## コマンドラインで
BASIC認証。アクセストークンはJSONで返される。  
作成されたトークンは、  
**Settings > Developer settings > Personal access tokens**  
で確認できる。
```bash
$ curl -u ivoryworks -d '{"scopes":["public_repo"], "note":"til authorization"}' https://api.github.com/authorizations
Enter host password for user 'ivoryworks':
```
結果
```json
{
  "id": 1234567,
  "url": "https://api.github.com/authorizations/1234567",
  "app": {
    "name": "til authorization",
    "url": "https://developer.github.com/v3/oauth_authorizations/",
    "client_id": "00000000000000000000"
  },
  "token": "d2387dx..........",
  "hashed_token": "606b10x..........",
  "token_last_eight": "kda034sn",
  "note": "til authorization",
  "note_url": null,
  "created_at": "2017-11-02T12:29:10Z",
  "updated_at": "2017-11-02T12:29:10Z",
  "scopes": [
    "public_repo"
  ],
  "fingerprint": null
}
```
