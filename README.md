```sh
$ cargo run

👋 I'm Caleb.
I am a Christian, father, hacker and runner.
I am passionate about Application Security.
You can find more information at derail.io.
```

```rust
// main.rs

fn main() {
    let cak = AboutMe {
        name: "Caleb",
        passion: "Application Security",
        roles: vec!["Christian", "father", "hacker", "runner"],
        website: "derail.io",
    };

    println!("{:?}", cak);
}

struct AboutMe<'a> {
    name: &'a str,
    passion: &'a str,
    roles: Vec<&'a str>,
    website: &'a str,
}

impl fmt::Debug for AboutMe<'_> {
    fn fmt(&self, fmt: &mut fmt::Formatter<'_>) -> fmt::Result {
        let output = format!(
            "👋 I'm {}.\nI am a {} and {}.\nI am passionate about {}.\nYou can find more information at {}.",
            self.name,
            self.roles[..3].join(", "),
            self.roles[3],
            self.passion,
            self.website
        );
        fmt.write_str(&output)
    }
}
```


 ♥️ [![Rust](https://img.shields.io/badge/-Rust-grey?style=flat-square&logo=Rust)](https://www.rust-lang.org) | [![Go](https://img.shields.io/badge/-Go-grey?style=flat-square&logo=Go)](https://golang.org) | [![Swift](https://img.shields.io/badge/-Swift-grey?style=flat-square&logo=Swift)](https://swift.org) | [![Kotlin](https://img.shields.io/badge/-Kotlin-grey?style=flat-square&logo=Kotlin)](https://kotlinlang.org) | [![TypeScript](https://img.shields.io/badge/-TypeScript-grey?style=flat-square&logo=TypeScript)](https://www.typescriptlang.org)

📇 [![derail.io](https://img.shields.io/badge/Website-derail.io-blue?color=purple&style=flat-square)](https://derail.io) | [![Twitter Follow](https://img.shields.io/twitter/follow/optionalvalue?color=purple&label=Twitter%20%40OptionalValue&style=flat-square)](https://www.twitter.com/optionalvalue/) | [![GitHub followers](https://img.shields.io/github/followers/cak?color=purple&label=Follow%20GitHub&logoColor=blue&style=flat-square)](https://www.github.com/cak) | [![LinkedIn](https://img.shields.io/badge/-LinkedIn-grey?style=flat-square&logo=Linkedin&color=grey&logoColor=blue&link=https://www.linkedin.com/in/calebk/)](https://www.linkedin.com/in/calebk/) 

👨‍💻 [![cak's stars](https://img.shields.io/github/stars/cak?affiliations=OWNER,ORGANIZATION_MEMBER&color=purple&style=flat-square)](https://www.github.com/cak)