# playground-rust-file-size
Messing around with Rust binary file size.

## Benchmarks
```txt
01  292B  # No optimizations whatsoever
02  289B  # Build with --release flag
03  228B  # Build with --release and strip(1)
04   88B  # --release, strip(1) and upx
```

## Note on dynamic linking
I really dislike dynamic linking.

## License
[MIT](https://tldrlegal.com/license/mit-license)
