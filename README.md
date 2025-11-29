# hashtriemap

Go's [`sync.Map`](https://pkg.go.dev/sync#Map) is not generic (and thus exposes `any` API all over), but is implemented in terms of a
a generic type that _is_ generic.
Unforuntately, that type is internal and thus not usable:
[`internal/sync.HashTrieMap`](https://pkg.go.dev/internal/sync#HashTrieMap).

This repo pulls that code out type out of its `internal` directory and
removes its dependencies on other `internal` packages so you can use
it in your own code, instead of `sync.Map`.


