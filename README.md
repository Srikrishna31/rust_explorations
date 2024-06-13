# rust_explorations

# Rust

Rust is a modern language aimed at both Systems programming and high performance areas. It doesn't use GC unlike other modern languages, and has safety, security and performance guarantees inbuilt.
As such it is gaining traction, and is fast becoming a viable alternative to embedded systems programming, with modern features. Below are some useful links for learning Rust:
[Article about Rust use case in automotive](https://medium.com/@sojan.james/the-case-for-using-rust-for-automotive-software-19400779f126)
[A page listing all interesting applications of Rust](https://robotics.rs/¶)

1. <https://github.com/nrc/r4cppp>

## Useful links to learn Rust

1. <https://doc.rust-lang.org/stable/rust-by-example/>
2. <https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/>
3. <https://doc.rust-lang.org/book/title-page.html>

A good book to learn backend development in Rust:
<https://www.zero2prod.com/index.html> and its github repo: <https://github.com/LukeMathWalker/zero-to-production>

My adaptation of the repo is here: <https://github.com/Srikrishna31/zero2prod>

For people with more mathematical bent of mind can try to adapt a C++ raytracer by following the three part series: <https://raytracing.github.io/books/RayTracingInOneWeekend.html>

My repo of raytracer written in Rust is here: <https://github.com/Srikrishna31/raytracing>

A more hands-on approach to learning rust: <https://github.com/rust-lang/rustlings>
This presents as code that is failing to compile, and your job is to fix the errors to get it to compile, and in the process learning rust.

Performance considerations: <https://nnethercote.github.io/perf-book/introduction.html>

Article about ownership and move semantics comparison in Rust and C++: <https://www.tangramvision.com/blog/c-rust-interior-mutability-moving-and-ownership>

A good series explaining implementing Linked Lists in Rust, en-route explaining Ownership and Borrow semantics: <https://rust-unofficial.github.io/too-many-lists/>

Streams in Rust: <https://www.qovery.com/blog/a-guided-tour-of-streams-in-rust>

### Performance

Rust performance handbook: <https://nnethercote.github.io/perf-book/title-page.html>

## Embedded Rust

Useful links to learn embedded Rust:

1. <https://docs.rust-embedded.org/discovery/microbit/>
2. <https://docs.rust-embedded.org/>
3. <https://docs.rust-embedded.org/book/>
4. [Rust OS tutorial](https://github.com/rust-embedded/rust-raspberrypi-OS-tutorials)

## Comparisons with other languages

1. [Rust vs Haskell](https://levelup.gitconnected.com/rust-vs-haskell-eb5d343d7be0)
2. [Rust vs C++](https://www.bairesdev.com/blog/when-speed-matters-comparing-rust-and-c/)
3. [Rust vs Swift](https://blog.logrocket.com/swift-vs-rust-comparison-guide/)

## State machine design explorations

State machines are an important design pattern which are encountered frequently in various domains of software. From web servers/apps to embedded applications, they are everywhere and help us solve important problems in a clean 
and neat way if designed rightly. Taken from [Hoverbear's blog](https://hoverbear.org/blog/rust-state-machine-pattern/), following are some of the goals of a good state machine implementation:

1. Can only be in one state at a time.
2. Each state should be able to have its own associated values if required.
3. Transitioning between states should have well defined semantics
4. It should be possible to have some level of shared state.
5. Only explicitly defined transitions should be permitted.
6. Changing from one state to another should consume the state so it can no longer be used.
7. We shouldn't need to allocate memory for all states. No more than largest sized state certainly.
8. Any error messages should be easy to understand.
9. We shouldn't need to resort to heap allocations to do this. Everything should be possible on the stack.
10. The type system should be harnessed to our greatest ability.
11. As many errors as possible should be at compile time.

The below links provide various explorations done by different people with above requirements in mind (and probably relaxing some of them for flexibility), which lead to different design possibilities:

1. [https://refactoring.guru/design-patterns/state/rust/example]
2. [https://hoverbear.org/blog/rust-state-machine-pattern/]
3. [https://blog.yoshuawuyts.com/state-machines-2/]
4. [https://blog.yoshuawuyts.com/state-machines-3/]
5. [https://dev.to/senyeezus/designing-state-machines-in-rust-252k]
6. [https://deislabs.io/posts/a-fistful-of-states/]
7. [https://medium.com/@danny.moghnie/a-simple-state-machine-library-in-rust-2b4f810ec61d]

## Work towards getting Rust qualify for ASIL-D

1. [https://ferrous-systems.com/blog/ferrocene-language-specification/]
2. [https://ferrous-systems.com/ferrocene/]

## Rust compiler development guidelines

This is a useful reference to understand how the community works to develop future versions of Rust: [https://rustc-dev-guide.rust-lang.org/getting-started.html]

## Some of the most useful Rust libraries

<https://jondot.medium.com/12-killer-rust-libraries-you-should-know-c60bab07624f>

## Experimenting with compiler flags for binary size vs speed

1. [https://stackoverflow.com/questions/68327937/how-to-optimize-the-size-of-the-executable-binary-file-for-native-and-wasm-toolc]
2. [https://github.com/johnthagen/min-sized-rust#build-in-release-mode]
3. [https://doc.rust-lang.org/cargo/reference/unstable.html#build-std]
4. [https://github.com/RazrFalcon/cargo-bloat]

## Parallel programming

1. <https://blog.logrocket.com/implementing-data-parallelism-rayon-rust/>

## Rust FFI

1. Some stack-overflow pages concerning passing structs to C/C++ from Rust:

    a. [https://stackoverflow.com/questions/64439168/how-can-i-safely-share-objects-between-rust-and-c]
    b. [https://stackoverflow.com/questions/58311426/how-do-i-use-cbindgen-to-return-and-free-a-boxvec]
    c. [https://stackoverflow.com/questions/62338832/how-to-hold-rust-objects-in-rust-code-created-through-c]

2. [CBindgen library which generates C/C++ headers based on Rust](https://docs.rs/cbindgen/latest/cbindgen/fn.generate.html)

    a. [A simple example](https://github.com/JoshuaBatty/cbindgen_simple_example/blob/master/build.rs)

3. [Box::from_raw, Box::into_raw which can be used to pass objects to C++ and have them destroyed in Rust](https://doc.rust-lang.org/beta/std/boxed/index.html#memory-layout)

4. [A detailed walkthrough of Rust FFI, with a sample implementation of Plugin System as well](https://michael-f-bryan.github.io/rust-ffi-guide/overview.html)

5. [https://github.com/mozilla/cbindgen]

## Bazel with Rust

1. [Article explaining how to build Rust crates with Bazel](https://earthly.dev/blog/bazel-with-rust/)
2. [https://anders.dev/bazel-build-system-and-rust/]
3. [Cargo Raze - Tool to generate BUILD files from Cargo.toml files](https://github.com/google/cargo-raze)
4. [Rules Rust](http://bazelbuild.github.io/rules_rust/crate_universe.html)

## Supported Platforms for Rust

1. [https://doc.rust-lang.org/rustc/platform-support.html]

## Idiomatic Rust

1. [https://github.com/mre/idiomatic-rust]

## CUDA Rust

1. [https://rust-gpu.github.io/Rust-CUDA/index.html]
2. [https://github.com/EmbarkStudios/rust-gpu]
3. [https://embarkstudios.github.io/rust-gpu/book/]
