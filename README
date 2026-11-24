<a id="readme-top"></a>

[![Contributors][contributors-shield]][contributors-url]

[![Forks][forks-shield]][forks-url]

[![Stargazers][stars-shield]][stars-url]

[![Issues][issues-shield]][issues-url]

[![License][license-shield]][license-url]

<!-- Add a LinkedIn badge when the project profile URL is available. -->

<br />
<div align="center">
  <a href="https://github.com/mithscape/mithscape">
    <img src="http://mithscape.com/assets/mithscape-badge-v1.png" alt="Logo" width="500" height="80">
  </a>

  <h1 align="center">MithScape</h1>

  <p align="center">
    An authentic, highly modular Old School RuneScape (OSRS) server and client ecosystem featuring revision 235 &amp; 242 protocols, native Sailing skill implementation, autonomous bot population, dynamic quest graph engine, and unified multi-world persistence. Oh! And we brought back <strong>Summoning</strong>!
    <br />
    <a href="docs/README.md"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="http://mithscape.com">Visit Website</a>
    &middot;
    <a href="https://github.com/mithscape/mithscape/issues/new?labels=bug&amp;template=bug-report---.md">Report Bug</a>
    &middot;
    <a href="https://github.com/mithscape/mithscape/issues/new?labels=enhancement&amp;template=feature-request---.md">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>

  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

<!-- Add a project screenshot here when its image URL is available. -->

Most private server projects either strip out newer client features or get stuck on decade-old revisions. **MithScape** is built to run modern OSRS revisions (pinned to 235 and 242) both locally and on a dedicated server. It gives you an authentic native client experience, custom skill additions like Sailing, and autonomous bots so the world doesn't feel like a ghost town when you're playing solo.

We wanted a setup where you can just boot up the game, create an account, and start playing without wrestling with desynced character saves, broken packet handshakes, or fragile configs. Everything—your stats, bank, inventory, and quest journal—is tied to a shared database, meaning you can jump between our main world, the PvP world, or our live VPS without losing a single XP drop.

A few highlights of what's in the box:

