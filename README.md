# Private-Modpack-Setup
A private, non-commercial Minecraft modpack setup tool for my home lab. It automates preparing client installations and optional dedicated servers for personal multiplayer sessions.

This is a personal home-lab project intended to simplify setting up and testing Minecraft modpacks with my girlfriend and a small group of friends.

We regularly play large modpacks, often containing 300 or more mods. Installing them manually is inconvenient, and the standard CurseForge application does not fit the automated workflow I want to build.

The tool will accept a CurseForge modpack link, prepare the required client files, and optionally set up a dedicated server in an isolated Docker container. A lightweight installer will let our computers download the prepared installation over our local network.

The project is strictly for personal use and private multiplayer sessions. It is not intended to be a commercial launcher, a public mod distribution platform, or a service offered to customers. I may host the tool on my own VPS for convenience, but access will remain limited to me and, at most, a few friends.

I am building it as a practical home-lab and software development project, with an emphasis on automation, reproducibility, and reducing the time required to set up and test modpacks.

The repository now contains an initial C# API solution under `apps/backend` and reusable component projects under `components`. The API is the current development focus. Provider integrations, modpack resolution, installation, persistence, and server management are planned but are not implemented yet.
