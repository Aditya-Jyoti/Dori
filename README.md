# Dori

Web development is a pain. Spending hours figuring why your web front does not match your design or why your api keeps responding with status 500 are very common causes making you want to quit. But that is just one half of the problem. The other issue you face is to actually deploy it. There are applications out there like Lercel, Leroku (names hidden for legal reasons) that do make this process extremely easy, but they just aren't **open source** and **free to use**.

Simple <ins>web hosting should not be limited to the privileged</ins>. You have a VPS, so you have the right to the ease of seeing website in front of your eyes in minutes. And that's where **Dori** <sub>(dori referenced from japanese word "dorei")</sub> comes in. 

## What?, Why? and How?

<center>
    <img src="./.github/diagram.png" alt="diagram" />
</center>

**Dori** is a terminal user interface made to ease your deployment process to just a few clicks. The way **dori** works is broken down into a few simple steps below :-

1. Understands your project based on your configuration file (generally a `package-lock.json` for node based applications).
2. Generates a `Dockerfile` from our set of templates based on the packages found in the configuration file.
    - The `Dockerfile` is responsible for actually building the project along with running init scripts.
3. Finds a suitable `docker-compose.yml` for the packages used (again from our provided templates) and configures it.
    - The `docker-compose.yml` is responsible for managing the various containers (ie services) used in the project
4. Generates a new "project" with only build and deployment files
5. Pushes these files to the connected VPS and then deploys the website using `docker-compose` tool.

All of these steps earlier had to be done manually, which led to a lot of redundant repetitions. Companies saw the need for this simplification and built **SAAS** products around it. We hope to change that with this **open source** tool.

## Core Developed by Team [Compsoc Majdoor](https://github.com/ComputerSocietyVITC/)

- [Aditya Jyoti](https://github.com/Aditya-Jyoti)
- [Shashwat Mishra](https://github.com/Shashwatm74)
- [Anirudh Sridhar](https://github.com/anirudhsridhar225)
- [Reuben Philip](https://github.com/AltSumpreme)

## License

This project is licensed under the MIT License. You are free to use, modify, and distribute this software under the terms of the [MIT LICENSE](https://github.com/Aditya-Jyoti/Dori/blob/main/LICENSE)
