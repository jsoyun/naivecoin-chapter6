## 네이브코인 시각화함
# 서버 출처는 Naivecoin: chapter 6

#####

npm install
npm start
``
client에서도
npm install
npm start

## 1. 채굴해서 코인베이스 얻기
## 2. 보낼 금액 양 amount 보낼 지갑주소 address 적어서 sendTx 트랙잭션 풀에 보내기
## 3. 트랜잭션풀에 있는 값 채굴해서 Block에 넣기 
## 4. 난이도 올라가는 것 확인하려면 시간조건있음 서버 재실행후 10이상 채굴


##밑에는 기존 코드의 명령어

##### Get blockchain
```
curl http://localhost:3001/blocks
```

##### Mine a block
```
curl -X POST http://localhost:3001/mineBlock
``` 

##### Send transaction
```
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:3001/sendTransaction
```

##### Query transaction pool
```
curl http://localhost:3001/transactionPool
```

##### Mine transaction
```
curl -H "Content-type: application/json" --data '{"address": "04bfcab8722991ae774db48f934ca79cfb7dd991229153b9f732ba5334aafcd8e7266e47076996b55a14bf9913ee3145ce0cfc1372ada8ada74bd287450313534b", "amount" : 35}' http://localhost:3001/mineTransaction
```

##### Get balance
```
curl http://localhost:3001/balance
```

#### Query information about a specific address
```
curl http://localhost:3001/address/04f72a4541275aeb4344a8b049bfe2734b49fe25c08d56918f033507b96a61f9e3c330c4fcd46d0854a712dc878b9c280abe90c788c47497e06df78b25bf60ae64
```

##### Add peer
```
curl -H "Content-type:application/json" --data '{"peer" : "ws://localhost:6001"}' http://localhost:3001/addPeer
```
#### Query connected peers
```
curl http://localhost:3001/peers
```
