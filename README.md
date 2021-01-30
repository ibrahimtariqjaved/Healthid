# Healthid
A Healthcare Identity Management System 
To setup a private etherum POA network 

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
