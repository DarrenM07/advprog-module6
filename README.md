# Reflection

## Commit 1

The `handle_connection` function takes a `TcpStream` as an argument and reads it using a `BufReader`. The `lines` method extracts each line from the stream, and `map` is used to unwrap the results. Then, `take_while` collects lines as long as they are not empty, and finally, `collect` stores them in a `Vec<String>`.

## Commit 2
![alt text](/assets/image/commit2.png)

## Commit 3
The improvement I made is using an if-else statement to load the page based on the response status.
![alt text](/assets/image/commit3.png)

## Commit 4
The `sleep` version runs slower because the code explicitly instructs the thread to pause for 10 seconds with this line: `thread::sleep(Duration::from_secs(10));`.

## Commit 5
The `pool` is utilized to enhance a program's throughput by assigning tasks to available threads in the pool while other threads remain idle until they receive a task.

## Bonus Reflection
I added a `build()` function in the `ThreadPool` implementation as an alternative to the conventional `new()` constructor. This was done to explore naming conventions and gain a deeper understanding of API design principles in Rust. The `build()` method mirrors `new()` in functionality, carrying out the same steps of creating a channel, wrapping it in a `Mutex` and `Arc`, and initializing worker threads.  

Using a name like `build()` can be beneficial when constructing an object that requires a more intricate setup or configuration. It also aligns with patterns found in many Rust libraries, where `build()` is commonly used in anticipation of a builder pattern. While `new()` and `build()` function identically in this case, `build()` can provide clearer intent for developers reading the code.  

The primary distinction between `new()` and `build()` lies in convention—`new()` is the typical method for straightforward object creation in Rust, whereas `build()` often suggests a more flexible or configurable initialization process, frequently seen in builder patterns.