# Stride-About
today i will show you how to install stride validator
### System requirements
```
4 CPU
8 RAM
200 GB SSD
```
# setup:
```
wget -q -O stride.sh https://api.rues.info/stride.sh && chmod +x stride.sh && sudo /bin/bash stride.sh
```
# Creating a wallet:
```
strided keys add <walletName>
```
# Creating a validator:
```
strided tx staking create-validator \
--amount=9900000ustrd \
--pubkey=$(strided tendermint show-validator) \
--moniker=RuesValidator \
--chain-id=STRIDE-1 \
--commission-rate="0.10" \
--commission-max-rate="0.20" \
--commission-max-change-rate="0.1" \
--min-self-delegation="1" \
--fees=250ustrd \
--gas=200000 \
--from=rues \
--website="http://forum.rues.info/" \
--details="https://linktr.ee/ruesandora0" \
-y
```
# Explorer Control:https://stride.explorers.guru/validator/stridevaloper1vm6wnmvxugqj8k6s6d2cktgctc550qaq53jyus
