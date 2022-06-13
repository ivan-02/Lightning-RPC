Bitcoin.conf

testnet=1
server=1
rpcuser=1234
rpcpassword=1234
zmqpubrawblock=tcp://127.0.0.1:18502
zmqpubrawtx=tcp://127.0.0.1:18503
addresstype=p2sh-segwit

lnd.conf

debuglevel=info
listen=127.0.0.1:9735
externalip=192.168.0.18
rpclisten=0.0.0.0:10009
restlisten=0.0.0.0:10013
tlsextraip=192.168.0.18
alias=test
color=#ffdc00
maxpendingchannels=10
bitcoin.testnet=1
bitcoin.active=1
bitcoin.node=bitcoind
bitcoind.rpcuser=1234
bitcoind.rpcpass=1234
bitcoind.zmqpubrawblock=tcp://127.0.0.1:18502
bitcoind.zmqpubrawtx=tcp://127.0.0.1:18503

lncli --network=testnet walletbalance
lncli --network=testnet connect 038863cf8ab91046230f561cd5b386cbff8309fa02e3f0c3ed161a3aeb64a643b9@203.132.94.196:9735
lncli --network=testnet openchannel --node_key 038863cf8ab91046230f561cd5b386cbff8309fa02e3f0c3ed161a3aeb64a643b9 --connect 203.132.94.196:9735 --local_amt 50000
lncli --network=testnet payinvoice lntb500u1p3fejx8pp5xf93gqluwul7rj3272qs6jqvpcuvgsa2hg0vlrx49dn0npc5x86sdqqcqzpgxqy9gcqqzwpmwcyrc0ysmap6ezwnm4jphjy4zfxd25ryumje9af3pgvxmwz7n4jxjplnkz96aqkqx7v0zgwvfcw90zncamq8zmqvxq0sar6qdsp8ku76e



litd --httpslisten=0.0.0.0:8443 --uipassword=Genhi2002!@# --network=testnet --lnd-mode=integrated --lnd.lnddir=C:\Users\Ivan\AppData\Local\lnd --lnd.rpclisten=0.0.0.0:10009 --lnd.listen=0.0.0.0:9735 --lnd.bitcoin.node=bitcoind --lnd.bitcoind.rpcuser=1234 --lnd.bitcoind.rpcpass=1234 --lnd.bitcoind.zmqpubrawblock=tcp://127.0.0.1:18502 --lnd.bitcoind.zmqpubrawtx=tcp://127.0.0.1:18503 --rpcserver=localhost:10009 --macaroonpath=C:\Users\Ivan\AppData\Local\lnd\data\chain\bitcoin\testnet\admin.macaroon


litd --uipassword=Genhi2002!@# --network=testnet --lnd-mode=integrated --lnd.bitcoin.node=bitcoind --lnd.bitcoind.dir=C:\Users\Ivan\Bitcoin
