# TON-EVM Toncoin Bridge

TON-Ethereum Bridge in `master` branch.

TON-BSC (Binance Smart Chain) Bridge in `bsc` branch.

TON-Ethereum and TON-BSC bridges differs only in the config parameter number 71/72.

## Prepare

```
PATH="/Users/tolyayanot/dev/newton/liteclient-build/crypto:$PATH"
export FIFTPATH=/Users/tolyayanot/dev/newton/ton/crypto/fift/lib:/Users/tolyayanot/dev/newton/ton/crypto/
```

## Run tests

```
node test/index.js
```

## Compile Func

```
func -o bridge_code2.fif -SPA stdlib.fc text_utils.fc message_utils.fc bridge-config.fc bridge_code.fc
func -o votes-collector.fif -SPA stdlib.fc message_utils.fc bridge-config.fc votes-collector.fc 
func -o multisig-code.fif -SPA stdlib.fc multisig-code.fc 
```

## Dev History

* Jun 29, 2021 - Update TON nodes to support Config71 (TON-ETH bridge config) - [Announcement](https://t.me/tonblockchain/26), [Description](https://github.com/ton-blockchain/TIPs/issues/34).

* Aug 16, 2021 - Deploy ETH Bridge to TON Mainnet - master branch, tag `eth_mainnet`.

    Network voting for Config -71
  
    ETH Governance 1.0 - kf8rV4RD7BD-j_C-Xsu8FBO9BOOOwISjNPbBC8tcq688Gcmk
  
    ETH Collector - EQCuzvIOXLjH2tv35gY4tzhIvXCqZWDuK9kUhFGXKLImgxT5
  
    ETH Bridge - Ef_dJMSh8riPi3BTUTtcxsWjG8RLKnLctNjAM4rw8NN-xWdr
  
    [Announcement](https://t.me/tonblockchain/35), [Description](https://github.com/ton-blockchain/TIPs/issues/35)

* Aug 20, 2021 - ETH-TON Bridge public launch - https://t.me/tonblockchain/36

* Sep 09, 2021 - Update TON nodes to support Config72 (TON-BSC bridge config) - [Announcement](https://t.me/tonblockchain/40).

* Sep 27, 2021 - Network voting for Config 71 - https://t.me/tonblockchain/43

* Oct 01, 2021 - Deploy BSC Bridge to TON Mainnet - `bsc` branch, tag `bsc_mainnet`.
   
    Network voting for Config 72
   
    BSC Governance 1.0 - kf8_gV8rpqtPl1vmYDrMzwxlGQDJ63SIKO8vDhNZHT5wwVhd
   
    BSC Collector - EQAHI1vGuw7d4WG-CtfDrWqEPNtmUuKjKFEFeJmZaqqfWTvW
   
    BSC Bridge - Ef9NXAIQs12t2qIZ-sRZ26D977H65Ol6DQeXc5_gUNaUys5r
   
    https://t.me/tonblockchain/44, https://github.com/ton-blockchain/TIPs/issues/37.

* Oct 04, 2021 - BSC-TON Bridge public launch - https://t.me/tonblockchain/45

* Nov 22, 2021-Nov 26, 2021 - To prevent overflow, external messages have been replaced with internal messages in multisig (governance).
    
* Nov 26, 2021 - Deploy and voting for new BSC Governance 2.0 to TON Mainnet - `bsc` branch, tag `bsc_mainnet2` - https://t.me/tonblockchain/71.
   
    BSC Governance 2.0 - kf8OvX_5ynDgbp4iqJIvWudSEanWo0qAlOjhWHtga9u2Yo7j

* Dec 02, 2021 - Deploy and voting for new ETH Governance 2.0 to TON Mainnet - master bracnh, tag `eth_mainnet2` - https://t.me/tonstatus/3.
   
    ETH Governance 2.0 - kf87m7_QrVM4uXAPCDM4DuF9Rj5Rwa5nHubwiQG96JmyAo-S
