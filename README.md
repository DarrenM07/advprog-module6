# Reflection

## Commit 1

The `handle_connection` function takes a `TcpStream` as an argument and reads it using a `BufReader`. The `lines` method extracts each line from the stream, and `map` is used to unwrap the results. Then, `take_while` collects lines as long as they are not empty, and finally, `collect` stores them in a `Vec<String>`.

## Commit 2
![alt text](/assets/image/commit2.png)

## Commit 3
The improvement I made is using an if-else statement to load the page based on the response status.
![alt text](/assets/image/commit3.png)