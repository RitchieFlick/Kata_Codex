```rust
fn greet() -> &'static str { "hello world!" }

#[test]
fn it_works() {
    let result = greet();
    assert_eq!(result, "sumsi");
}
```
