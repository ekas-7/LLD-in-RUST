# LLD-in-RUST

This repository contains curated resources and interview practice materials to learn Low-Level Design (LLD) / Object-Oriented Design (OOD), and to prepare for system and design interviews — presented with a Rust lens.

Whether you're learning design concepts for the first time or preparing for interviews, this repo gathers patterns, principles, UML, and problem walkthroughs with example Rust code and design notes.

## What's inside

- Fundamental Concepts
  - Basics of OOP (as applicable in Rust)
  - DRY, YAGNI, KISS
  - SOLID principles (adapted for Rust idioms)

- Design Patterns (with Rust examples where appropriate)
  - Creational: Singleton, Factory Method, Abstract Factory, Builder, Prototype
  - Structural: Adapter, Bridge, Composite, Decorator, Facade, Flyweight, Proxy
  - Behavioral: Iterator, Observer, Strategy, Command, State, Template Method, Visitor, Chain of Responsibility, Mediator, Memento

- UML & Modeling
  - Class diagrams (structs, traits, enums)
  - Use case diagrams
  - Sequence diagrams
  - Activity diagrams
  - State machine diagrams

- LLD Interview Problems
  - Easy: Parking Lot, Stack Overflow, Vending Machine, Logging Framework, Traffic Signal, Coffee Vending Machine, Task Management System
  - Medium: ATM, LinkedIn, LRU Cache, Tic Tac Toe, Pub/Sub, Elevator, Car Rental, Online Auction, Hotel Management, Digital Wallet, Airline, Library, Social Network, Restaurant, Concert Ticket Booking
  - Hard: CricInfo, Splitwise, Chess, Snake & Ladder, Ride-Sharing (Uber), Course Registration, Movie Ticket Booking, E-commerce (Amazon), Stock Brokerage, Music Streaming (Spotify), Food Delivery (Swiggy)

- Courses & Books
  - Master LLD Interviews - AlgoMaster.io
  - Head First Design Patterns
  - Clean Code
  - Refactoring: Improving the Design of Existing Code

- Newsletter
  - AlgoMaster Newsletter

## Why Rust?
Rust enforces memory safety and has powerful type and trait systems that influence the way you design software. This repository adapts traditional OOD/LLD techniques to Rust's idioms — using struct composition, traits (instead of classical subclassing), enums for algebraic data types, and ownership-aware APIs.

Expect guidance on:
- Mapping SOLID principles to Rust (when they apply and when to prefer Rust-specific patterns)
- Replacing inheritance with trait-based polymorphism and composition
- Thread-safe designs using ownership and concurrency primitives (e.g., Arc, Mutex)
- Idiomatic error handling with Result and Option

## Example layout for a problem (suggested)
Each design problem in this repo should include:
1. Problem statement and requirements (functional + non-functional)
2. Constraints and assumptions
3. High-level design (textual + small UML/ASCII diagrams)
4. Data model (structs, enums, traits)
5. Key APIs and methods with signatures
6. One or more small Rust code examples and tests
7. Discussion of trade-offs and scaling concerns

## Contributing
Contributions are welcome!

If you'd like to add a new problem, improve existing content, or add Rust example code:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature-name`
3. Add your changes and commit: `git commit -m "Add <feature/notes>"
4. Push your branch and open a pull request

Please update README files and documentation as appropriate. Add small tests or example programs when possible.

## How to add a Rust example
Create a new folder for the problem (e.g., `designs/parking_lot`) and include:
- `Cargo.toml` (if you want an isolated crate)
- `src/lib.rs` or `src/main.rs` with example code
- `tests/` for unit/integration tests
- `README.md` documenting the design and usage

Quick commands to create an example crate:

```bash
cd designs
cargo new --lib parking_lot
cd parking_lot
# add your code in src/lib.rs and tests in tests/
cargo test
```

## License
This repository is provided as-is for learning purposes. Please include license information on contributions.

## Contact & Newsletter
For a deeper guided experience, check out AlgoMaster.io and subscribe to the AlgoMaster Newsletter.

---

Happy designing — with Rust!