# Mission Reflection

## How does `docker-compose.yml` make an engineer’s job easier?
Writing a Compose file turns dozens of manual steps into a single, repeatable command. Instead of remembering and typing long `docker run` commands with all their flags, ports, and variables — once for the database, once for the app — I define everything once in code. I can deploy the full stack with `docker-compose up -d` and remove it completely with `docker-compose down`. It eliminates typos, forgotten settings, and inconsistent environments. The same file works on my machine, in the lab, and in production — "it works here" becomes "it works everywhere."

## What happens with indentation errors in YAML?
YAML is extremely sensitive to whitespace. Using a Tab instead of spaces, or mismatched indentation levels, causes Compose to reject the file immediately with a parse error. The structure defines meaning — incorrect spacing breaks the hierarchy, and Compose can’t tell which variable belongs to which service. It’s a strict but fair system: consistent formatting guarantees predictable structure.

## Why use environment variables?
Hard‑coding passwords and settings into an image is insecure and inflexible. Environment variables let us pass configuration at runtime without baking it into the container itself. Sensitive values stay out of version control, and we can reuse the same Nextcloud or MariaDB image across dev, test, and production just by changing the variables — no rebuild needed. It’s a core security and portability practice.

## Deploying enterprise software in minutes — how did it feel?
It felt powerful. Just a few lines of code stood up what would otherwise take hours: installing a database, configuring users, downloading and setting up Nextcloud, connecting them securely. It highlighted how cloud computing is less about manual installation and more about orchestration — describing what you want, and letting the system assemble it. It also felt a little humbling; the complexity hasn’t vanished, it’s just been abstracted — and understanding that abstraction is what makes you the engineer, not just a user.

## How has my understanding evolved since Mission 1?
I started thinking of "cloud computing" as just "someone else’s computer" — a place to upload files. Now I see it as **infrastructure as code**: servers, networks, databases, and applications all described in text files, version‑controlled, replicated, and automated. I’ve moved from "how do I install this?" to "how do I design, declare, and orchestrate this?" Cloud computing isn’t just using the web — it’s building the systems that power it, and doing so with the same discipline as software development itself.
