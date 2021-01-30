# Healthid
A Healthcare Identity Management System 
To setup a private etherum POA network 

1. Initiate geth using genesis \\

# geth --datadir "./data" account new
# geth --datadir ./data init ./genesis.json

2. Initialize blockchain on node
# geth --networkid 786 --datadir ./data --port 30303 --ipcdisable --syncmode full --rpc --allow-insecure-unlock --rpccorsdomain "*" --rpcport 8545 --rpcaddr "172.31.47.35" --unlock 0x8A6E712B4fa7c3A5B3CED67d9C2137A9b1988Ce0 --mine --rpcapi personal\,admin,db,eth,net,web3,miner,shh,txpool,debug,clique --ws --wsaddr 0.0.0.0 --wsport 8546 --wsorigins '*' --wsapi personal,admin,db,eth,net,web3,miner,shh,txpool,debug,clique --maxpeers 25 --etherbase 0 --gasprice 0 --targetgaslimit 9999999 console

3. Adding peers to the network 
# admin.addPeer("enode://203707e965cee114efbd51e9d6f138a7bd7c5144000d3de0f65ae165022166cf979ce6fa441266424423eb019aa3a5030c85a6ca6418abdc039870a66f35349a}@54.216.90.147:30303")}


The healthID consists of three types of smartcontract 
1. Patient SC
2. Provider SC
3. Registry SC

The Patient SC and Provider SC consist of the following five functions:

1. set_public_key: Allowsa the owner of the smartcontract to upload and store its public key.
2. get_public_key: Allows anyone to retrieve the public key of the owner by using their healthID. 
3. set_hash: Allows the owner to store the hash and hashID of their identity attribute. 
4. get_hash: Allow to retrive hash by using hashID of the identity attribute. 
5. pause_SC: Allow the owner of the smart contract to pause and unpause the contract.

The registry SC consists of the following functions:

1. register_regulator: Allows regulators to register themselves and upload their public key. 
2. verify_regulator: Allows anyone to retrieve the public key of regulators using their Ethereum address.   
3. register_attestation: Allows regulators to register the healthID and public key. 
4. verify_attestation: Allows to retreive the public key of registered healthID.  
5. revoke_attestation: Allows the regulator to revoke the attestation. 
