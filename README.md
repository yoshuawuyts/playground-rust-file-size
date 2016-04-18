# playground-rust-file-size
Messing around with Rust binary file size.

## The code
```rust
fn main() {
  println!("Hello, world!");
}
```

## Benchmarks
```txt
01  292kB  # No optimizations whatsoever
02  292kB  # Build with --release flag
03  228kB  # Build with --release and strip(1)
04   88kB  # --release, strip(1) and upx(1)
05   36kB  # and using #![feature(alloc_system)]
```

## Optimizations
- `--release` should make logs less verbose
- `strip(1)` removes DWARF symbols and other debug data
- `upx(1) -9` creates a self-extracting archive
- `#![feature(alloc_system)]` uses the system allocator

## Note on dynamic linking
I really dislike dynamic linking.

## Future stuff
- [Code Gen](https://github.com/rust-lang/rust/pull/32386)
- [Custom Panic Runtimes](https://github.com/rust-lang/rust/pull/32900)

## See Also
- [reddit - binary: can we do better?](https://www.reddit.com/r/rust/comments/4fbm9h/i_created_an_88b_hello_world_binary_can_we_do/)
- [super tiny Rust hello world](https://github.com/retep998/hello-rs)
- [advanced linking](https://doc.rust-lang.org/book/advanced-linking.html)

## License
[MIT](https://tldrlegal.com/license/mit-license)
