# Data Protocol
Future-oriented infrastructure - Data Protocol.

## What is data
There are two types of data, one is normalized data and the other is structured data.

**Normalized data** is scattered, disorderly, and without a fixed format. This data cannot be directly used for external interactions and transactions. This data has only two attributes, one is the content and the other is the generation time. Our daily chat records, visit history, shopping lists, article blogs and others belong to this kind of data. The data has the characteristics of intuitive visibility, free reproducibility, forgeability, and non-traceability.

**Structured data** has a strict representation. Can be used for external interaction and transactions. This data type has the five attributes. The rest of this article discusses structured data.

## Attribute
- **Owner**: Indicates the producer of the data, and the producer is the owner. Structured data has strict data validation rights.
- **DID**: Represents the unique identity of the data.
- **Parent-DID**: The data is marked as a modified copy of the original data. This is an optional attribute, and the data generated for the first time does not have this attribute by default.
- **Value**: Indicates the specific content and form of the data.
- **Lifetime**: Represents the generation time and expiration time of the data, and is also the entire life cycle of the data.

For example:
```json
{
  "owner": "000000000000000000",    // owner
  "did": "base58000000000000",      // DID
  "pid": "base58000000000000",      // Parent-DID
  "value": "type:xxxxx:0101010101", // Value
  "time": "00120112:00123423",      // Lifetime
}
```

## Features
### Visibility
- **Unencrypted and permissionless**: anyone and organization can access data, and can read the attributes of the data (public, public network).
- **Unencrypted and permissioned**: data can be obtained only with permission, and data attributes can be read (private, local sharing).
- **Encrypted and permissionless**: anyone and organization can access data, but cannot read the attributes of the data (private, decentralized storage).
- **Encrypted and permissioned**: data can be obtained only with permission, and the attributes of the data can be read (private, distributed storage).

### Verifiability
- Can verify the ownership of the data.
- Can verify the uniqueness, completeness and timeliness of data.
- Can verify the access and operational rights to the data.

### Processability
- Data can be read.
- Data can be modified.
- Data can be processed.
- Data can be deleted.

### Reproducibility
- Data can be copied, copying all attributes of the data.
- Data can be propagated, propagating all the attributes of the data.
- Modify the attributes of the data, the data will no longer be the same.

## Core protocol
### [Data Identity Protocol](./identity)
- Data unique identification and attributes. [detail](./identity)
- Verifiable protocol of data. [detail](./identity)


### [Data Process Protocol](./process)
- Data generate. [detail](./process)
- Data read. [detail](./process)
- Data computer. [detail](./process)
- Data modify. [detail](./process)
- Data delete. [detail](./process)


### [Data Storage Protocol](./storage)
- Storage value
  - Unencrypted storage. [detail](./storage)
  - Encrypted storage. [detail](./storage)
- Storage location
  - Local storage. [detail](./storage)
  - cloud storage. [detail](./storage)
  - Distributed storage. [detail](./storage)
  - Decentralized storage. [detail](./storage)


### [Data Exchange Protocol](./exchange)
- Data summary and proof. [detail](./exchange)
- Data copy and proof. [detail](./exchange)
- Third party guarantee transaction. [detail](./exchange)
- No third party guarantee transaction. [detail](./exchange)

# Contributing

Your contributions are always welcome! Please take a look at the [contribution guidelines](https://github.com/cympletech/data-protocol/blob/master/CONTRIBUTING.md) first.

- - -

If you have any question about this opinionated list, do not hesitate to contact us [@CympleTech](https://twitter.com/CympleTech) on Twitter or open an issue on GitHub.

Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a
[Creative Commons Attribution 4.0 International License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
