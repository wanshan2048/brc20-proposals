
## Background

Currently, 5-byte tickers issuance are restricted to self-minting, and [Proposal for Issuance and Burn Enhancements](https://l1f.discourse.group/t/brc-20-proposal-for-issuance-and-burn-enhancements-brc20-ip-1/621) said the option for public mint issuance will be introduced at a later stage.


## Changes to Deploy Inscription

This proposal only changes the tick description of the original BRC-20 protocol. 

* BRC-20 deploy inscription content:
```
{
  "p": "brc-20",
  "op": "deploy",
  "tick": "12345",
  "max": "21000000",
  "lim": "1000"
}
```

| Key       | Required? |Description|
|-----------|-----------|-----------|
| p         | Yes       | Protocol: Helps other systems identify and process brc-20 events |
| op        | Yes       | Operation: Type of event (Deploy, Mint, Transfer)  |
| tick      | Yes       | Ticker: 4 or 5 letter identifier of the brc-20  |
| max       | Yes       | Max supply: set max supply of the brc-20  |
| lim       | No        | Mint limit: If letting users mint to themsleves, limit per ordinal  |
| dec       | No        | Decimals: set decimal precision, default to 18  |


##  Block Activation Height: TBD
