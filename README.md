# Sui dApp starter

The mono repository is managed via pnpm, including contracts, backend and frontend.


## Project structure
```sh
├── project_root/
    ├── docs            # design documents
    ├── packages
    │   ├── move
	│	│   ├── pkg1    # standard move package
	│   │   ├── pkg2    # standard move package
    │   │   ├── scripts # move package operation scripts
    │   │   ├── package.json 
    │   ├── frondend
    │	│   ├── ...
    │   └── backend
    │	│   ├── ...
    ├── ...
	└── package.json
```

## Common Commands

0. Install prerequisite and dependencies

* Install `suibase` by following [suibase instruction](https://suibase.io/how-to/install.html).
* Install dependencies `pnpm install`

1. Create move package
```sh
> cd packages/move
> lsui move new <my_first_package>
```

2. Build and test move package
```sh
> cd package/move/greeting
> lsui move build
> lsui move test
```

3. Start localnet for development and tests

* Start suibase localnet: `localnet start`
* Start local sui explorer: `pnpm localnet:start`

4. Deploy package on localnet|devnet|testnet|mainnet
```sh
> pnpm --filter move localnet:deploy:greeting
```