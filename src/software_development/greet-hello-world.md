```rust
fn greet() -> &'static str { "hello world!" }

#[cfg(test)]
mod tests {
    use super::*;

    #[test]
    fn it_works() {
        let result = greet();
        assert_eq!(result, "sumsi");
    }
}
```
