# O1 Containers Collection

Containerized Web3 and Cloud-Native applications

**Overview**
  - [Containers](#containers)
  - [Options](#options)
  - [License](#license)
  - [Author Information](#author-information)

#### Containers

| name | description | link |
| :---: | :---: | :---: |
| [avalanchego](./avalanchego) | Go implementation of an Avalanche node | [![avalanchego](https://img.shields.io/docker/pulls/0labs/avalanchego?style=flat)](https://hub.docker.com/repository/docker/0labs/avalanchego) |
| [bitcoind](./bitcoind) | Client software for running a Bitcoin Core node | [![bitcoind](https://img.shields.io/docker/pulls/0labs/bitcoind?style=flat)](https://hub.docker.com/repository/docker/0labs/bitcoind) |
| [bitcoin-abcd](./bitcoin-abcd) | Node software and infrastructure for the Bitcoin Cash/eCash project | [![bitcoin-abcd](https://img.shields.io/docker/pulls/0labs/bitcoin-abcd?style=flat)](https://hub.docker.com/repository/docker/0labs/bitcoin-abcd) |

#### Options

##### run args

- `RUN_ARGS`: specify arbitrary application command-line arguments on container startup within the runtime environment.

```
docker run --env RUN_ARGS="--help" <image>
```

##### dynamic application configuration mounts

Mount customized application configuration files to locations of your choosing - can be used in tandem with `RUN_ARGS` to specify where configuration files are loaded from.

```
docker run --volume ./config/mainnet:/config <image>
```

##### custom entrypoints

Execute customized scripts and operations within each container on startup. All executables mounted to `/docker-entrypoint.d` will be ran in lexical  sort order according to the C/POSIX locale character collation rules. ([example](https://github.com/0x0I/container-file-lighthouse/tree/master/entrypoints))

```
docker run --volume ./custom-app-entrypoints:/docker-entrypoint.d <image>
```

License
-------

MIT

Author Information
------------------

Created in 2023 by O1.IO.

🏆 **always happy to help & donations are always welcome** 💸

* **ETH (Ethereum):** 0x652eD9d222eeA1Ad843efec01E60C29bF2CF6E4c

* **BTC (Bitcoin):** 3E8gMxwEnfAAWbvjoPVqSz6DvPfwQ1q8Jn

* **ATOM (Cosmos):** cosmos19vmcf5t68w6ug45mrwjyauh4ey99u9htrgqv09
