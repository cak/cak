```sh
$ cargo run

👋 I'm Caleb. I am passionate about Application Security and enjoy coding in Rust, Swift, Kotlin and TypeScript. You can find more information at derail.io.
```

```rust
// main.rs

fn main() {
    let cak = AboutMe {
        name: "Caleb",
        passion: "Application Security",
        code: vec!["Rust", "Swift", "Kotlin", "TypeScript"],
        website: "derail.io",
    };

    println!("{:?}", cak);
}

struct AboutMe<'a> {
    name: &'a str,
    passion: &'a str,
    code: Vec<&'a str>,
    website: &'a str,
}

impl fmt::Debug for AboutMe<'_> {
    fn fmt(&self, fmt: &mut fmt::Formatter<'_>) -> fmt::Result {
        let output = format!("👋 I'm {}. I am passionate about {} and enjoy coding in {} and {}. You can find more information at {}.",self.name, self.passion, self.code[..3].join(", "), self.code[3], self.website);
        fmt.write_str(&output)
    }
}
```


 ♥️![Rust](https://img.shields.io/badge/-Rust-black?style=flat-square&logo=Rust) | ![Swift](https://img.shields.io/badge/-Swift-black?style=flat-square&logo=Swift) | ![Kotlin](https://img.shields.io/badge/-Kotlin-black?style=flat-square&logo=Kotlin)| ![TypeScript](https://img.shields.io/badge/-TypeScript-black?style=flat-square&logo=TypeScript)

[![Twitter: OptionalValue](https://img.shields.io/twitter/follow/OptionalValue?style=flat-square)](https://twitter.com/optionalvalue) | [![GitHub cak](https://img.shields.io/github/followers/cak?label=follow%20github&style=flat-square)](https://github.com/cak) | ![visitors](https://visitor-badge.glitch.me/badge?page_id=cak.readme)
