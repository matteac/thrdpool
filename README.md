# ThreadPool
A simple package to run multiple jobs in a threadpool

```rs
    // you can handle 4 connections !!!!!!
    let pool = ThreadPool::new(4);
    for stream in listener.incoming() {
        let stream = stream.unwrap();
        pool.execute(|| {
            handle_connection(stream);
            println!("Connection handled!");
        })
    }
```