- **Playable Sailing &amp; Summoning:** Skill tab integration, proper XP progression, skill guides, and familiar mechanics right in the native client.
- **Autonomous Player Bots:** Not just decorative NPCs—these are real player entities wandering around with proper collision checks and persistent saving when the server turns off.
- **One Account Everywhere:** Log into World 1, hop over to World 2 for PvP, or connect to our live STRATO VPS. Your character, bank, and quest stages follow you everywhere.
- **Hand-Crafted Quests:** A growing library of fully scripted quests (*Druidic Ritual*, *Witch's House*, *Recruitment Drive*, *Shield of Arrav*, *Vampire Slayer*, etc.) with authentic dialogues, cutscenes, and mechanics.
- **Play on PC, Linux, or Mobile:** One-click launchers for Windows, shell scripts for Linux desktop, and ready-to-install Android APKs (`Play-OSRS.apk`).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

The server runs on Kotlin and modern Java with asynchronous netcode, backed by a clean relational database schema:

- [![Kotlin][Kotlin.io]][Kotlin-url]
- [![Java][Java.com]][Java-url]
- [![Gradle][Gradle.org]][Gradle-url]
- [![MySQL][MySQL.com]][MySQL-url]
- [![Node.js][Node.js]][Node-url]
- [![PowerShell][PowerShell]][PowerShell-url]
- [![Bash][Bash.org]][Bash-url]
- [![PHP][PHP.net]][PHP-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

Getting a local world running on your machine only takes a few minutes. Follow these steps to get everything set up.

### Prerequisites

Here's what you need installed before running the server:

- **Java 21+ (JDK):** Make sure you have a modern JDK installed (Eclipse Temurin 21 or OpenJDK).

  ```sh
  java -version
  ```

- **Node.js (v18+):** Powers the local configuration and world-list services.

  ```sh
  node --version
  ```

- **MySQL / MariaDB:** Stores website accounts and game progress (XAMPP works great locally, or you can use our SSH tunnel to connect to the remote database).
- **PowerShell 7+** (on Windows) or **Bash** (on Linux/macOS).

### Installation

1. Clone the repo

   ```sh
   git clone https://github.com/mithscape/mithscape.git
   cd mithscape
   ```

2. Run the automated setup script to build the server and extract cache data

   ```powershell
   .\Setup.ps1
   ```

3. Make sure your database is running, or start the encrypted database tunnel to STRATO

   ```powershell
   .\scripts\Start-DatabaseTunnel.ps1
   ```

4. Run the local service checks to make sure your ports and configs match up

   ```sh
   node --test tests/local-services.test.mjs
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- USAGE EXAMPLES -->

## Usage

### Start World 1 (with Bots)

Double-click `Play.cmd` or run the launcher in PowerShell. You can choose how many bots you want roaming around:

```powershell
# Launch with 12 bots wandering Lumbridge and surrounding areas
.\Play.ps1 -Bots 12
# Play completely solo (0 bots)
.\Play.ps1 -Bots 0
```

### Jump into the PvP World (World 2)

To hop into the dangerous PvP world with your existing character and stats:

```powershell
.\Play-PvP.cmd
```

### Connect to the Live Dedicated Server (STRATO VPS)

If you want to play on the live public server hosted on our STRATO VPS (`85.215.38.71`):

```powershell
.\Play-Strato.cmd
```

### Run Both Worlds Together

To run both World 1 and World 2 on the same machine to test cross-world session locking:

```powershell
.\Play-Both.cmd
```

### Playing on Mobile & Linux

- **Android:** Grab `Play-OSRS.apk` or `Play-Sailing.apk` from the root folder and install it directly on your Android phone or tablet.
- **Linux Desktop:** Run `./MithScape.sh` or `./Play-OSRS.sh` directly from your terminal.

_For more technical details and quest walkthroughs, check out the [Docs folder](docs/README.md) and [Tutorial Island guide](docs/TUTORIAL.md)._

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->

## Roadmap

- [x] Pinned RSMod engine baseline for OSRS revisions 235 &amp; 242
- [x] Sailing skill registration, XP curve, and custom interface tab
- [x] Roaming player bots with collision checks and graceful saving on shutdown
- [x] Unified MySQL account backend (`runescape.members` &amp; normalized `game_*` tables)
- [x] Tutorial Island walkthrough with persistent character creation
- [x] Multi-world session lock (blocks duplicate logins &amp; prevents save rollbacks)
- [x] Live VPS deployment with private SSH database tunneling
- [x] Content Studio dynamic quest pipeline (210+ releases)
  - [x] *Druidic Ritual* (Herblore unlock &amp; Cauldron of Thunder dipping)
  - [x] *Recruitment Drive* (Temple trials, Sir Leye prophecy &amp; Initiate armor)
  - [x] *Witch's House* (Garden infiltration &amp; 4-phase shapeshifter fight)
  - [x] *Shield of Arrav* (Phoenix &amp; Black Arm gangs with solo helper broker)
  - [x] *Vampire Slayer* &amp; *Demon Slayer* authentic quest flows
- [x] 15-family native pet support (following, overlap pickup, relog resume)
- [ ] Smarter bot routines (skilling loops, banking, trading, and combat AI)
- [ ] Open sea navigation and boat upgrades for Sailing
- [ ] Cross-world Grand Exchange order matching
- [ ] God Wars Dungeon &amp; Raids encounter script ports

See the [open issues](https://github.com/mithscape/mithscape/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Top contributors:

<a href="https://github.com/mithscape/mithscape/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=mithscape/mithscape" alt="contrib.rocks image" />
</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

## License

Distributed under the ISC and MIT Licenses. See `LICENSE.md` and `client/LICENSE` for more information.

> [!NOTE]

> RuneScape and Old School RuneScape are registered trademarks of Jagex Limited. MithScape is in no way, shape or form affiliated with Jagex.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

## Contact

MithScape Project Team - [@mithscape](https://twitter.com/mithscape) - contact@mithscape.com

Project Link: [https://github.com/mithscape/mithscape](https://github.com/mithscape/mithscape)

Website: [http://mithscape.com](http://mithscape.com)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->

## Acknowledgments

Huge thanks to the open-source projects, tools, and research communities that made this possible:

- [RSMod Framework](https://github.com/rsmod/rsmod)
- [2009Scape Project](https://github.com/2009scape/2009scape)
- [Blurite / RSProx Client Tools](https://github.com/blurite/rsprox)
- [OpenRune OSRS Server Resources](https://github.com/OpenRune/OpenRune-Server)
- [Avexiis OS Map Viewer](https://github.com/Avexiis/os-map-viewer)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
[contributors-shield]: https://img.shields.io/github/contributors/mithscape/mithscape?style=for-the-badge
[contributors-url]: https://github.com/mithscape/mithscape/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mithscape/mithscape?style=for-the-badge
[forks-url]: https://github.com/mithscape/mithscape/network/members
[stars-shield]: https://img.shields.io/github/stars/mithscape/mithscape?style=for-the-badge
[stars-url]: https://github.com/mithscape/mithscape/stargazers
[issues-shield]: https://img.shields.io/github/issues/mithscape/mithscape?style=for-the-badge
[issues-url]: https://github.com/mithscape/mithscape/issues
[license-shield]: https://img.shields.io/github/license/mithscape/mithscape?style=for-the-badge
[license-url]: https://github.com/mithscape/mithscape/blob/HEAD/LICENSE.md
[Kotlin.io]: https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white
[Kotlin-url]: https://kotlinlang.org/
[Java.com]: https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white
[Java-url]: https://www.java.com/
[Gradle.org]: https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logo=gradle&logoColor=white
[Gradle-url]: https://gradle.org/
[MySQL.com]: https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white
[MySQL-url]: https://www.mysql.com/
[Node.js]: https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white
[Node-url]: https://nodejs.org/
[PowerShell]: https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white
[PowerShell-url]: https://learn.microsoft.com/powershell/
[Bash.org]: https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnubash&logoColor=white
[Bash-url]: https://www.gnu.org/software/bash/
[PHP.net]: https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white
[PHP-url]: https://www.php.net/
