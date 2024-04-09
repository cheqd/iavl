# Changelog

## 0.19.5 (February 2, 2023)

### Breaking Changes

- [#622](https://github.com/cosmos/iavl/pull/622) `export/newExporter()` and `ImmutableTree.Export()` returns error for nil arguements

## Improvements

- [#640](https://github.com/cosmos/iavl/pull/640) commit `NodeDB` batch in `LoadVersionForOverwriting`.
- [#636](https://github.com/cosmos/iavl/pull/636) Speed up rollback method: `LoadVersionForOverwriting`.
- [#654](https://github.com/cosmos/iavl/pull/654) Add API `TraverseStateChanges` to extract state changes from iavl versions.
- [#638](https://github.com/cosmos/iavl/pull/638) Make LazyLoadVersion check the opts.InitialVersion, add API `LazyLoadVersionForOverwriting`.

## 0.19.4 (October 28, 2022)

- [#599](https://github.com/cosmos/iavl/pull/599) Populate ImmutableTree creation in copy function with missing field
- [#589](https://github.com/cosmos/iavl/pull/589) Wrap `tree.addUnsavedRemoval()` with missing `if !tree.skipFastStorageUpgrade` statement

## 0.19.3 (October 8, 2022)

- `ProofInner.Hash()` prevents both right and left from both being set. Only one is allowed to be set. 

> Note: It is recommended to not use the native proof structure of IAVL in its current form. Please refer to [ics23](https://github.com/confio/ics23/tree/master/go) for IAVL proofs

## 0.19.2 (October 6, 2022)

 - [#547](https://github.com/cosmos/iavl/pull/547) Implement `skipFastStorageUpgrade` in order to skip fast storage upgrade and usage. 
 - [#531](https://github.com/cosmos/iavl/pull/531) Upgrade to fast storage in batches. 

## 0.20.1 (September 5, 2023)

### Improvements

- [#654](https://github.com/cosmos/iavl/pull/654) Add API `TraverseStateChanges` to extract state changes from iavl versions.
- [#726](https://github.com/cosmos/iavl/pull/726) Make `KVPair` and `ChangeSet` serializable with protobuf.
- [#795](https://github.com/cosmos/iavl/pull/795) Use gogofaster buf plugin.

### Bug Fixes

- [#801](https://github.com/cosmos/iavl/pull/801) Fix rootKey empty check by len equals 0.
- [#829](https://github.com/cosmos/iavl/pull/829) Fix fastnode concurrency panic.

## 0.20.0 (March 14, 2023)

- [#622](https://github.com/cosmos/iavl/pull/622) `export/newExporter()` and `ImmutableTree.Export()` returns error for nil arguements
- [#586](https://github.com/cosmos/iavl/pull/586) Remove the `RangeProof` and refactor the ics23_proof to use the internal methods.
- [#640](https://github.com/cosmos/iavl/pull/640) commit `NodeDB` batch in `LoadVersionForOverwriting`.
- [#636](https://github.com/cosmos/iavl/pull/636) Speed up rollback method: `LoadVersionForOverwriting`.
- [#638](https://github.com/cosmos/iavl/pull/638) Make LazyLoadVersion check the opts.InitialVersion, add API `LazyLoadVersionForOverwriting`.
