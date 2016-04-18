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

## Note on dynamic linking
I really dislike dynamic linking.

## License
[MIT](https://tldrlegal.com/license/mit-license)
