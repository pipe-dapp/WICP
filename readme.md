
# What is WICP(Wrapped-ICP)
WICP is an alt token based on the ICP-20 standard, and it's value is 1:1 with ICP

# Why you need WICP
* Support atomic and batch transfer to implementation complex transactions
* Zero transaction fee
* WICP brings more liquidity to the internet computer, decentralized exchange(DEX) and DeFi applications
* Query transaction records directly though the canister

# Canister ID
* Production: o5d6i-5aaaa-aaaah-qbz2q-cai
* Test: sgymv-uiaaa-aaaaa-aaaia-cai

# Deploy
```
npm install
dfx canister --netwotk ic create --all
dfx build --network ic
dfx deploy --network ic WICP --argument '(principal "<owner principal>", principal "<fee to principal>")'
dfx canister --network ic call WICP newStorageCanister '(principal "owner principal")'
```

# Commonly used commands
transfer
```
dfx canister --network ic call <canister id> transfer '(principal "<to principal>", <amount> : nat)'
```

transferFrom
```
dfx canister --network ic call <canister id> transferFrom '(principal "<from principal>", principal "<to principal>", <amount> : nat)'
```

approve
```
dfx canister --network ic call <canister id> approve '(sendper "<to principal>", <amount> : nat)'
```

mint
```
dfx canister --network ic call <canister id> mint '(record {blockHeight = <block height>:nat64})'
```

burn
```
dfx canister --network ic call <canister id> burn '(<amount>:nat)'
```


