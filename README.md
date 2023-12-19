```
use std::io;

fn main() {

    let mut language: String = String::new();
    let mut stack: Vec<&str> = Vec::new();
    
    println!("Hi there, I'm Anton, a backend developer, type language:");

    io::stdin().read_line(&mut language).expect("Sorry, I understand only string format");

    let language: String = language.trim().to_lowercase();

    match language.as_str() {
        "python" => {
            stack = vec!["Python 3.v", "Django", "FastApi", "Flask", "SQLAlchemy", "SQLModel", "Tortoise ORM", "bs4"];
        }
        "rust" => {
            stack = vec!["Rust", "Actix-web", "Rocket", "Tokio", "Diesel", "SQLx"];
        }
        _ => {
            println!("Sorry, I don't know this language");
        }
    }

    if !stack.is_empty() {
        let other_skills = vec![
            "SQL", "PostgreSQL", "JavaScript", "HTML", "CSS", "Docker", "Nginx", "Git", "Redis", "Celery", "Kafka",
        ];
        println!("My stack: {:?}", stack);
        println!("My other skills: {:?}", other_skills);
    }
}
```







