# Distributed Map Reduce
An experimental implementation of Map Reduce based on Google's Map Reduce [paper](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf) written in Rust.


## Architecture Diagram
![Arch Diagram](Architecture.png)

## Instructions to Run
First start the coordinator
```
cargo run --bin coordinator -- <n_reduce> <filenames>
```

Example: `cargo run --bin coordinator -- 5 *.txt`

Then start the workers
```
cargo run --bin worker -- 127.0.0.1:12345 <number_of_workers>
```

Example: `cargo run --bin worker -- 127.0.0.1:12345 10`