# `Vec`

[`Vec`][1] is the standard resizable heap-allocated buffer:

```rust,editable
fn main() {
    let mut numbers = Vec::new();
    numbers.push(42);

    let mut v1 = Vec::new();
    v1.push(42);
    println!("v1: len = {}, capacity = {}", v1.len(), v1.capacity());

    let mut v2 = Vec::with_capacity(v1.len() + 1);
    v2.extend(v1.iter());
    v2.push(9999);
    println!("v2: len = {}, capacity = {}", v2.len(), v2.capacity());
}
```

`Vec` implements [`Deref<Target = [T]>`][2], which means that you can call slice
methods on a `Vec`.

[1]: https://doc.rust-lang.org/std/vec/struct.Vec.html
[2]: https://doc.rust-lang.org/std/vec/struct.Vec.html#deref-methods-[T]
