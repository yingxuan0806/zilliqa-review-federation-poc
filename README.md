# Review Federation POC

## Set-up
```
git clone git@github.com:iangohy/zilliqa-review-federation-poc.git
cd zilliqa-review-federation-poc
yarn install
yarn run start
```

To listen on other ports
```
PORT=8888 yarn run start
```

## Usage
### Recommendations
Add `PRIVATE_KEY` and `CONTRACT_ADDRESS` to .env file at the root of the project folder. Additional required environmental variables can be prepended to the desired commands. Examples shown assume that `PRIVATE_KEY` and `CONTRACT_ADDRESS` have been added to .env file or already exists as an environment variable.
### Get Rating
```
/getRating/<smart_contract_address>/<ipfs_hash>
```
Example: http://localhost:3000/getRating/0x6e3d093864Ee51C691d68447Afe9fdC38c025866/Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u

### Deploy Smart Contract
```
PRIVATE_KEY=xxxx yarn run deploy
```
Example: 
```
yarn run deploy
```
### Add Rating
```
PRIVATE_KEY=xxxx CONTRACT_ADDRESS=xxxx IPFS_HASH=Qxxxx RATING=x yarn run addRating
```
Example: 
```
IPFS_HASH=Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u RATING=1 yarn run addRating
```

### Add to Federation
```
PRIVATE_KEY=xxxx CONTRACT_ADDRESS=xxxx ADD_CONTRACT_ADDRESS=xxxx yarn run addFed
```
Example:
```
ADD_CONTRACT_ADDRESS=0x5a53a64d5076b36845b7a97354e346051fc74d96 yarn run addFed
```

### Remove from Federation
```
PRIVATE_KEY=xxxx CONTRACT_ADDRESS=xxxx RM_CONTRACT_ADDRESS=xxxx yarn run rmFed
```
Example:
```
RM_CONTRACT_ADDRESS=0x5a53a64d5076b36845b7a97354e346051fc74d96 yarn run rmFed
```

## Testing Data
### IPFS
Cat Picture IPFS Hash
```
Qmd286K6pohQcTKYqnS1YhWrCiS4gz7Xi34sdwMe9USZ7u
```

### Contracts
Main Contract
```
0x6e3d093864Ee51C691d68447Afe9fdC38c025866
```

Secondary Contracts (federation)
```
0x5a53a64d5076b36845b7a97354e346051fc74d96
0xfb079782bf674fe8649348dbfd1db312097744c3
0x9a97d7412f30c194bd1ee2565953f558bb9adfda
```