# playground-rus-file-size
Messing around with Rust binaries file size

## Benchmarks
```txt
01  292B  # No optimizations whatsoever
02  289B  # Build with --release flag
03  228B  # Build with --release and strip(1)
04   88B  # --release, strip(1) and upx
```

## License
[MIT](https://tldrlegal.com/license/mit-license)
