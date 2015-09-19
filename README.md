# difference.rs [![](https://travis-ci.org/johannhof/difference.rs.svg?branch=master)](https://travis-ci.org/johannhof/difference.rs)[![](https://img.shields.io/crates/v/difference.svg)](https://crates.io/crates/difference)
A Rust text diffing library with built-in diffing assertion.

__[Documentation](https://johannhof.github.io/difference.rs)__

__[Examples](/Examples.md)__

```rust
let (dist, changeset) = diff("test", "tent", "");

assert_eq!(changeset, vec![
    Difference::Same("te".to_string()),
    Difference::Rem("s".to_string()),
    Difference::Add("n".to_string()),
    Difference::Same("t".to_string())
]);
```

![](https://raw.githubusercontent.com/johannhof/difference.rs/master/assets/fox.png)
![](https://raw.githubusercontent.com/johannhof/difference.rs/master/assets/github-style.png)

Usage
----------

Add the following to your Cargo.toml:

```toml
[dependencies]
difference = "0.4"
```

Now you can use the crate in your code
```rust
extern crate difference;
```

Using the binary
-----------------

difference can also be used as a command-line application. The best way to install it is using rustle:

```
curl -sf https://raw.githubusercontent.com/brson/rustle/master/rustle.sh | sh -s -- https://github.com/johannhof/difference.rs
```
