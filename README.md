# Stride Hakkında
Bugün sizlere validator nasıl oluşturulur onu göstericem ondan önce biraz strike projesini tanıyalım.
Stride ,stake edilen varlıklar için likidite sağlayan bir blokzincirdir.Stride'ı kullanarak Cosmos IBC ekosisteminde hem stake hem de DeFi getirileri kazanabilirsiniz .Stake ettiğiniz token karşılığında stTokens kazanırsınız.Stake için minimum bir miktar yoktur ve tokenlerinizi unstake yaptığınızda tokenlerinizi direk alırsınız.Cosmos ekosistemininde normalde bu 21 gündür.Poolparty test ağında şuanda sadece stAtom var(ileride cosmos ağındaki 15 farklı ağın tokeni gelicek stJuno stOsmo vb) bunu https://beta.stride.zone/ linkten test edebilirsiniz.Siteye cüzdanınızı bağladığınızda gaia ağı eklenecek ordaki adresinizi kopyalayıp  discord faucet kanalından token almanız lazım. https://discord.gg/Q6RUuX9x bu linkten discord kanalında katılabilirsiniz.Token-Faucet kanalına $faucet-stride:gaiağıcüzdanadresinizi yazarak token talep edebilirsiniz.Daha sonra sitede stake ve unstake ederek test edebilirsiniz.



### Sistem Gereksiinmleri
```
4 CPU
8 RAM
200 GB SSD
```
# setup:
```
wget -q -O stride.sh https://api.rues.info/stride.sh && chmod +x stride.sh && sudo /bin/bash stride.sh
```
# Wallet Oluşturma:
```
strided keys add <walletName>
```
# Validator Oluşturma:
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
