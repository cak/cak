```sh
$ cargo run

👋 I'm Caleb.
I am passionate about Application Security and enjoy coding in Rust, Swift, Kotlin and TypeScript.
You can find more information at derail.io.
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
        let output = format!("👋 I'm {}.\nI am passionate about {} and enjoy coding in {} and {}.\nYou can find more information at {}.",self.name, self.passion, self.code[..3].join(", "), self.code[3], self.website);
        fmt.write_str(&output)
    }
}
```


 ♥️ ![Rust](https://img.shields.io/badge/-Rust-grey?style=flat-square&logo=Rust) | ![Swift](https://img.shields.io/badge/-Swift-grey?style=flat-square&logo=Swift) | ![Kotlin](https://img.shields.io/badge/-Kotlin-grey?style=flat-square&logo=Kotlin)| ![TypeScript](https://img.shields.io/badge/-TypeScript-grey?style=flat-square&logo=TypeScript)

📇 ![Twitter Follow](https://img.shields.io/twitter/follow/cak?color=purple&label=Twitter%20%40OptionalValue&style=flat-square&link=https://www.twitter.com/optionalvalue/) | ![GitHub followers](https://img.shields.io/github/followers/cak?color=purple&label=Follow%20GitHub&logoColor=blue&style=flat-square&link=https://www.github.com/cak) | [![LinkedIn](https://img.shields.io/badge/-LinkedIn-grey?style=flat-square&logo=Linkedin&color=grey&logoColor=blue&link=https://www.linkedin.com/in/calebk/)](https://www.linkedin.com/in/calebk/) 

👨‍💻 ![GitHub User's stars](https://img.shields.io/github/stars/cak?affiliations=OWNER,ORGANIZATION_MEMBER&color=purple&style=flat-square) 