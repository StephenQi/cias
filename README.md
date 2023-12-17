# cias mint 脚本

## 感谢 [qzz0518](https://github.com/qzz0518/coss)

## 安装

```
yarn install
```

修改 .env.example 为 .env

## 配置环境变量

在项目根目录中创建 .env 文件，并填写以下信息：

```
# rpc配置, 从https://atomscan.com/directory/celestia找
NODE_URL=https://public-celestia-rpc.numia.xyz

# 主钱包私钥,用于转账
PRIVATE_KEY=

# 生成钱包配置,按需配置
NUM_OF_WALLETS=30
WALLET_JSON_FILE=wallets.json

# celestia配置
CHAIN_SYMBOL=celestia
TOKEN_DENOM=utia
TOKEN_DECIMAL=1000000

# 每个钱包转账多少个TIA,按需修改
TOKEN_TRANSFER_AMOUNT=1

# gas配置,一定要调整
GAS_PRICE=3000
GAS_LIMIT=100000

# mint配置, 一定要看官方参数
MINT_AMOUNT=10000
TICK=cias
PROTOCOL=
MINT_TIMES=100 # 每个钱包mint100次

```

## 钱包批量生成

```
node wallet_gen.js
```

代码里面可以调整生成的个数

## 批量转账

```
node transfer.js
```

请先执行批量生成，然后再执行批量转账, 默认往生成地址各转 1 个 TIA，请按需调整

## mint 运行

```
node mint.js
```
