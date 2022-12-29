<h1 align="center">Wormholes Testneti Kurulum Rehberi

## Merhabalar, Wormholes testnetine katılıyor olacağız. Sadece 578 kişi katılıyor, sayı düşük. Ödül ihtimalinde beklenmedik güzel sürprizler olabilir bu yüzden. Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/193394860-8e7e2608-727c-44cd-8eb4-cd706c0a7a29.png)

## Sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Testnet | 4          | 8         | 500*  |

`*`: Resmi dokümanda 500GB olarak belirtlmiş.

![image](https://user-images.githubusercontent.com/101462877/193394913-27eeed39-6b28-465f-bdfa-b2980312afa2.png)


## Wormholes için önemli linkler:
- [Website](https://www.wormholes.com/)
- [Explorer](https://www.wormholesscan.com/)
- [Twitter](https://twitter.com/WormholesChain)
- [Discord](https://discord.gg/rDHc4XHrjQ)

# 0) Güncelleme için.
```
wget -O wormholes.sh https://raw.githubusercontent.com/thisislexar/Wormholes-Testnet/main/wormholes.sh && chmod +x wormholes.sh && ./wormholes.sh
```

## Daha öncesinde kurduysanız ve güncelleme yapacaksanız bu kısımda `y`'ye basın.
![image](https://user-images.githubusercontent.com/101462877/193442332-35663e38-b861-4a70-b605-9421dbe4a95f.png)

## Ardından [1a](https://github.com/thisislexar/Wormholes-Testnet/blob/main/README.md#1a-script-ile-kurulum) kısmında gösterdiğim gibi `private key`'inizi bularak terminale yapıştırın.

![image](https://user-images.githubusercontent.com/101462877/193442410-34ae281a-0c7f-40da-892c-d6b16c2e125c.png)
  
## GÜNCELLEME BİTTİ AŞAĞIYA DEVAM ETMEYİN.

# 1a) Script ile kurulum.

```
wget -O wormholes.sh https://raw.githubusercontent.com/thisislexar/Wormholes-Testnet/main/wormholes.sh && chmod +x wormholes.sh && ./wormholes.sh
```

![image](https://user-images.githubusercontent.com/101462877/193395770-401fa358-a549-4198-b902-f0635a71fd21.png)

## Bu kısımda bizden private key isteyecek, aşağıdaki görsellerde nasıl bulacağınızı anlatıyorum.

## Daha öncesinde testnete başvururken cüzdan açtığımız [Limino](https://www.limino.com/)'ya gidiyoruz. Sol üstteki yoncaya tıklıyoruz.

![image](https://user-images.githubusercontent.com/101462877/193395813-1cfd2679-d221-46db-8673-7aa065e916b0.png)

## Settings'e tıklıyoruz.

![image](https://user-images.githubusercontent.com/101462877/193395849-85a3aedc-c6ea-4186-b6b9-a18063911847.png)

## Security & Privacy'ye tıklıyoruz.


![image](https://user-images.githubusercontent.com/101462877/193395869-2e61e15a-cea7-49cf-9bbe-9e492a528bb5.png)


## Daha öncesinde oluşturduğumuz cüzdan şifresini giriyoruz.

![image](https://user-images.githubusercontent.com/101462877/193395899-9500ebef-470b-4e25-9e99-6f8f447a3275.png)

## Private key'imizi kopyalıyoruz.
![image](https://user-images.githubusercontent.com/101462877/193395922-45ec2958-b1bc-40b2-be4b-a800c9e8a7f2.png)



# Private key'i terminale yapıştırıyoruz.
![image](https://user-images.githubusercontent.com/101462877/193396169-2498e943-bc68-419e-8995-8af7ab48e8d6.png)


# 1b) Manuel kurulum.

Node bilginizi geliştirmek adına dilerseniz orijinal doküman üzerinden [Manuel Kurulum](https://www.wormholes.com/docs/Install/run/index.html#spin-up-your-own-wormholes-node) da yapabilirsiniz. Çok da zor değil, script'i kendileri vermişler.

# 2) Node'u kurduktan sonra staking ile devam ediyoruz.

## [Limino](https://www.limino.com/) cüzdana gidiyoruz. Sol üstte yoncaya tıklıyoruz.

![image](https://user-images.githubusercontent.com/101462877/193396221-3310f74b-5894-4f42-9bdd-4a095587495c.png)

## `Become a validator`'e tıklıyoruz.
![image](https://user-images.githubusercontent.com/101462877/193396254-df8fe754-9ab9-45b9-9284-8228e7f3614e.png)

## Confirm diyoruz.
![image](https://user-images.githubusercontent.com/101462877/193396347-18c58217-191a-4aba-b627-a0e9aac3c11d.png)

## Onaylanmasını bekliyoruz.
![image](https://user-images.githubusercontent.com/101462877/193396399-364caed2-bb19-493b-b58d-21fd9915de27.png)

## Onaylandıktan sonra [Explorer](https://www.wormholesscan.com/)'a giderek kontrol edebiliriz.
![image](https://user-images.githubusercontent.com/101462877/193396498-4fe8a902-15a2-426d-9c99-d5308c3295a0.png)

![image](https://user-images.githubusercontent.com/101462877/193396623-6e8753f8-7b34-487b-a597-b0b505d88120.png)



# Node kontrol komutları

## Node bağlantısı

```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"net_peerCount","id":1}' http://127.0.0.1:8545/
```


## Blok kontrolü

```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}' http://127.0.0.1:8545/
```
  
## Node versiyon kontrolü

```
curl -X POST -H "Content-Type:application/json" --data '{"jsonrpc":"2.0","method":"eth_version","id":64}' http://127.0.0.1:8545/
```

## Cüzdan bakiyesi

```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_getBalance","params":["<CÜZDANADRESİ>","pending"],"id":1}' http://127.0.0.1:8545
```
## Node görüntüleme

```
wget -O nodemonitoring.sh https://raw.githubusercontent.com/thisislexar/Wormholes-Testnet/main/nodemonitoring.sh && chmod +x nodemonitoring.sh && ./nodemonitoring.sh
```

![image](https://user-images.githubusercontent.com/101462877/193398815-6cc3f19e-2d24-4bd0-b5e8-2de93a20e83a.png)


# Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)



