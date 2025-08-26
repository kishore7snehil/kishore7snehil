

<!--
## Hi there 👋
**kishore7snehil/kishore7snehil** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# Hi, I’m Snehil Kishore 👋

Full‑stack developer & SDK architect with 4+ years of experience building authentication libraries and developer tools at Auth0/Okta. I design secure, scalable APIs in **Python (FastAPI)** and **PHP**, and I’ve contributed extensively to the official Auth0 Python and PHP SDKs.

```python
from dataclasses import dataclass, field
from typing import List


PRONOUNS = ("he", "him")

@dataclass(frozen=True)
class Role:
    company: str
    team: str
    title: str


@dataclass
class Developer:
    name: str
    pronouns: tuple = field(default=PRONOUNS)
    role: Role = field(default=None)
    skills: List[str] = field(default_factory=list)

    def introduce(self) -> str:
        return (
            f"Hi, I'm {self.name}. "
            f"I work at {self.role.company} on the {self.role.team} team as a {self.role.title}. "
            f"My pronouns are {', '.join(self.pronouns)}."
        )

    def list_skills(self) -> str:
        return "Some of my tools & technologies: " + ", ".join(self.skills)


if __name__ == "__main__":
    snehil = Developer(
        name="Snehil Kishore",
        role=Role(company="Okta", team="SDKs / Identity", title="Senior Software Engineer"),
        skills=[
            "Python", "FastAPI", "React", "Node.js", "PHP", "Laravel",
            "Postgres", "Redis", "Docker", "GitHub Actions", "OAuth2/OIDC"
        ]
    )

    print(snehil.introduce())
    print(snehil.list_skills())

```

## 📫 Let’s connect
- [LinkedIn](https://www.linkedin.com/in/snehilkishore)  
<!--- [GitHub](https://github.com/kishore7snehil)  
- [Resume](link-to-your-latest-resume)](url) -->

*Always open to collaborating on open‑source projects and building products.*
