# Wormholes Testnet Installation Guide

## Hello, we are joining the Wormholes testnet. Only 578 people are participating, the number is low. There may be unexpected pleasant surprises in the possibility of a reward, so don't forget to star and fork from the top right. If you have any questions: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/193394860-8e7e2608-727c-44cd-8eb4-cd706c0a7a29.png)

## System requirements:
NODE TYPE | CPU | RAM | SSD |
| ------------- | ------------- | ------------- | -------- |
| Testnet | 4 | 8 | 500* |

`*`: Stated as 500GB in the official documentation.

![image](https://user-images.githubusercontent.com/101462877/193394913-27eeed39-6b28-465f-bdfa-b2980312afa2.png)

## Important links for Wormholes:
- [Website](https://www.wormholes.com/)
- [Explorer](https://www.wormholesscan.com/)
- [Twitter](https://twitter.com/WormholesChain)
- [Discord](https://discord.gg/rDHc4XHrjQ)

# 0) For update.


## If you have previously installed and want to update, press `enter` in this section.
![image](https://user-images.githubusercontent.com/101462877/193442332-35663e38-b861-4a70-b605-9421dbe4a95f.png)

## DO NOT CONTINUE BELOW AFTER THE UPDATE.

# 1a) Installation with the script.

wget -O wormholes.sh https://raw.githubusercontent.com/thisislexar/Wormholes-Testnet/main/wormholes.sh && chmod +x wormholes.sh && ./wormholes.sh


![image](https://user-images.githubusercontent.com/101462877/193395770-401fa358-a549-4198-b902-f0635a71fd21.png)

## At this point, it will ask for our private key. I explain how to find it in the images below.

## Go to [Limino](https://www.limino.com/), where we opened the wallet when applying for the testnet. Click on the clover in the upper left.

![image](https://user-images.githubusercontent.com/101462877/193395813-1cfd2679-d221-46db-8673-7aa065e916b0.png)

## Click on Settings.

![image](https://user-images.githubusercontent.com/101462877/193395849-85a3aedc-c6ea-4186-b6b9-a18063911847.png)

## Click on Security & Privacy.

![image](https://user-images.githubusercontent.com/101462877/193395869-2e61e15a-cea7-49cf-9bbe-9e492a528bb5.png)

## Enter the wallet password you created earlier.

![image](https://user-images.githubusercontent.com/101462877/193395899-9500ebef-470b-4e25-9e99-6f8f447a3275.png)

## Copy our private key.
![image](https://user-images.githubusercontent.com/101462877/193395922-45ec2958-b1bc-40b2-be4b-a800c9e8a7f2.png)



# Paste the private key into the terminal.
![image](https://user-images.githubusercontent.com/101462877/193396169-2498e943-bc68-419e-8995-8af7ab48e8d6.png)


# 1b) Manual installation.

If you want to improve your node knowledge, you can also do the [Manual Installation](https://www.wormholes.com/docs/Install/run/index.html#spin-up-your-own-wormholes-node) from the original documentation. It's not too difficult; they have provided the script themselves.

# 2) After installing the node, we continue with staking.

## Go to [Limino](https://www.limino.com/) wallet. Click on the clover in the upper left.

![image](https://user-images.githubusercontent.com/101462877/193396221-3310f74b-5894-4f42-9bdd-4a095587495c.png)

## Click on `Become a validator`.
![image](https://user-images.githubusercontent.com/101462877/193396254-df8fe754-9ab9-45b9-9284-8228e7f3614e.png)

## Confirm.

![image](https://user-images.githubusercontent.com/101462877/193396347-18c58217-191a-4aba-b627-a0e9aac3c11d.png)

## Wait for approval.

![image](https://user-images.githubusercontent.com/101462877/193396399-364caed2-bb19-493b-b58d-21fd9915de27.png)

## After approval, you can check it on [Explorer](https://www.wormholesscan.com/).
![image](https://user-images.githubusercontent.com/101462877/193396498-4fe8a902-15a2-426d-9c99-d5308c3295a0.png)

![image](https://user-images.githubusercontent.com/101462877/193396623-6e8753f8-7b34-487b-a597-b0b505d88120.png)

# Node control commands

## Node connection

curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"net_peerCount","id":1}' http://127.0.0.1:8545/


## Block check

curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}' http://127.0.0.1:8545/

  
## Node version check

curl -X POST -H "Content-Type:application/json" --data '{"jsonrpc":"2.0","method":"eth_version","id":64}' http://127.0.0.1:8545/


## Wallet balance

curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_getBalance","params":["<WALLETADDRESS>","pending"],"id":1}' http://127.0.0.1:8545

## Node viewing

wget -O nodemonitoring.sh https://raw.githubusercontent.com/thisislexar/Wormholes-Testnet/main/nodemon


![image](https://user-images.githubusercontent.com/101462877/193398815-6cc3f19e-2d24-4bd0-b5e8-2de93a20e83a.png)


# If you have any questions: [LossNode Chat](@cossy125)

