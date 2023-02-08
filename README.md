## etherspot-popular-tokens-tokenlist
*Disclaimer: 
The list is from the Popular tokenlist filtered by Volume (24H) on explorers listed below:*
https://polygonscan.com/tokens

https://gnosisscan.io/tokens

https://etherscan.io/tokens

https://bscsscan.com/tokens

**Date of snapshot: Jan 16, 2023**

Etherspot SDK PopularTokens token list

Web: [https://etherspot.io](https://etherspot.io)

Docs: [https://docs.etherspot.dev/](https://docs.etherspot.dev/)

Use Etherspot SDK to fetch popular token list

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
