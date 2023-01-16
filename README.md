## etherspot-popular-tokens-tokenlist
Etherspot SDK PopularTokens token list

Web: [https://etherspot.io](https://etherspot.io)

Docs: [https://docs.etherspot.dev/](https://docs.etherspot.dev/)

Use Etherspot SDK to fetch stable coins: 

```
import { Sdk, NetworkNames, randomPrivateKey } from 'etherspot';
const privateKey = randomPrivateKey();
let sdk: Sdk
sdk = new Sdk({
  privateKey,
  }, {
    networkName: 'mainnet' as NetworkNames, 
    });
async function main() {
  const output = await sdk.getTokenListTokens({
    name: 'EtherspotPopularTokens',
  });

  console.log('token list tokens', output);
}

main().catch(console.error);
