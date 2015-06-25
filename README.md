Rust Radix Trie
====

[![Build Status](https://travis-ci.org/michaelsproul/rust_radix_trie.svg)](https://travis-ci.org/michaelsproul/rust_radix_trie)

This is a [Radix Trie][radix-wiki] implementation in Rust, building on the lessons learnt from
`TrieMap` and [Sequence Trie][seq-trie].

You can read about my experience implementing this data structure [here][radix-paper].

# Features

* Compressed nodes. Common key prefixes are stored only once.
* Trie-specific methods to look-up predecessors (closest ancestors).
* Key Generic. Any type that can be serialised as a vector of bytes can be used as a key.
* Safe - no unsafe code.

# Usage

Available on Crates.io as `radix_trie`.

```toml
[dependencies]
radix_trie = "*"
```

# Documentation

https://michaelsproul.github.io/rust_radix_trie/

# To Do

* Optimise (make a `NibbleSlice`, see [paper][radix-paper]).
* QuickCheck tests.
* Successor methods?
* Implement the Entry API?

# License

MIT License. Copyright (c) Michael Sproul 2015.

[radix-wiki]: http://en.wikipedia.org/wiki/Radix_tree
[seq-trie]: https://github.com/michaelsproul/rust-sequence-trie
[radix-paper]: https://michaelsproul.github.io/rust_radix_paper/
