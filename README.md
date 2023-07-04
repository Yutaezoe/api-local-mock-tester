# Install
npm init --yes  
npm install --save-dev json-server


# RestApi Mock Server
## 起動
node index.js

## モックコマンド(Curl)
URLパラメタあり
curl -X GET 'http://localhost:8000/test?test=123'

なし
curl -X GET 'http://localhost:8000/posts'

正常
curl -X POST -H "Content-Type: application/json" -d '{"name": "John", "age": 30}' "http://localhost:8000/test"

異常
curl -X POST -H "Content-Type: application/json" -d '{"age": 30}' "http://localhost:8000/test"

正常
curl -X PUT -H "Content-Type: application/json" -d '{"id": 1, "name": "John", "age": 30}' "http://localhost:8000/test"

異常
curl -X PUT -H "Content-Type: application/json" -d '{"name": "John", "age": 30}' "http://localhost:8000/test"


