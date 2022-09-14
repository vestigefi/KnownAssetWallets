## Vestige - Known ASA wallets repository
A list of known wallets related to Algorand Standard Assets used for either team allocation or burns.

### How to add a wallet:

###### CREATOR and RESERVE wallets attached to asset on chain are automatically included in circulating supply calculation and  need not be added

#### 

##### 1. Fork this repository

##### 2. If not existent add a JSON file for your asset 

**Filename:** _ASSET_ID_.json _(example: *700965019.json*)_

**Structure:**

```json
[
  {
    "address": YOUR_WALLET_ALGORAND_ADDRESS,
    "type": "TEAM" or "BURN",
    "txid": CONFIRMATION_TRANSACTION_ID,
    "description": "A short explanation of what the wallet is used for." 
  }
]
```

In case of burn wallets, a burn security mechanism explanation is **required** in the description field.

**CONFIRMATION_TRANSACTION_ID** is a transaction id of a transaction coming out of your already known wallet (creator or reserve address) to the wallet that is requested to be added.

The transaction is **required** to contain a note with text:\
`Vestige ASA wallets repository confirmation`

If your project does not have access to creator and reserve wallets, send a detailed explanation to *team@vestige.fi* in order to have your wallet added

##### 3. For additional wallets, simply expand your JSON file

```json
[
  {
    "address": "VEST2A43254FW6XZYIRUL2RZPCR4M3BH35UPMRSMFS3YCBX5SYPQDIBSIU",
    "type": "TEAM",
    "txid": "AUJIVOA2XV4QXIO3K5UIJD7SOXPOTUF4MUMR63FBAGVVSUXCNU7Q",
    "description": "Wallet used for TINY -> VEST swap SC creation." 
  },
  {
    "address": "VESTAGG6ZLWOESZQJWUWWBOCZSBVEDDT5AHHYZWBH4P2HLMNESGCLFSNVY",
    "type": "TEAM",
    "txid": "6ZIQOFXQHIIWWTZGDZGJLOJ5KOJX24QB33DTJXUYPUZAJKCYWUUA",
    "description": "Wallet used for DEX aggregator fee allocation." 
  }
]
```

##### 4. Propose a Pull Request (PR) to merge your changes into this repository

Updated wallets will be included into our circulating supply calculation within 7 days after verification
