## Classes and Objects Explained

At the core of Object-Oriented Programming (OOP) are two key concepts: **classes** and **objects**.

A **class** is a **blueprint** for creating things. Think of it like a cookie cutter 🍪. The cutter defines the shape (the data or **attributes**) and the process of making the cookie (the behavior or **methods**), but it isn't a cookie itself.

An **object** is the **actual thing** created from that blueprint. It's the cookie you make using the cutter. You can create many independent objects (cookies) from a single class (the cutter), and each one can have its own unique details (like different sprinkles).

-----

## The Rust Approach: Structs and Impl

Rust is not a traditional OOP language and does not have the `class` keyword. Instead, it achieves similar results by combining `structs` (for data) and `impl` blocks (for behavior).

  * **`struct`**: This is Rust's blueprint for data. It defines the **attributes** (called **fields**) that an object will have.
  * **`impl`**: The implementation block is where you define **methods** (behavior) for a `struct`.

An **instance** of a `struct` is the Rust equivalent of an **object**.

### Coding Example in Rust

Let's create a blueprint for a `Book`. The `struct` will define its data, and the `impl` block will define what it can do.

```rust
// The blueprint for the data (like class attributes)
struct Book {
    title: String,
    author: String,
    pages: u32,
}

// The implementation block for behavior (like class methods)
impl Book {
    // This is an "associated function" that acts like a constructor.
    // It creates and returns a new instance of the Book struct.
    fn new(title: String, author: String, pages: u32) -> Self {
        Self {
            title,
            author,
            pages,
        }
    }

    // This is a method. It uses the data of a specific Book instance.
    // `&self` means it borrows the instance to read its data.
    fn summary(&self) {
        println!("'{}' by {} is {} pages long.", self.title, self.author, self.pages);
    }
}

fn main() {
    // Create an object (instance) of the Book struct
    let book1 = Book::new(
        "The Hobbit".to_string(),
        "J.R.R. Tolkien".to_string(),
        310
    );

    // Create another independent object
    let book2 = Book::new(
        "Dune".to_string(),
        "Frank Herbert".to_string(),
        412
    );

    // Call the summary method on each object
    book1.summary();
    book2.summary();
}
```

#### **Output:**

```
'The Hobbit' by J.R.R. Tolkien is 310 pages long.
'Dune' by Frank Herbert is 412 pages long.
```

In this example, `Book` is the blueprint (`struct` + `impl`). `book1` and `book2` are two separate **objects** (instances), each with its own independent data but sharing the same `summary` behavior.