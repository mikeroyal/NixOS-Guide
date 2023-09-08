<h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/128645103-795eebbd-f853-47cc-8087-916dfd98347b.png">
  <br />
   NixOS Guide
</h1>

<a href="https://github.com/mikeroyal?tab=followers">
         <img alt="followers" title="Follow for Updates" src="https://custom-icon-badges.demolab.com/github/followers/mikeroyal?color=236ad3&labelColor=1155ba&style=for-the-badge&logo=person-add&label=Follow&logoColor=white"/></a> 

![Maintenance](https://img.shields.io/maintenance/yes/2023?style=for-the-badge)
![Last-Commit](https://img.shields.io/github/last-commit/mikeroyal/nixos-guide?style=for-the-badge)

#### A guide on setting up your NixOS Desktop with all the essential Applications, Tools, and Games to make your experience with NixOS great! This may not be perfect guide for everyone but I feel there is at least one or more perfect solutions for New and Advanced NixOS users.

**Note: You can easily convert this markdown file to a PDF in [VSCode](https://code.visualstudio.com/) using this handy extension [Markdown PDF](https://marketplace.visualstudio.com/items?itemName=yzane.markdown-pdf).**

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/128645106-874b3883-1d6f-46b8-86f4-2cefd54d4117.png">
  <br />
</p>

# Table of Contents

1. [Getting Started](https://github.com/mikeroyal/NixOS-Guide#getting-started)

   - [NixOS Developer Resources](https://github.com/mikeroyal/NixOS-Guide#NixOS-developer-resources)
   - [NixOS YouTube Tutorials](#youtube-tutorials)
   - [NixOS Tools & Modules](https://github.com/mikeroyal/NixOS-Guide#NixOS-Tools-and-Modules)
   - [NixOS Desktop](https://github.com/mikeroyal/NixOS-Guide#NixOS-Desktop)   
   - [Programming Languages & Frameworks with NixOS support](https://github.com/mikeroyal/NixOS-Guide#programming-languages--with-nixos-support)
    
     - [C](#C)
     - [Python](#python)
     - [Ruby](#ruby)
     - [Go](h#Go)
     - [Rust](#rust)
     - [Scala](#scala)
     - [Clojure](#Clojure)
     - [Haskell](#haskell)
     - [Node.js](#nodejs)
     - [PHP](#php)
     - [Perl](#Perl)
     - [Java](#Java)
     - [Lua](#Lua)
     - [LLVM](#LLVM)
     - [Julia](#Julia)
     - [R](#R)
     - [Arduino](#Arduino)
     - [Crystal](#Crystal)
     - [Lisp](#lisp)
     - [Nim](#nim)
     - [Elm](#Elm)
     - [Elixir](#elixir)
     - [Erlang](#erlang)
     - [DotNet](#dotnet)
     - [CUDA](#cuda)
     - [Qt](#qt)

2. [Getting Software](https://github.com/mikeroyal/NixOS-Guide#getting-software)

3. [Gaming](https://github.com/mikeroyal/NixOS-Guide/blob/main/README.md#gaming)

   - [Steam](https://github.com/mikeroyal/NixOS-Guide#steam)
   - [ProtonDB](https://github.com/mikeroyal/NixOS-Guide#protondb)
   - [Lutris](https://github.com/mikeroyal/NixOS-Guide#lutris)
   - [GameHub](https://github.com/mikeroyal/NixOS-Guide#gamehub)
   - [Epic Games Store](https://github.com/mikeroyal/NixOS-Guide#epic-games-store)
   - [Game Streaming](https://github.com/mikeroyal/NixOS-Guide#game-streaming)
   - [Game Emulators](https://github.com/mikeroyal/NixOS-Guide#game-emulators)
   - [Graphics Performance](https://github.com/mikeroyal/NixOS-Guide#graphics-performance)
   - [WINE](https://github.com/mikeroyal/NixOS-Guide#wine)

4. [Setting up a macOS Workspace](https://github.com/mikeroyal/NixOS-Guide#setting-up-a-macos-workspace)

5. [Setting up a Windows 10 Workspace](https://github.com/mikeroyal/NixOS-Guide#setting-up-a-windows-10-workspace)

6. [Using Android and Android Apps on Linux](https://github.com/mikeroyal/NixOS-Guide#using-android-and-android-apps-on-linux)

7. [Professional Audio/Video Editing](https://github.com/mikeroyal/NixOS-Guide#professional-audio--video-editing)

8. [Kubernetes](https://github.com/mikeroyal/NixOS-Guide#kubernetes)

9. [Machine Learning](https://github.com/mikeroyal/NixOS-Guide#machine-learning)

10. [Robotics](https://github.com/mikeroyal/NixOS-Guide#robotics)

11. [Open Source Security](https://github.com/mikeroyal/NixOS-Guide#open-source-security)

12. [Differential Privacy](https://github.com/mikeroyal/NixOS-Guide#differential-privacy)

13. [Cloud Native Development](https://github.com/mikeroyal/NixOS-Guide#cloud-native-development)

14. [DevOps Development](https://github.com/mikeroyal/NixOS-Guide#devops-development)

15. [Networking](https://github.com/mikeroyal/NixOS-Guide#networking)

16. [Databases](https://github.com/mikeroyal/NixOS-Guide#databases)


# Getting Started

[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[NixOS](https://nixos.org/) is a Linux distribution built on top of the [Nix package manager](https://nixos.wiki/wiki/Nix). It has tools dedicated to DevOps and deployment tasks.

[Nix Tour](https://nixcloud.io/tour/) is an interactive tour that uses the actual package manager to learn you the language by example, in the browser.

[Nix](https://nixos.wiki/wiki/Nix) is a package manager and build system that parses reproducible build instructions specified in the [Nix Expression Language](https://nixos.wiki/wiki/Nix_Expression_Language), is a pure functional language with lazy evaluation. Nix expressions are pure functions taking dependencies as arguments and producing derivation specifying a reproducible build environment for the package. Nix stores the results of the build in unique addresses specified by a hash of the complete dependency tree, creating an immutable package store that allows for atomic upgrades, rollbacks and concurrent installation of different versions of a package, essentially eliminating [dependency hell](https://en.wikipedia.org/wiki/Dependency_hell).

[Nix Expression Language](https://nixos.wiki/wiki/Nix_Expression_Language) is a pure, lazy, functional language. Purity means that operations in the language don't have side-effects (for instance, there is no variable assignment). The language is not a full-featured, general purpose language. Its main job is to describe packages, compositions of packages, and the variability within packages.

[Nixpkgs](https://nixos.wiki/wiki/Nixpkgs) is the largest repository of [Nix](https://nixos.wiki/wiki/Nix) packages(over 80,000 packages) and [NixOS](https://nixos.wiki/wiki/NixOS) modules. The repository is [hosted on GitHub](https://github.com/nixos/nixpkgs) and maintained by the community, with official backing from the [NixOS Foundation](https://nixos.org/). Additionally, checkout [Language-specific package helpers](https://nixos.wiki/wiki/Language-specific_package_helpers) and [Alternative Package Sets](https://nixos.wiki/wiki/Alternative_Package_Sets).

[NixOS Packages Search](https://search.nixos.org/packages) is a tool for searching through NixOS packages.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/173939766-8972583c-855e-4a9b-b9f1-761b60ea255e.png">
  <br />
  NixOS Packages Search
</p>

[Nix Software Center](https://github.com/vlinkz/nix-software-center) is a simple gtk4/libadwaita software center to easily install and manage nix packages.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/211189056-cd719480-ce81-466f-9c8d-562b7296db01.png">
  <br />
  NixOS Software Center
</p>

[FlakeHub](https://flakehub.com/new) is a platform developed by [Determinate Systems](https://determinate.systems/) for discovering and publishing [Nix flakes](https://zero-to-nix.com/concepts/flakes). [FlakeHub](https://determinate.systems/posts/introducing-flakehub) provides the Nix ecosystem with a variety of new capabilities:

   * The ability to explore the Nix flake landscape.
   * Semantic versioning for flakes, including version modifiers like **~ (flexible patch)** and **= (exact match)**.
   * Automated flake publishing with GitHub Actions.

<p align="center">
 <img src="https://github.com/mikeroyal/NixOS-Guide/assets/45159366/b2b7526d-2192-4ee0-990c-d9733c3a9a20">
</br>
FlakeHub
</p>

[Determinate Nix Installer](https://github.com/DeterminateSystems/nix-installer) is an opinionated alternative to the official [Nix install scripts](https://nixos.org/download.html).

**The nix-installer tool is ready to use in a number of environments:**

|Platform |	Multi User |	root only |	Maturity|
|------|------|-------|------|
|Linux (x86_64 & aarch64) |✓ (via [systemd](https://systemd.io/)) |	✓ |	Stable|
|MacOS (x86_64 & aarch64) |	✓ |		|Stable (See note)|
|Valve Steam Deck (SteamOS)| 	✓ |		|Stable|
|WSL2 (x86_64 & aarch64) |	✓ (via [systemd](https://systemd.io/)) |	✓ |	Stable|
Podman Linux Containers |	✓ (via [systemd](https://systemd.io/)) |	✓ |	Stable|
|Docker Containers 	|	|✓ |	Stable|
|Linux (i686) |	✓ (via [systemd](https://systemd.io/)) |	✓ 	|Unstable|

## NixOS Developer Resources
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [NixOS Wiki](https://nixos.wiki/)

 - [NixOS Pills - Developer Guides](https://nixos.org/guides/nix-pills/)
 
 - [NixOS Learn](https://nixos.org/learn.html)

 - [Nix Package Manager Manual](https://nixos.org/manual/nix/stable/#chap-installation)

 - [Home Manager - NixOS Wiki](https://nixos.wiki/wiki/Home_Manager)
 
 - [What Is Nix — Developer Tooling | Shopify Engineering](https://shopify.engineering/what-is-nix)
 
 - [NixOS configurations collection](https://nixos.wiki/wiki/Configuration_Collection)
 
 - [Install and Configure NixOS on a Linode](https://www.linode.com/docs/guides/install-nixos-on-linode/)
 
 - [Zero to Nix from Determinate Systems](https://zero-to-nix.com/start/install)

 - [Cheatsheet - NixOS Wiki](https://nixos.wiki/index.php?title=Cheatsheet&useskin=vector)
 
 - [nix.dev guide for developers](https://nix.dev/)
 
 - [Hound - search across all/selected Nix-related repositories.](https://search.nix.gsc.io) 
 
 - [Nix(A One Pager) - A one page introduction to Nix, the language](https://github.com/tazjin/nix-1p) 
 
 - [Nix Shorts](https://github.com/justinwoo/nix-shorts/)
 
 - [How to Learn Nix tutorials by Ian Henry](https://ianthehenry.com/posts/how-to-learn-nix/)

 - [Getting started with Home Manager for Nix](https://ghedam.at/24353/tutorial-getting-started-with-home-manager-for-nix)

 - [NixOS Wiki - Raspberry Pi 4](https://nixos.wiki/wiki/NixOS_on_ARM/Raspberry_Pi_4)

 - [NixOS aarm64 SD image](https://hydra.nixos.org/job/nixos/trunk-combined/nixos.sd_image.aarch64-linux)

 - [nixery.dev](https://nixery.dev/)
 
 - [NixOS Discourse Forum](https://discourse.nixos.org/)
 
 - [NixCon- annual community conference](https://nixcon.org/)

 - [NixOS Community](https://nixos.org/community.html)

 - [NixOS Governance](https://nixos.org/governance.html)

 - [Consider Donating to the NixoS Project](https://nixos.org/donate.html)

### YouTube Tutorials

[Back to the Top](#table-of-contents)

[![NixOS is Mindblowing](https://ytcards.demolab.com/?id=fuWPuJZ9NcU&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "NixOS is Mindblowing")](https://www.youtube.com/watch?v=fuWPuJZ9NcU)
[![NixOS Is The Power User Distro (Now With An Easy Installer!)](https://ytcards.demolab.com/?id=ck4J2Faa7Fc&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "NixOS Is The Power User Distro (Now With An Easy Installer!)")](https://www.youtube.com/watch?v=ck4J2Faa7Fc) 
[![NixOS Setup Guide - Configuration / Home-Manager / Flakes](https://ytcards.demolab.com/?id=AGVXJ-TIv3Y&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "NixOS Setup Guide - Configuration / Home-Manager / Flakes")](https://www.youtube.com/watch?v=AGVXJ-TIv3Y)
[![NixOS Intro - Installation and basic usage](https://ytcards.demolab.com/?id=9fWrxmEYGAs&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "NixOS Intro - Installation and basic usage")](https://www.youtube.com/watch?v=9fWrxmEYGAs)
[![Nixpkgs - Python packaging, and development workflow.](https://ytcards.demolab.com/?id=jXd-hkP4xnU&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "Nixpkgs - Python packaging, and development workflow.")](https://www.youtube.com/watch?v=jXd-hkP4xnU)
[![NixOS: How it works and how to install it!](https://ytcards.demolab.com/?id=oPymb2-IXbg&lang=en&background_color=%230d1117&title_color=%23ffffff&stats_color=%23dedede&width=240 "NixOS: How it works and how to install it!")](https://www.youtube.com/watch?v=oPymb2-IXbg)  

## NixOS Tools and Modules
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Hydra](https://github.com/nixos/hydra) is Nix's official continuous integration and build system.

 - [Kubenix](https://github.com/xtruder/kubenix) is a Kubernetes resource builder written in Nix.

 - [Nix-kubernetes](https://github.com/xtruder/nix-kubernetes) is a Kubernetes deployment manager written in nix.

 - [Disnix](https://github.com/svanderburg/disnix) is a microservice architecture built with Nix.

 - [Hail](https://github.com/TaktInc/hail) is a service for pull-based continuous deployment.

 - [Morph](https://github.com/DBCDK/morph) is a NixOS deployment tool.

 - [Nixery](https://nixery.dev/) is a ad-hoc container images from Nix.

 - [Home Manager](https://github.com/nix-community/home-manager) is a tool to manage your user configuration just like NixOS.s.

 - [NixVim](https://github.com/pta2002/nixvim) is a NeoVim distribution built with Nix modules and Nixpkgs.

 - [Simple Nixos Mailserver](https://gitlab.com/simple-nixos-mailserver/nixos-mailserver) is a complete mailserver, managed with NixOS modules.
   
 - [NixOS Anywhere](https://numtide.github.io/nixos-anywhere/) is a tool that let's you install NixoS everywhere via ssh on a target machine running x86_64 Linux with [kexec](https://man7.org/linux/man-pages/man8/kexec.8.html) support. 

 - [Stylix](https://github.com/danth/stylix) is a system-wide colorscheming and typography for NixOS.

 - [Awesome-Nix-HPC](https://github.com/freuk/awesome-nix-hpc) is a High Performance Computing package sets.

 - [Nix-darwin](https://github.com/LnL7/nix-darwin) is a tool to manage macOS configuration just like on NixOS.

 - [Nixpkgs-firefox-darwin](https://github.com/bandithedoge/nixpkgs-firefox-darwin) is a nikpkg to automatically updated Firefox binary packages for macOS.

 - [Nixpkgs-wayland](https://github.com/nix-community/nixpkgs-wayland) is a bleeding-edge Wayland packages.

 - [NUR(Nix User Repositories)](https://github.com/nix-community/NUR/) is the mother of all overlays, allowing access to user repositories and installing packages via attributes.

 - [Alejandra](https://github.com/kamadorueda/alejandra) is a opinionated Nix code formatter optimized for speed and consistency.

 - [Comma](https://github.com/Shopify/comma) is a tool that quickly runs any binary; wraps together `nix run` and `nix-index`

 - [Colmena](https://github.com/zhaofengli/colmena) is a simple, stateless NixOS deployment tool modeled after NixOps and morph.

 - [Krops](https://cgit.krebsco.de/krops/about/) is a lightweight toolkit to deploy NixOS systems, remotely or locally.

 - [KuberNix](https://github.com/saschagrunert/kubernix) is a single-dependency Kubernetes clusters via Nix packages.

 - [Terraform-nixos](https://github.com/tweag/terraform-nixos) is a set of Terraform modules designed to deploy NixOS.

 - [Terranix](https://terranix.org) is a tool to use Nix and the NixOS module system to write your Terraform code.

 - [Arion](https://github.com/hercules-ci/arion#readme) is a configure Docker Compose with Nix modules.

 - [Deploy-rs](https://github.com/serokell/deploy-rs) is a simple multi-profile Nix-flake deploy tool.

 - [Fractalide](https://github.com/fractalide/fractalide) is a reusable Reproducible Composable Software.

 - [Nixos-shell](https://github.com/Mic92/nixos-shell) is a simple headless VM configuration using Nix (similar to Vagrant).

 - [Pushnix](https://github.com/arnarg/pushnix) is a simple cli utility that pushes NixOS configuration and triggers a rebuild using ssh.

 - [Musnix](https://github.com/musnix/musnix) is a real-time audio modules for NixOS.

 - [Nix-bundle](https://github.com/matthewbauer/nix-bundle) is a package Nix attributes into single-file executables.

 - [Extra-container](https://github.com/erikarvstedt/extra-container) is a run declarative NixOS containers from the command line. Similar to nixos-shell (chrisfarms).

 - [Nixcloud-webservices](https://github.com/nixcloud/nixcloud-webservices) is a set of nixpkgs extension for web-related technologies.

 - [Mach-nix](https://github.com/DavHau/mach-nix) is a tool that makes it easy to create and share reproducible python environments or packages. Existing tools for python package management often suffer from reproducibility and complexity issues, requiring a multitude of tools and additional virtualization layers to work sufficiently. 
 
  - [Digga](https://github.com/divnix/digga) is a flake utility library that helps you declaratively craft and manage all three layers of your system environment within a single nix flakes repository:

    * Development shells (via numtide/devshell).
    * Home environments (via nix-community/home-manager).
    * Host configurations (via NixOS/nixpkgs/nixos).

 - [Impermanence](https://github.com/nix-community/impermanence) is a set of modules to help you handle persistent state on systems with ephemeral root storage.
 
 - [NixOS Vagrant Plugin](https://github.com/nix-community/vagrant-nixos-plugin) is a plugin that adds nix provisioning for [NixOS](https://nixos.org/) guests to [Vagrant](https://www.vagrantup.com/).
 
 - [Fenix](https://github.com/nix-community/fenix) is a Rust toolchains and Rust analyzer nightly for nix.

 - [NixOS-WSL](https://github.com/nix-community/NixOS-WSL) is a minimal root filesystem for running NixOS on WSL. It can be used with DistroLauncher as ```install.tar.gz``` or as input to ```wsl --import --version 2```.

 - [Nix-bitcoin](https://github.com/nixbitcoin/nix-bitcoin/) is a set of NixOS modules to install a bitcoin node with emphasis on security.

 - [Nixpkgs-review](https://github.com/Mic92/nixpkgs-review) is a review nixpkgs pull requests.

 - [Nix-update](https://github.com/Mic92/nix-update) is a swiss army knife for updating nix packages.

 - [Nox](https://github.com/madjar/nox) is a set of tools to make Nix easier to use.

 - [Nix-diff](https://github.com/Gabriel439/nix-diff) is a tool to compare Nix derivations.

 - [Niff](https://github.com/FRidh/niff) is a tool to compare two Nix expressions to determine what attributes changes.

 - [Nix-upgrade-scripts](https://github.com/peterhoeg/nix-upgrade-scripts)  is a set of tools for Nixpkgs maintainers to upgrade packages.

 - [Nixops-manager](https://github.com/grafted-in/nixops-manager) is a NixOps wrapper for Git repositories.

 - [Narfuse](https://github.com/taktoa/narfuse) is a FUSE filesystem for mounting Nix archive (NAR) files as a virtual Nix store.

 - [Nix-visualize](https://github.com/craigmbooth/nix-visualize) is a tool to visualize the dependencies of a given package.

 - [Home-manager](https://github.com/rycee/home-manager) is a system for managing a user environment using Nix.

 - [NixGl](https://github.com/guibou/nixGL) is a wrapper to run OpenGL applications outside of NixOS.

 - [Nixfmt](https://github.com/serokell/nixfmt) is a formatter for Nix code.

 - [Nix-index](https://github.com/bennofs/nix-index) is a tool that quickly locate Nix packages with specific files.

 - [Nix-prefetch](https://github.com/msteen/nix-prefetch) is a universal tool for updating source checksums.

 - [Nix-tree](https://github.com/utdemir/nix-tree) is a tool that let's you interactively browse the dependency graph of Nix derivations.

 - [Statix](https://github.com/nerdypepper/statix) is a linter/fixer to check for and fix antipatterns in Nix code.

 - [Cached-nix-shell](https://github.com/xzfc/cached-nix-shell) is a `nix-shell` replacement that uses caching to open subsequent shells quickly.

 - [Cachix](https://cachix.org/) is a hosted binary cache service; free for open-source projects.

 - [Devshell](https://github.com/numtide/devshell) is a `mkShell` with extra bits and a toml config option to be able to onboard non-nix users.

 - [Flake-utils](https://github.com/numtide/flake-utils) - Pure Nix flake utility functions to help with writing flakes.

 - [Gitignore.nix](https://github.com/hercules-ci/gitignore.nix) - The most feature-complete and easy-to-use `.gitignore` integration.

 - [Lorri](https://github.com/target/lorri/) is a much better `nix-shell` for development that augments direnv.

 - [Makes](https://github.com/fluidattacks/makes) is a Nix-based CI/CD pipeline framework for building, testing, and releasing projects in any language, from anywhere. 

 - [Niv](https://github.com/nmattia/niv/) is a easy dependency management for Nix projects with package pinning.

 - [Nix-direnv](https://github.com/nix-community/nix-direnv) is a fast loader and flake-compliant configuration for the direnv environment auto-loader.

 - [Nixpkgs-review](https://github.com/Mic92/nixpkgs-review) is the best tool to verify that a pull-request in Nixpkgs is building properly.

 - [Pre-commit-hooks.nix](https://github.com/cachix/pre-commit-hooks.nix) is a tool to run linters/formatters at commit time and on your CI.

 - [Robotnix](https://github.com/danielfullmer/robotnix) is a declarative and reproducible build system for Android (AOSP) images.

 - [Nixpkgs-hammering](https://github.com/jtojnar/nixpkgs-hammering) is a nixpkg to beat your package expressions into a shape.

 - [Nix-alien](https://github.com/thiagokokada/nix-alien) is a tool to run unpatched binaries on Nix/NixOS easily.
 
 - [Disko](https://github.com/nix-community/disko) is a declarative disk partitioning tool using Nix. 
 
 - [NixOS on WSL](https://github.com/nix-community/NixOS-WSL) is a minimal root filesystem for running NixOS on WSL. It can be used with DistroLauncher as ```install.tar.gz``` or as input to ```wsl --import --version 2```.
 
 - [Appvm](https://github.com/jollheef/appvm) is a simple application VMs (hypervisor-based sandbox) based on Nix package manager. It uses one read-only /nix directory for all appvms. So creating a new appvm (but not first) is just about one minute.

 - [Deadnix](https://github.com/astro/deadnix) is a tool that scan ```.nix``` files for dead code (unused variable bindings).

 - [nix2container](https://github.com/nlewo/nix2container) isa tool that provides an efficient container development workflow with images built by Nix: it doesn't write tarballs to the Nix store and allows to skip already pushed layers (without having to rebuild them).
   
 - [nixos-mailserver](https://gitlab.com/simple-nixos-mailserver/nixos-mailserver) is a complete and Simple Nixos Mailserver.

## NixOS Desktop
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Etcher](https://www.balena.io/etcher/) is an open source, cross-platform software that makes it easy to flash operating system images to a microSD card or USB device.

 - [nixos-generators](https://github.com/nix-community/nixos-generators) is a NixOS config and build multiple different images types including VirtualBox VMs, Azure images, and installation ISOs.
 
 - [nixos-up](https://github.com/samuela/nixos-up) is a super easy NixOS installer that can be used from the installation ISO.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/173939768-31847173-88ab-45f0-8501-0980d1a2a29e.png">
  <br />
  NixOS Desktop with the new Calamares Installer
</p>

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/128645111-b2a92dd2-f246-4df0-b05c-5b0ffce05448.png">
  <br />
  NixOS with the Plasma Desktop
</p>

## Programming Languages with NixOS support
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)
    
###  C
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

  - [C - NixOS Wiki](https://nixos.wiki/wiki/C)
 
  - [ccls](https://github.com/MaskRay/ccls)  is a C/C++/Objective-C language server.
   
### Python
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Python - NixOS Wiki](https://nixos.wiki/wiki/Python)

 - [Mach-nix](https://github.com/DavHau/mach-nix) is a tool to create highly reproducible python environments.
 
 - [Poetry2nix](https://github.com/nix-community/poetry2nix) is a tool to build Python packages directly from [Poetry's](https://python-poetry.org/) `poetry.lock`. No conversion step needed.
 
 - [Pypi2nix](https://github.com/nix-community/pypi2nix)  is a tool to generate Nix expressions for Python packages.

### Ruby
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Ruby - NixOS Wiki](https://nixos.wiki/wiki/Ruby)

 - [Bundix](https://github.com/nix-community/bundix) is a tool that generates a Nix expression for your Bundler-managed application.
 
### Go
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Go - NixOS Wiki](https://nixos.wiki/wiki/Go)
 
 - [Gomod2nix](https://github.com/tweag/gomod2nix) is a tool to convert applications using Go modules to Nix expressions.
 
 - [Dep2nix](https://github.com/nixcloud/dep2nix) is a tool using golang/dep to create a deps.nix file for go projects to package them for nixpkgs. 
 
 - [Vgo2nix](https://github.com/nix-community/vgo2nix) is a tool to Convert go.mod files to nixpkgs buildGoPackage compatible deps.nix files.

### Rust
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)
 
 - [Rust - NixOS Wiki](https://nixos.wiki/wiki/Rust)

 - [Fenix](https://github.com/nix-community/fenix) is a Rust toolchains and Rust analyzer nightly for nix.
 
 - [Naersk](https://github.com/nmattia/naersk) is a build to Rust packages directly from `Cargo.lock`. No conversion step needed.
 
 - [Nix-cargo-integration](https://github.com/yusdacra/nix-cargo-integration) is a library that allows easy and effortless integration for Cargo projects.
 
 - [Nixpkgs-mozilla](https://github.com/mozilla/nixpkgs-mozilla) is  Mozilla's overlay with Rust toolchains and Firefox.
 
 - [Rust-nix-templater](https://github.com/yusdacra/rust-nix-templater) is a tool that generates Nix build and development files for Rust projects.
 
 - [Rust-overlay](https://github.com/oxalica/rust-overlay) is a pure and reproducible nix overlay of binary distributed Rust toolchains.

### Scala
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Sbtix](https://gitlab.com/teozkr/Sbtix) isa tool that generates a Nix definition that represents your SBT project's dependencies. It then uses this to build a Maven repo containing the stuff your project needs, and feeds it back to your SBT build.
 
 - [Sbt-derivation](https://github.com/zaninime/sbt-derivation) is a mkDerivation for sbt, similar to buildGoModule.
 
 - [Sbt-nix.g8](https://github.com/gvolpe/sbt-nix.g8) is a [giter8](https://github.com/foundweekends/giter8) template for new Scala projects with Nix support.

### Clojure
 [Back to the Top](#table-of-contents)
 
 - [Clojure Packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=clojure)
  
 - [Clj-nix](https://github.com/jlesquembre/clj-nix) is Nix helpers for Clojure projects.
 
 - [Clj2nix](https://github.com/hlolli/clj2nix) is a tool that converts deps.edn to a nix expression.
 
 - [Clojure-nix-locker](https://github.com/bevuta/clojure-nix-locker) is a simple and flexible tool to build clojure projects with Nix.
 
### Haskell
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)
 
 - [Haskell - NixOS Wiki](https://nixos.wiki/wiki/Haskell)
 
 - [Cabal2nix](https://github.com/NixOS/cabal2nix) is a tool that converts a Cabal file into a Nix build expression.
 
 - [Haskell.nix](https://github.com/input-output-hk/haskell.nix) is an alternative Haskell Infrastructure for Nixpkgs.
 
 - [Nix-haskell-mode](https://github.com/matthewbauer/nix-haskell-mode) is an automatic Haskell setup in Emacs.
 
 - [Nixkell](https://github.com/pwm/nixkell) is a Haskell project template using Nix and direnv.
 
 - [Stack2nix](https://github.com/input-output-hk/stack2nix) is a tool to generate nix expressions for Haskell projects.

### Node.js
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Node.js - NixOS Wiki](https://nixos.wiki/wiki/Node.js)
 
 - [Napalm](https://github.com/nmattia/napalm) - Support for building npm packages in Nix with a lightweight npm registry.
 
 - [Node2nix](https://github.com/svanderburg/node2nix) - Generate Nix expression from a `package.json` (or `package-lock.json`) (to be stored as files).
 
 - [Npmlock2nix](https://github.com/tweag/npmlock2nix) - Generate Nix expressions from a `package-lock.json` (in-memory), primarily for web projects.
 
 - [Yarn2nix](https://github.com/nix-community/yarn2nix) - Generate Nix expressions from a `yarn.lock` file.

### PHP
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)
 
 - [PHP - NixOS Wiki](https://nixos.wiki/wiki/PHP)
 
 - [Composer2nix](https://github.com/svanderburg/composer2nix) is a tool to generate Nix expressions to build composer packages.
 
 - [Composer-plugin-nixify](https://github.com/stephank/composer-plugin-nixify) is a composer plugin to help with Nix packaging.
 
 - [Composition-c4](https://github.com/fossar/composition-c4) is support for building composer packages from a `composer.lock` (using IFD).
 
 - [Nix-phps](https://github.com/fossar/nix-phps) is a  Flake containing old and unmaintained PHP versions (intended for CI use).
 
 - [Nix-shell](https://github.com/loophp/nix-shell/) is a Nix shells for PHP development.
 
### Perl
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Perl- NixOS Wiki](https://nixos.wiki/wiki/Perl)
 
 - [Perl packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=perl)
 
### Java
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Java - NixOS Wiki](https://nixos.wiki/wiki/Java)
 
 - [Java Packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=java)
 
  - [mvn2nix](https://github.com/fzakaria/mvn2nix) is a tool to easily package your Maven Java application with the Nix package manager.
 
### Lua
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Lua - NixOS Wiki](https://nixos.wiki/wiki/Lua)
 
 - [Lua packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=lua)
 
### LLVM
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [LLVM - NixOS Wiki](https://nixos.wiki/wiki/LLVM)
 
 - [LLVM packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=llvm)
 
### Julia
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Julia - NixOS Wiki](https://nixos.wiki/wiki/Julia)
 
 - [Julia packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=julia)
 
### R 
 [Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)
 
 - [R - NixOS Wiki](https://nixos.org/manual/nixpkgs/stable/#r)
 
 - [R packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=r)
 
### Arduino
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [nixduino](https://github.com/boredom101/nixduino) is a Nix-based tool to help build Arduino sketches.
 
 - [Arduino packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=Arduino)

### Crystal
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [crystal2nix](https://github.com/nix-community/crystal2nix) is a tool to convert `shard.lock` into Nix expressions.
 
 - [Crystal packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=crystal)
 
### Lisp
[Back to the Top](#table-of-contents)

 - [Lisp packages for NixOS](https://github.com/NixOS/nixpkgs/tree/nixos-22.05/pkgs/development/lisp-modules)

 - [Emacs for NixOS](https://nixos.wiki/wiki/Emacs) is an interactive graphical emacs lisp interpreter that comes with many applications, but is primarily used as a text and code editor. 

 - [Emacs overlay for Nixpkgs](https://github.com/nix-community/emacs-overlay) is a bleeding edge emacs overlay for Nixpkgs.

 - [nix-mode](https://github.com/NixOS/nix-mode) is a An Emacs major mode for editing Nix expressions. 


### Nim
[Back to the Top](#table-of-contents)

 - [Nim](https://nim-lang.org/) is a statically typed compiled systems programming language. It combines successful concepts from mature languages like Python, Ada and Modula. 

 - [Nim packages for NixOS](https://github.com/NixOS/nixpkgs/tree/nixos-22.05/pkgs/development/nim-packages)

 - [Nim Language Server](https://github.com/nim-lang/langserver) is a Language Server, or nimlangserver, is a language server for Nim.

### Elm
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [elm2nix](https://github.com/hercules-ci/elm2nix) is a tool to convert `elm.json` into Nix expressions.
 
 - [Elm packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=elm)

### Elixir
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [BEAM Languages (Erlang, Elixir & LFE)](https://nixos.org/manual/nixpkgs/stable/#how-to-install-beam-packages)
 
 - [Elixir packages for NixOS](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=elixir)

### Erlang
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [BEAM Languages (Erlang, Elixir & LFE)](https://nixos.org/manual/nixpkgs/stable/#how-to-install-beam-packages)

 - [NixOS packages for Erlang](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=erlang)
 
 ### DotNet
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [ DotNet - NixOS Wiki](https://nixos.wiki/wiki/DotNET)
 
 - [NixOS packages for DotNet](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=dotnet)

### CUDA
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [CUDA - NixOS Wiki](https://nixos.wiki/wiki/CUDA)
 
 - [NixOS packages for CUDA](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=cuda)

### Qt
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

 - [Qt - NixOS Wiki](https://nixos.wiki/wiki/Qt)
 
 - [NixOS packages for Qt](https://search.nixos.org/packages?channel=22.05&from=0&size=50&sort=relevance&type=packages&query=qt)
 

# Getting Software
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Nixpkgs](https://nixos.wiki/wiki/Nixpkgs) is the largest repository of [Nix](https://nixos.wiki/wiki/Nix) packages(over 80,000 packages) and [NixOS](https://nixos.wiki/wiki/NixOS) modules. The repository is [hosted on GitHub](https://github.com/nixos/nixpkgs) and maintained by the community, with official backing from the [NixOS Foundation](https://nixos.org/). Additionally, checkout [Language-specific package helpers](https://nixos.wiki/wiki/Language-specific_package_helpers) and [Alternative Package Sets](https://nixos.wiki/wiki/Alternative_Package_Sets).

[NixOS Packages Search](https://search.nixos.org/packages) is a tool for searching through NixOS packages.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/173939766-8972583c-855e-4a9b-b9f1-761b60ea255e.png">
  <br />
  NixOS Packages Search
</p>

[NUR(Nix User Repositories)](https://github.com/nix-community/NUR/) is the mother of all overlays, allowing access to user repositories and installing packages via attributes.

[NixOS-GUI](https://github.com/Celestialme/Nixos-Gui) is a GUI for Nixos package manager. It is developed and maintained by [Celestialme](https://github.com/Celestialme/).

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/175184677-c985b399-da35-4139-8ac2-1a8c3b0f254a.png">
  <br />
  NixOS GUI tool
</p>

**Using Flatpaks on NixOS makes installing/updating applications a lot easier especially if some software is proprietary.**

## Flatpaks

**[Setting up Flatpak on NixOS](https://www.flatpak.org/setup/NixOS)**

[FlatHub](https://flathub.org/) is a build and distribution service for Flatpak applications.

[FlatHub Forum](https://discourse.flathub.org/)

 <img src="https://github.com/mikeroyal/NixOS-Guide/assets/45159366/3dbf5f71-91c3-4e64-9ad0-eba5b88b4b60">

## AppImages

[AppImageKit](https://search.nixos.org/packages?channel=22.05&show=appimagekit&from=0&size=50&sort=relevance&type=packages&query=appimage) is an implementation of the AppImage format that provides tools such as appimagetool and appimaged for handling AppImages. 

```$ nix-env -iA nixos.appimagekit```

[AppImageHub](https://www.appimagehub.com) is a build and distribution service for AppImage applications.

[AppImage Manager](https://github.com/AppImageCrafters/appimage-manager) is a package manager for AppImages.

[AppImage Forum](https://discourse.appimage.org/)

 <img src="https://user-images.githubusercontent.com/45159366/106686382-0b505c80-657f-11eb-9d74-9a94ec0d0693.png">


# Gaming

[Back to the Top](https://github.com/mikeroyal/NixOS-Guide/blob/main/README.md#table-of-contents)

**[NixOS Gaming config by fufexan on GitHub ](https://github.com/fufexan/nix-gaming)**

I recommend using Flatpaks on NixOS, which makes installing/updating applications a lot easier especially if some software is proprietary.

**[Setting up Flatpak on NixOS](https://www.flatpak.org/setup/NixOS)**

## Steam
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Steam - NixOS Wiki](https://nixos.wiki/wiki/Steam)

[Steam Flatpak](https://flathub.org/apps/details/com.valvesoftware.Steam) available on FlatHub.

[Steam Remote Play Together](https://store.steampowered.com/remoteplay/#together) is a steam service that let's you share your Steam local multi-player games with friends over the internet, for free. Using Remote Play Together, one player owns and runs the game, then up to four players can join.

[Proton](https://github.com/ValveSoftware/Proton/) is a tool for use with the Steam client which allows games which are exclusive to Windows to run on the Linux operating system. It uses Wine to facilitate this.

[ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt) is a tool to install and manage [Proton-GE](https://github.com/GloriousEggroll/proton-ge-custom) and [Luxtorpeda](https://github.com/luxtorpeda-dev/luxtorpeda) for Steam and [Wine-GE](https://github.com/GloriousEggroll/wine-ge-custom) for Lutris with this graphical user interface. Based on AUNaseef's [ProtonUp](https://github.com/AUNaseef/protonup), made with Python 3 and Qt 6. **[Flatpak version](https://flathub.org/apps/details/net.davidotek.pupgui2)**

## Enable Proton in Steam

 - Click on “Steam” then “Settings” to open the Settings window at the far-left corner.
 - On the “Settings” window, click on “Steam Play.” Ensure you check the “Enable Steam Play for supported files” and “Enable Steam Play for   all other titles” checkboxes. Lastly, select the Proton version you wish to use from the drop-down menu.

 <img src="https://user-images.githubusercontent.com/45159366/106686402-13100100-657f-11eb-9012-6bdac264a808.png">

## ProtonDB
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[ProtonDB](https://www.protondb.com) is a collection of over 100,000 gaming reports from other gamers as they test games with Proton on Linux and provide aggregate scores of how well games perform. A growing pool of suggestions provides tweaks that you can try to get games working while Proton continues development. In addition to this, you may explore the Steam game catalog on this site to browse and discover a wide range of titles that were previously unavailable for use on Linux.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108773213-dcd8f800-7512-11eb-8775-19b0c8924d55.png">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108773214-dd718e80-7512-11eb-983b-ce192e5b30f2.png">
</p>

## Lutris
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Lutris](https://github.com/lutris/lutris/releases) is a gaming client for Linux. It gives you access to all your video games with the exception of the current console generation. Also, integrates nicely with other stores like GOG, Steam, Battle.net, Origin, Uplay and many other sources that allow you to import your existing game library and community maintained install scripts give you a completely automated setup.

[Add Epic Games Store](https://lutris.net/games/epic-games-store/)

 <img src="https://user-images.githubusercontent.com/45159366/106686406-14412e00-657f-11eb-97c4-c80c6e25a374.png">

## GameHub
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[GameHub](hhttps://github.com/tkashkin/GameHub/releases) is a unified library for all your games. It allows you to store your games from different platforms into one program to make it easier for you to manage your games.

<img src="https://user-images.githubusercontent.com/45159366/107862734-96451880-6e03-11eb-9b92-9d355b890083.png">

**GameHub supports:**

 - native games for Linux
 - **multiple compatibility layers:**
   - Wine
   - Proton
   - [DOSBox](https://www.dosbox.com/)
   - [RetroArch](https://store.steampowered.com/app/1118310/RetroArch/)
   - [ScummVM](https://www.scummvm.org/)
   - [WineWrap](https://www.gog.com/forum/general/adamhms_linux_wine_wrappers_news_faq_discussion/post1) — a set of preconfigured wrappers for [supported games](https://www.gog.com/forum/general/adamhms_linux_wine_wrappers_news_faq_discussion/post3);
   - custom emulators

 - **multiple game platforms:**
   - [Steam](https://store.steampowered.com/)
   - [GOG](https://www.gog.com/)
   - [Humble Bundle (including Humble Trove)](https://www.humblebundle.com/)
   - [itch.io](https://itch.io/)


## Epic Games Store
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Heroic](https://heroicgameslauncher.com/) is an Open Source Game Launcher for Linux, Windows and macOS (for both Native and Windows Games using Crossover). It supports launching games from the Epic Games Store using Legendary, a CLI alternative to the Epic Games Launcher. [Flatpak for Heroic Games Launcher](https://flathub.org/apps/details/com.heroicgameslauncher.hgl)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/111918016-3fed7a00-8a40-11eb-964e-930c801c1c72.png">
</p>

## Game Streaming
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Geforce NOW](https://www.nvidia.com/en-us/geforce-now/download/) is NVIDIA's Cloud Gaming Service.

 <img src="https://user-images.githubusercontent.com/45159366/106686391-0f7c7a00-657f-11eb-9d0b-1ebb4d385883.jpeg">

[Moonlight Game Streaming](https://moonlight-stream.org/) is a program that let you stream from your PC games over the Internet with no configuration required. Stream from almost any device, whether you're in another room or miles away from your gaming rig.

<img src="https://user-images.githubusercontent.com/45159366/106686398-11463d80-657f-11eb-841a-d534829ccc3d.png">

[Chiaki](https://git.sr.ht/~thestr4ng3r/chiaki) is a Free and Open Source Software Client for PlayStation 4 and PlayStation 5 Remote Play for Linux, FreeBSD, OpenBSD, Android, macOS, Windows, Nintendo Switch and potentially even more platforms. [Chiaki Flatpak](https://flathub.org/apps/details/re.chiaki.Chiaki)

[Xbox Cloud Gaming](https://www.xbox.com/en-US/xbox-game-pass/cloud-gaming) is Microsoft's cloud-based Xbox game-streaming technology **(currently in Beta)**. **Play games like Forza Horizon 4, Halo 5: Guardians, Gears of War 4, Sea of Thieves, Cuphead, Red Dead Redemption 2, and 100+ other games on your mobile device or Chrome web browser**. Xbox Cloud Gaming does require an [Xbox Game Pass Ultimate](https://www.xbox.com/en-US/xbox-game-pass/cloud-gaming) subscription.

<img src="https://user-images.githubusercontent.com/45159366/108111388-74d56e00-7049-11eb-8aeb-3e5d65f9e832.png">

[Stadia](https://stadia.google.com/games) is Google's gaming platform that lets you instantly play your favorite video games on screens you already own. Game on TVs with Chromecast with Google TV, laptops, desktops, tablets or compatible phones. [Stadia Pro](https://stadia.google.com/) is a subscription($9.99 per month) that unlocks a growing collection of free games to play on Stadia. 

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/162089471-3eb27f98-2366-4117-9af5-93bb126a2c37.png">
</p>

[Parsec](https://parsec.app/cloud-gaming) is a video game streaming platform, which offers a wide variety of games and genres to choose from and provides a high-quality and smooth gameplay. SParsec is developed in order to provide a high-quality smooth gameplay, same time to be free of all ads and in-game purchases.

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/166166858-e70ca081-8931-46f3-9dc3-fe9c719d76f8.png">
</p>

[Amazon Luna](https://www.amazon.com/luna/landing-page) is Amazon's Cloud Gaming Service. Amazon Luna is Compatible/Supported on a vartiey of [Devices and Browsers](https://www.amazon.com/gp/help/customer/display.html?nodeId=GUFHUSX8X324T4XE).

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/112693072-364b8400-8e3d-11eb-9df0-d58af7ac9c9c.png">
</p>

## Game Emulators
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[EmulationStation Desktop Edition (ES-DE)](https://www.es-de.org/) is a frontend application for browsing and launching games from your multi-platform game collection. It's  available for Unix/Linux, macOS(M1 & Intel) and Windows.

[RetroPie](https://retropie.org.uk/) is a frontend for emulators that allows you to turn your Raspberry Pi, ODroid C1/C2, or PC into a retro-gaming machine. It builds upon Raspbian, [EmulationStation](https://github.com/Aloshi/EmulationStation), RetroArch and many other projects to enable you to play your favourite Arcade, home-console, and classic PC games with the minimum set-up.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/153087555-e1bde100-6079-4089-a33d-804e29064789.png">
<br />
</p>

[RetroArch](https://www.retroarch.com/) is a frontend for emulators, game engines and media players. It enables you to run classic games on a wide range of computers and consoles through its slick graphical interface. Settings are also unified so configuration is done once and for all. [RetroArch Flatpak](https://flathub.org/apps/details/org.libretro.RetroArch)

[Cartridge](https://github.com/unclebacon-live/cartridge) is a self-hosted game library made with Laravel + Vue.js.

**Cartridge Features**

   - Scan for ROM files and match with IGDB game information
   - Serve ROM download links alongside game details
   - Manage access to library with user creation and permissions (WIP)
   - Allow users to request games (Planned)
   - Play select ROMs in-browser using JS emulators (Planned)
   - Track played and favorite games (even ones that aren't available for download) (Planned)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/172274231-d691a850-1879-44fb-8fa0-08e549d7bb29.png">
<br />
 Cartridge UI
</p>

[Dolphin](https://dolphin-emu.org) is an emulator for two recent Nintendo video game consoles: the GameCube and the Wii. It allows PC gamers to enjoy games for these two consoles in full HD (1080p) with several enhancements: compatibility with all PC controllers, turbo speed, networked multiplayer, and even more. [Dolphin Flatpak](https://flathub.org/apps/details/org.DolphinEmu.dolphin-emu)

[Citra](https://citra-emu.org/) is an open-source emulator for the Nintendo 3DS capable of playing many of your favorite games. [Citra Flatpak](https://flathub.org/apps/details/org.citra_emu.citra)

[yuzu](https://yuzu-emu.org) is an experimental open-source emulator for the Nintendo Switch from the creators of Citra.[Yuzu Flatpak](https://flathub.org/apps/details/org.yuzu_emu.yuzu)

[m64p](https://m64p.github.io/) is a Nintendo 64 Emulator. It uses mupen64plus-gui, a brand new mupen64plus frontend written in Qt5. It supports all of the things you’d expect from a frontend (savestate management, pausing, screenshots). [m64p Flatpak](https://flathub.org/apps/details/io.github.m64p.m64p)

[DeSmuME](https://desmume.org/) is a Nintendo DS emulator. [DeSmuME Flatpak](https://flathub.org/apps/details/org.desmume.DeSmuME)

[Snes9x](https://www.snes9x.com/) is a portable, freeware Super Nintendo Entertainment System (SNES) emulator. [Snes9x Flatpak](https://flathub.org/apps/details/com.snes9x.Snes9x) 

[bsnes](https://github.com/bsnes-emu/bsnes) is a Super Nintendo (SNES) emulator focused on performance, features, and ease of use. [bsnes flatpak](https://flathub.org/apps/details/dev.bsnes.bsnes)

[mGBA](https://mgba.io/) is a new emulator for running Game Boy Advance games. It aims to be faster and more accurate than many existing Game Boy Advance emulators, as well as adding features that other emulators lack. [mGBA Flatpak](https://flathub.org/apps/details/io.mgba.mGBA)

[DOSBox](https://www.dosbox.com/) is an open-source DOS emulator which primarily focuses on running DOS Games.

[DOSBox Staging](https://github.com/dosbox-staging/dosbox-staging) is a full x86 CPU emulator (independent of host architecture), capable of running DOS programs that require real or protected mode. [DOSBox Staging Flatpak](https://flathub.org/apps/details/io.github.dosbox-staging)

[Flycast](https://github.com/flyinghead/flycast) is a multi-platform Sega Dreamcast, Naomi and Atomiswave emulator derived from reicast. [Flycast Flatpak](https://flathub.org/apps/details/org.flycast.Flycast)

[PCSX2](https://pcsx2.net/) is a PlayStation 2 'emulator', a free program that tries to replicate the PlayStation 2 console to enable you to play PS2 games on your PC. [PCSX2 Flatpak](https://flathub.org/apps/details/net.pcsx2.PCSX2)

[RPCS3](https://rpcs3.net/) is an experimental open-source Sony PlayStation 3 emulator and debugger written in C++ for Windows and Linux. RPCS3 started development in May of 2011 by its founders DH and Hykem. The emulator is currently capable of running over 1800 commercial titles powered by Vulkan and OpenGL. [RPCS3 Flatpak](https://flathub.org/apps/details/net.rpcs3.RPCS3)

[MAME](https://www.mamedev.org/) is a Arcade Machine Emulator.

[xemu](https://xemu.app/) is an original Xbox emulator.

[Xenia](https://github.com/xenia-project/xenia) is an Xbox 360 Emulator.

**Also checkout these subreddits for more great Game Emulators recommendations**
  
   - [r/emulation](https://www.reddit.com/r/emulation/)
   - [r/emulations](https://www.reddit.com/r/emulators/)
   - [r/RetroArch](https://www.reddit.com/r/RetroArch/)
   - [r/RetroPie](https://www.reddit.com/r/RetroPie/)
   - [r/DolphinEmulator](https://www.reddit.com/r/DolphinEmulator/)
   - [r/Citra](https://www.reddit.com/r/Citra/)
   - [r/cemu](https://www.reddit.com/r/cemu/)
   - [r/yuzu](https://www.reddit.com/r/yuzu/)
   - [r/OpenEmu](https://www.reddit.com/r/OpenEmu/)
   - [r/MAME](https://www.reddit.com/r/MAME/)
   - [r/EmuDev](https://www.reddit.com/r/EmuDev/)
   - [r/Roms](https://www.reddit.com/r/Roms/)


## Graphics Performance
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[GreenWithEnvy (GWE)](https://gitlab.com/leinardi/gwe) is a GTK system utility designed by Roberto Leinardi to provide information, control the fans and overclock your NVIDIA video card for better performance. [Flatpak version](https://flathub.org/apps/details/com.leinardi.gwe).

<img src="https://user-images.githubusercontent.com/45159366/107091994-89974380-67b7-11eb-85ed-eedec7e3dfbf.png">

## Wine
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[WINE(Wine Is Not an Emulator)](https://www.winehq.org) is a compatibility layer capable of running Windows applications on several POSIX-compliant operating systems, such as Linux, macOS, & BSD. Instead of simulating internal Windows logic like a virtual machine or emulator, Wine translates Windows API calls into POSIX calls on-the-fly, eliminating the performance and memory penalties of other methods and allowing you to cleanly integrate Windows applications into your desktop.


# Setting up a macOS workspace
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

**REQUIREMENTS**

   - A modern Linux distribution
   - QEMU > 2.11.1
   - A CPU with Intel VT-x / AMD SVM support is required
   - A CPU with SSE4.1 support is required for >= macOS Sierra
   - A CPU with AVX2 support is required for >= macOS Mojave
   - Internet access for the installation process

[Sosumi](https://snapcraft.io/install/sosumi) is a app that let's you download and install macOS in a VM.
 <img src="https://user-images.githubusercontent.com/45159366/107092234-0fb38a00-67b8-11eb-9f30-f4d16545624b.png">

[OpenCore for macOS](https://dortania.github.io/OpenCore-Install-Guide/)

 <img src="https://user-images.githubusercontent.com/45159366/107092246-15a96b00-67b8-11eb-91fb-27494c7f1d4f.jpg">

# Setting up a Windows 10 workspace
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

**REQUIREMENTS**

   - A modern Linux distribution
   - QEMU > 2.11.1
   - A CPU with Intel VT-x / AMD SVM support is required
   - [WindowsGuestDrivers/Download Drivers - KVM](https://www.linux-kvm.org/page/WindowsGuestDrivers/Download_Drivers)
   - Internet access for the installation process


[GNOME Boxes](https://wiki.gnome.org/Apps/Boxes) is an application that gives you access to virtual machines, running locally or remotely. It also allows you to connect to the display of a remote computer.

 <img src="https://user-images.githubusercontent.com/45159366/107092256-1cd07900-67b8-11eb-9ae9-f389045dad26.png">
 <img src="https://user-images.githubusercontent.com/45159366/107093639-72a62080-67ba-11eb-8d88-477929a5516b.png">

 [OpenCore for Windows 10](https://dortania.github.io/OpenCore-Install-Guide/)

 <img src="https://user-images.githubusercontent.com/45159366/107092270-222dc380-67b8-11eb-82cc-d41e9e8a39e0.png">

# Using Android and Android Apps on Linux
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

[Android Studio](https://developer.android.com/studio/) is the development suite for Google's Android Operating System(OS). It's built on [JetBrains IntelliJ IDEA](https://www.jetbrains.com/idea/) software and designed specifically for Android development. It is available for download on Windows, macOS and Linux.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637349-29530380-743f-11eb-8c61-549064b7d80b.png">
</p>

[Android Virtual Device (AVD)](https://developer.android.com/studio/run/managing-avds) is a configuration in [Android Studio](https://developer.android.com/studio/intro) that defines the characteristics of an Android phone, tablet, Wear OS, Android TV, or Automotive OS device that you want to simulate in the Android Emulator. The [Android Emulator](https://developer.android.com/studio/run/emulator) simulates Android devices on your computer so that you can test your application on a variety of devices and Android API levels without needing to have each physical device.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637365-2c4df400-743f-11eb-8265-c07faab3523f.png">
</p>

[LineageOS](https://lineageos.org/) is a free and open-source operating system for various devices, based on the Android mobile platform.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108647222-f0ca1e80-746c-11eb-8e55-0e9808bb24fc.png">
</p>

[Anbox](https://anbox.io/) is an application that provides a container-based approach to boot a full Android system on a regular GNU/Linux system like Ubuntu, Debian Fedora, and openSUSE.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637384-34a62f00-743f-11eb-9edc-83267a673b38.png">
</p>

[Anbox Cloud](https://anbox-cloud.io/) is the mobile cloud computing platform delivered by Canonical. Run Android in the cloud, at high scale and on any type of hardware.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637983-efcfc780-7441-11eb-80fc-b3d1612593ca.png">
</p>

[Genymotion](https://www.genymotion.com/) is a very fast Android emulator. The program itself is based on VirtualBox and is known for its effectively fast speed and is usefulness for running Android apps on a Windows, Mac and Linux desktop.

**Desktop**

Local virtual devices with high performances.

 - Emulate a wide range of virtual device configurations (Android versions, screen size, hardware capacities, etc.)
 - Simulate multiple scenarios thanks to our full set of hardware sensors (GPS, network, multitouch, etc.)
 - Cross-platform: Windows, Mac and Linux
 - Manipulate easily with ADB
 - $412 per year for employees in a company (BUSINESS). All features, advanced support.
 - $136 per year for freelancers (INDIE). All features, best effort support.
 - [Free](https://www.genymotion.com/download/) for personal use only (learning & entertainment). Limited features, no support.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637388-37a11f80-743f-11eb-9f37-6e22e1172f2d.png">
</p>

[Scrcpy](https://github.com/Genymobile/scrcpy) is an application by Genymotion that provides display and control of Android devices connected on USB (or over TCP/IP). It does not require any root access and works on GNU/Linux, Windows and macOS. The Android device requires at least API 21 (Android 5.0).

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108637389-396ae300-743f-11eb-971a-f5b554033552.jpg">
</p>

# Professional Audio & Video Editing
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/108773208-dba7cb00-7512-11eb-8fd0-2d009dbfc729.png">
</p>


[H.264(AVC)](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC) is a video compression standard based on block-oriented and motion-compensated integer-DCT coding that defines multiple profiles (tools) and levels (max bitrates and resolutions) with support up to 8K.

[H.265(HEVC)](https://en.wikipedia.org/wiki/High_Efficiency_Video_Coding) is a video compression standard that is the successor to H.264(AVC). It offers a 25% to 50% better data compression at the same level of video quality, or improved video quality at the same bit-rate.

[FFmpeg](https://ffmpeg.org) is a leading multimedia framework that can decode, encode, transcode, mux, demux, stream, filter and play pretty much anything that humans and machines have created. It supports the most obscure ancient formats up to the cutting edge ones on multiple platforms such as Windows, macOS, and Linux.

[HandBrake](https://handbrake.fr/) is a tool for transcoding video from almost any format with a selection of widely supported codecs. It is supported on Window, macOS, and Linux.

[Dynamic Adaptive Streaming over HTTP (DASH)](https://developer.mozilla.org/en-US/docs/Web/HTML/DASH_Adaptive_Streaming_for_HTML_5_Video) is an adaptive streaming protocol that allows for a video stream to switch between bit rates on the basis of network performance, in order to keep a video playing.

[OpenMAX™](https://www.khronos.org/openmax/) is a cross-platform API that provides comprehensive streaming media codec and application portability by enabling accelerated multimedia components to be developed, integrated and programmed across multiple operating systems and silicon platforms.

[DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve/) is the world’s only solution that combines professional 8K editing, color correction, visual effects and audio post production all in one software tool! You can instantly move between editing, color, effects, and audio with a single click. DaVinci Resolve Studio is also the only solution designed for multi user collaboration so editors, assistants, colorists, VFX artists and sound designers can all work live on the same project at the same time.

[Blender](https://www.blender.org/features/video-editing/) comes with a built-in video sequence editor allows you to perform basic actions like video cuts and splicing, as well as more complex tasks like video masking or color grading. The Video Editor includes: Live preview, luma waveform, chroma vectorscope and histogram displays. Audio mixing, syncing, scrubbing and waveform visualization.

[Kdenlive](https://kdenlive.org/en/) is an open source video editing tool that supports unlimited multimedia files. It's based on the MLT Framework, KDE and Qt. People who are looking for a very versatile video editing tool that comes packed with features. The latest 20.08 release is out with nifty features like Interface Layouts, Multiple Audio Stream support, Cached data management and Zoombars in the Clip Monitor and Effects Panel but one may argue that the highlights of this release are stability and interface improvements.

[OpenShot](https://www.openshot.org/) is an open-source video editing tool that's designed for users new in the editing environment. It has simple features such as a simple drag-and-drop function, it provides an easy-to-use and quick-to-learn user interface. The powerful video editor offers tons of efficient ways to cut and trim down your videos. You can freely utilize the unlimited tracks, video effects engine, title editor, 3D animations, slow motion, and time effects. It supports commonly used video codecs that are supported by FFmpeg like WebM (VP9), AVCHD (libx264), HEVC (libx265) and audio codecs like mp3 (libmp3lame) and aac (libfaac). The program can render MPEG4, ogv, Blu-ray and DVD video, and Full HD videos for uploading to the internet video websites like YouTube.

[Lightworks](https://www.lwks.com/) is a non-linear video editing appluication for editing and mastering digital video used by the film industry. Its professional edition has been used for box office hits, such as Shutter Island, Pulp Fiction, and Mission Impossible. Intimidating user interface. Like professional video editors, such as Adobe Premiere Pro, Lightworks is rather complicated to use for new users.

[Shotcut](https://www.shotcut.org/) is an open source multi-platform video editor. You can perform various actions such as video editing (including 4K video quality), add effects, create new movies, import most image files formats, export to almost any file format and much more.

[Olive](https://www.olivevideoeditor.org) is a free non-linear video editor aiming to provide a fully-featured alternative to high-end professional video editing software.

[Natron](https://natrongithub.github.io/) is a powerful Digital Compositor that can handle all of your 2D/2.5D needs. Its robust OIIO file formats and OpenFX architecture is what make Natron the most flexible open source compositor for the visual effects community. Its interface and functionally are the same across all platforms such as MacOS, Linux and Windows.

[OBS (Open Broadcaster Software)](https://obsproject.com/) is free and open source software for video recording and live streaming. Stream to Twitch, YouTube and many other providers or record your own videos with high quality H264 / AAC encoding.

[REAPER](https://www.reaper.fm/) is a complete digital audio production application for computers, offering a full multitrack audio and MIDI recording, editing, processing, mixing and mastering toolset.REAPER supports a vast range of hardware, digital formats and plugins, and can be comprehensively extended, scripted and modified.

[JACK Audio Connection Kit AKA JACK](https://jackaudio.org/) is a professional sound server daemon that provides real-time, low-latency connections for both audio and MIDI data between applications that implement its API. JACK can be configured to send audio data over a network to a "master" machine, which then outputs the audio to a physical device. This can be useful to mix audio from a number of "slave" computers without requiring additional cables or hardware mixers, and keeping the audio path digital for as long as possible.

[Bitwig Studio](https://www.bitwig.com) is a digital audio workstation that has linear and non-linear workflows for sound design, recording, live performance, and more. Along with 90+ instruments, effects, and other creative tools. It is supported Windows, macOS, and Linux.

[PipeWire](https://pipewire.org) is a server and user space API to deal with multimedia pipelines.It provides a low-latency, graph based processing engine on top of audio and video devices that can be used to support the use cases currently handled by both pulseaudio and JACK. PipeWire was designed with a powerful security model that makes interacting with audio and video devices from containerized applications easy. Nodes in the graph can be implemented as separate processes, communicating with sockets and exchanging multimedia content using fd passing.

[Yabridge](https://github.com/robbert-vdh/yabridge) is a modern and transparent way to use Windows VST2 and VST3 plugins on Linux. Yabridge seamlessly supports using both 32-bit and 64-bit Windows VST2 and VST3 plugins in a 64-bit Linux VST host as if they were native VST2 and VST3 plugins, with optional support for [plugin groups](https://github.com/robbert-vdh/yabridge#plugin-groups) to enable inter-plugin communication for VST2 plugins and quick startup times.

[Sonobus](https://sonobus.net) is an easy to use application for streaming high-quality, low-latency peer-to-peer audio between devices over the internet or a local network.

[Avid Pro Tools](https://www.avid.com/pro-tools) is an industry standard audio-production software for songwriters, musicians, producers, and engineers.

[LMMS](https://lmms.io/) is an open source digital audio workstation application program. When LMMS is pairedr with appropriate computer hardware, it allows music to be produced by arranging samples, synthesizing sounds, playing on a MIDI keyboard, and combining the features of trackers and sequencers. Developed by Paul Giblock and Tobias Junghans, this program stands for "Linux MultiMedia Studio" and supports handy plugins that enables it to work on different operating systems.

[Ardour](http://ardour.org/) is an open source, collaborative effort of a worldwide team including musicians, programmers, and professional recording engineers. Development is transparent — anyone can watch our work as it happens. Like a good piece of vintage hardware, you can open the box and look inside.

[Audacity](https://www.audacityteam.org/) is an easy-to-use, multi-track audio editor and recorder for Windows, Mac OS X, GNU/Linux and other operating systems. Developed by a group of volunteers as open source and offered free of charge. Amazing support community.

[Glimpse](https://glimpse-editor.github.io/) is a cross-platform raster graphics editor based on the GNU Image Manipulation Program available for Linux, MacOS, and Windows. A great tool for making YouTube video thumbnails.

# Kubernetes
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/95383873-a884d800-08a0-11eb-8eaf-57af5b119f56.png">
</p>

[Kubernetes (K8s)](https://kubernetes.io/) is an open-source system for automating deployment, scaling, and management of containerized applications.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/105645195-db9ea780-5e4e-11eb-8357-fb38b2f06d74.png">

**Building Highly-Availability(HA) Clusters with kubeadm. Source: [Kubernetes.io](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/high-availability/)**
</p>

[Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine/) is a managed, production-ready environment for running containerized applications.

[Azure Kubernetes Service (AKS)](https://azure.microsoft.com/en-us/services/kubernetes-service/) is serverless Kubernetes, with a integrated continuous integration and continuous delivery (CI/CD) experience, and enterprise-grade security and governance. Unite your development and operations teams on a single platform to rapidly build, deliver, and scale applications with confidence.

[Amazon EKS](https://docs.aws.amazon.com/eks/latest/userguide/what-is-eks.html) is a tool that runs Kubernetes control plane instances across multiple Availability Zones to ensure high availability.

[AWS Controllers for Kubernetes (ACK)](https://aws.amazon.com/blogs/containers/aws-controllers-for-kubernetes-ack/) is a new tool that lets you directly manage AWS services from Kubernetes. ACK makes it simple to build scalable and highly-available Kubernetes applications that utilize AWS services.

[Container Engine for Kubernetes (OKE)](https://www.oracle.com/cloud-native/container-engine-kubernetes/) is an Oracle-managed container orchestration service that can reduce the time and cost to build modern cloud native applications. Unlike most other vendors, Oracle Cloud Infrastructure provides Container Engine for Kubernetes as a free service that runs on higher-performance, lower-cost compute.

[Anthos](https://cloud.google.com/anthos/docs/concepts/overview) is a modern application management platform that provides a consistent development and operations experience for cloud and on-premises environments.

[Red Hat Openshift](https://www.openshift.com/) is a fully managed Kubernetes platform that provides a foundation for on-premises, hybrid, and multicloud deployments.

[OKD](https://okd.io/) is a community distribution of Kubernetes optimized for continuous application development and multi-tenant deployment. OKD adds developer and operations-centric tools on top of Kubernetes to enable rapid application development, easy deployment and scaling, and long-term lifecycle maintenance for small and large teams.

[Odo](https://odo.dev/) is a fast, iterative, and straightforward CLI tool for developers who write, build, and deploy applications on Kubernetes and OpenShift.

[Kata Operator](https://github.com/openshift/kata-operator) is an operator to perform lifecycle management (install/upgrade/uninstall) of [Kata Runtime](https://katacontainers.io/) on Openshift as well as Kubernetes cluster.

[Thanos](https://thanos.io/) is a set of components that can be composed into a highly available metric system with unlimited storage capacity, which can be added seamlessly on top of existing Prometheus deployments.

[OpenShift Hive](https://github.com/openshift/hive) is an operator which runs as a service on top of Kubernetes/OpenShift. The Hive service can be used to provision and perform initial configuration of OpenShift 4 clusters.

[Rook](https://rook.io/) is a tool that turns distributed storage systems into self-managing, self-scaling, self-healing storage services. It automates the tasks of a storage administrator: deployment, bootstrapping, configuration, provisioning, scaling, upgrading, migration, disaster recovery, monitoring, and resource management.

[VMware Tanzu](https://tanzu.vmware.com/tanzu) is a centralized management platform for consistently operating and securing your Kubernetes infrastructure and modern applications across multiple teams and private/public clouds.

[Kubespray](https://kubespray.io/) is a tool that combines Kubernetes and Ansible to easily install Kubernetes clusters that can be deployed on [AWS](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/aws.md), GCE, [Azure](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/azure.md), [OpenStack](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/openstack.md), [vSphere](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/vsphere.md), [Packet](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/packet.md) (bare metal), Oracle Cloud Infrastructure (Experimental), or Baremetal.

[KubeInit](https://github.com/kubeinit/kubeinit) provides Ansible playbooks and roles for the deployment and configuration of multiple Kubernetes distributions.

[Rancher](https://rancher.com/) is a complete software stack for teams adopting containers. It addresses the operational and security challenges of managing multiple Kubernetes clusters, while providing DevOps teams with integrated tools for running containerized workloads.

[K3s](https://github.com/rancher/k3s) is a highly available, certified Kubernetes distribution designed for production workloads in unattended, resource-constrained, remote locations or inside IoT appliances.

[Helm](https://helm.sh/) is a Kubernetes Package Manager tool that makes it easier to install and manage Kubernetes applications.

[Knative](https://knative.dev/) is a Kubernetes-based platform to build, deploy, and manage modern serverless workloads. Knative takes care of the operational overhead details of networking, autoscaling (even to zero), and revision tracking.

[KubeFlow](https://www.kubeflow.org/) is a tool dedicated to making deployments of machine learning (ML) workflows on Kubernetes simple, portable and scalable.

[Etcd](https://etcd.io/) is a distributed key-value store that provides a reliable way to store data that needs to be accessed by a distributed system or cluster of machines. Etcd is used as the backend for service discovery and stores cluster state and configuration for Kubernetes.

[OpenEBS](https://openebs.io/) is a Kubernetes-based tool to create stateful applications using Container Attached Storage.

[Container Storage Interface (CSI)](https://www.architecting.it/blog/container-storage-interface/) is an API that lets container orchestration platforms like Kubernetes seamlessly communicate with stored data via a plug-in.

[MicroK8s](https://microk8s.io/) is a tool that delivers the full Kubernetes experience. In a Fully containerized deployment with compressed over-the-air updates for ultra-reliable operations. It is supported on Linux, Windows, and MacOS.

[Charmed Kubernetes](https://ubuntu.com/kubernetes/features) is a well integrated, turn-key, conformant Kubernetes platform, optimized for your multi-cloud environments developed by Canonical.

[Grafana Kubernetes App](https://grafana.com/grafana/plugins/grafana-kubernetes-app) is a toll that allows you to monitor your Kubernetes cluster's performance. It includes 4 dashboards, Cluster, Node, Pod/Container and Deployment. It allows for the automatic deployment of the required Prometheus exporters and a default scrape config to use with your in cluster Prometheus deployment.

[KubeEdge](https://kubeedge.io/en/) is an open source system for extending native containerized application orchestration capabilities to hosts at Edge.It is built upon kubernetes and provides fundamental infrastructure support for network, app. deployment and metadata synchronization between cloud and edge.

[Lens](https://k8slens.dev/)  is the most powerful IDE for people who need to deal with Kubernetes clusters on a daily basis. It has support for MacOS, Windows and Linux operating systems.

[kind](https://kind.sigs.k8s.io/) is a tool for running local Kubernetes clusters using Docker container “nodes”. It was primarily designed for testing Kubernetes itself, but may be used for local development or CI.

[Flux CD](https://fluxcd.io/) is a tool that automatically ensures that the state of your Kubernetes cluster matches the configuration you've supplied in Git. It uses an operator in the cluster to trigger deployments inside Kubernetes, which means that you don't need a separate continuous delivery tool.

## Kubernetes Learning Resources

[Getting Kubernetes Certifications](https://training.linuxfoundation.org/certification/catalog/?_sft_technology=kubernetes)

[Getting started with Kubernetes on AWS](https://aws.amazon.com/kubernetes/)

[Kubernetes on Microsoft Azure](https://azure.microsoft.com/en-us/topic/what-is-kubernetes/)

[Intro to Azure Kubernetes Service](https://docs.microsoft.com/en-us/azure/aks/kubernetes-dashboard)

[Getting started with Google Cloud](https://cloud.google.com/learn/what-is-kubernetes)

[Getting started with Kubernetes on Red Hat](https://www.redhat.com/en/topics/containers/what-is-kubernetes)

[Getting started with Kubernetes on IBM](https://www.ibm.com/cloud/learn/kubernetes)

[YAML basics in Kubernetes](https://developer.ibm.com/technologies/containers/tutorials/yaml-basics-and-usage-in-kubernetes/)

[Elastic Cloud on Kubernetes](https://www.elastic.co/elastic-cloud-kubernetes)

[Docker and Kubernetes](https://www.docker.com/products/kubernetes)

[Deploy a model to an Azure Kubernetes Service cluster](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python)

[Simplify Machine Learning Inference on Kubernetes with Amazon SageMaker Operators](https://aws.amazon.com/blogs/machine-learning/simplify-machine-learning-inference-on-kubernetes-with-amazon-sagemaker-operators/)

[Running Apache Spark on Kubernetes](http://spark.apache.org/docs/latest/running-on-kubernetes.html)

[Kubernetes Across VMware vRealize Automation](https://blogs.vmware.com/management/2019/06/kubernetes-across-vmware-cloud-automation-services.html)

[VMware Tanzu Kubernetes Grid](https://tanzu.vmware.com/kubernetes-grid)

[All the Ways VMware Tanzu Works with AWS](https://tanzu.vmware.com/content/blog/all-the-ways-vmware-tanzutm-works-with-aws)

[VMware Tanzu Education](https://tanzu.vmware.com/education)

[Using Ansible in a Cloud-Native Kubernetes Environment](https://www.ansible.com/blog/how-useful-is-ansible-in-a-cloud-native-kubernetes-environment)

[Managing Kubernetes (K8s) objects with Ansible](https://docs.ansible.com/ansible/latest/collections/community/kubernetes/k8s_module.html)

[Setting up a Kubernetes cluster using Vagrant and Ansible](https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/)

[Running MongoDB with Kubernetes](https://www.mongodb.com/kubernetes)

[Kubernetes Fluentd](https://docs.fluentd.org/v/0.12/articles/kubernetes-fluentd)

[Understanding the new GitLab Kubernetes Agent](https://about.gitlab.com/blog/2020/09/22/introducing-the-gitlab-kubernetes-agent/)

[Kubernetes Contributors](https://www.kubernetes.dev/)

[KubeAcademy from VMware](https://kube.academy/)


# Machine Learning
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<img src="https://user-images.githubusercontent.com/45159366/108111395-756e0480-7049-11eb-85ca-b87315e9d3ef.jpeg">

## ML frameworks & applications

[TensorFlow](https://www.tensorflow.org) is an end-to-end open source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML powered applications.

[Tensorman](https://github.com/pop-os/tensorman) is a utility for easy management of Tensorflow containers by developed by [System76]( https://system76.com).Tensorman allows Tensorflow to operate in an isolated environment that is contained from the rest of the system. This virtual environment can operate independent of the base system, allowing you to use any version of Tensorflow on any version of a Linux distribution that supports the Docker runtime.

[Keras](https://keras.io) is a high-level neural networks API, written in Python and capable of running on top of TensorFlow, CNTK, or Theano.It was developed with a focus on enabling fast experimentation. It is capable of running on top of TensorFlow, Microsoft Cognitive Toolkit, R, Theano, or PlaidML.

[PyTorch](https://pytorch.org) is a library for deep learning on irregular input data such as graphs, point clouds, and manifolds. Primarily developed by Facebook's AI Research lab.

[Amazon SageMaker](https://aws.amazon.com/sagemaker/) is a fully managed service that provides every developer and data scientist with the ability to build, train, and deploy machine learning (ML) models quickly. SageMaker removes the heavy lifting from each step of the machine learning process to make it easier to develop high quality models.

[Azure Databricks](https://azure.microsoft.com/en-us/services/databricks/) is a fast and collaborative Apache Spark-based big data analytics service designed for data science and data engineering. Azure Databricks, sets up your Apache Spark environment in minutes, autoscale, and collaborate on shared projects in an interactive workspace. Azure Databricks supports Python, Scala, R, Java, and SQL, as well as data science frameworks and libraries including TensorFlow, PyTorch, and scikit-learn.

[Microsoft Cognitive Toolkit (CNTK)](https://docs.microsoft.com/en-us/cognitive-toolkit/) is an open-source toolkit for commercial-grade distributed deep learning. It describes neural networks as a series of computational steps via a directed graph. CNTK allows the user to easily realize and combine popular model types such as feed-forward DNNs, convolutional neural networks (CNNs) and recurrent neural networks (RNNs/LSTMs). CNTK implements stochastic gradient descent (SGD, error backpropagation) learning with automatic differentiation and parallelization across multiple GPUs and servers.

[Apache Airflow](https://airflow.apache.org) is an open-source workflow management platform created by the community to programmatically author, schedule and monitor workflows. Install. Principles. Scalable. Airflow has a modular architecture and uses a message queue to orchestrate an arbitrary number of workers. Airflow is ready to scale to infinity.

[Open Neural Network Exchange(ONNX)](https://github.com/onnx) is an open ecosystem that empowers AI developers to choose the right tools as their project evolves. ONNX provides an open source format for AI models, both deep learning and traditional ML. It defines an extensible computation graph model, as well as definitions of built-in operators and standard data types.

[Apache MXNet](https://mxnet.apache.org/) is a deep learning framework designed for both efficiency and flexibility. It allows you to mix symbolic and imperative programming to maximize efficiency and productivity. At its core, MXNet contains a dynamic dependency scheduler that automatically parallelizes both symbolic and imperative operations on the fly. A graph optimization layer on top of that makes symbolic execution fast and memory efficient. MXNet is portable and lightweight, scaling effectively to multiple GPUs and multiple machines. Support for Python, R, Julia, Scala, Go, Javascript and more.

[AutoGluon](https://autogluon.mxnet.io/index.html) is toolkit for Deep learning that automates machine learning tasks enabling you to easily achieve strong predictive performance in your applications. With just a few lines of code, you can train and deploy high-accuracy deep learning models on tabular, image, and text data.

[Anaconda](https://www.anaconda.com/) is a very popular Data Science platform for machine learning and deep learning that enables users to develop models, train them, and deploy them.

[PlaidML](https://github.com/plaidml/plaidml) is an advanced and portable tensor compiler for enabling deep learning on laptops, embedded devices, or other devices where the available computing hardware is not well supported or the available software stack contains unpalatable license restrictions.

[OpenCV](https://opencv.org) is a highly optimized library with focus on real-time computer vision applications. The C++, Python, and Java interfaces support Linux, MacOS, Windows, iOS, and Android.

[Scikit-Learn](https://scikit-learn.org/stable/index.html) is a Python module for machine learning built on top of SciPy, NumPy, and matplotlib, making it easier to apply robust and simple implementations of many popular machine learning algorithms.

[Weka](https://www.cs.waikato.ac.nz/ml/weka/) is an open source machine learning software that can be accessed through a graphical user interface, standard terminal applications, or a Java API. It is widely used for teaching, research, and industrial applications, contains a plethora of built-in tools for standard machine learning tasks, and additionally gives transparent access to well-known toolboxes such as scikit-learn, R, and Deeplearning4j.

[Caffe](https://github.com/BVLC/caffe) is a deep learning framework made with expression, speed, and modularity in mind. It is developed by Berkeley AI Research (BAIR)/The Berkeley Vision and Learning Center (BVLC) and community contributors.

[Theano](https://github.com/Theano/Theano) is a Python library that allows you to define, optimize, and evaluate mathematical expressions involving multi-dimensional arrays efficiently including tight integration with NumPy.

[nGraph](https://github.com/NervanaSystems/ngraph) is an open source C++ library, compiler and runtime for Deep Learning. The nGraph Compiler aims to accelerate developing AI workloads using any deep learning framework and deploying to a variety of hardware targets.It provides the freedom, performance, and ease-of-use to AI developers.

[NVIDIA cuDNN](https://developer.nvidia.com/cudnn) is a GPU-accelerated library of primitives for [deep neural networks](https://developer.nvidia.com/deep-learning). cuDNN provides highly tuned implementations for standard routines such as forward and backward convolution, pooling, normalization, and activation layers. cuDNN accelerates widely used deep learning frameworks, including [Caffe2](https://caffe2.ai/), [Chainer](https://chainer.org/), [Keras](https://keras.io/), [MATLAB](https://www.mathworks.com/solutions/deep-learning.html), [MxNet](https://mxnet.incubator.apache.org/), [PyTorch](https://pytorch.org/), and [TensorFlow](https://www.tensorflow.org/).

[Jupyter Notebook](https://jupyter.org/) is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. Jupyter is used widely in industries that do data cleaning and transformation, numerical simulation, statistical modeling, data visualization, data science, and machine learning.

[Apache Spark](https://spark.apache.org/) is a unified analytics engine for large-scale data processing. It provides high-level APIs in Scala, Java, Python, and R, and an optimized engine that supports general computation graphs for data analysis. It also supports a rich set of higher-level tools including Spark SQL for SQL and DataFrames, MLlib for machine learning, GraphX for graph processing, and Structured Streaming for stream processing.

[Apache Spark Connector for SQL Server and Azure SQL](https://github.com/microsoft/sql-spark-connector) is a high-performance connector that enables you to use transactional data in big data analytics and persists results for ad-hoc queries or reporting. The connector allows you to use any SQL database, on-premises or in the cloud, as an input data source or output data sink for Spark jobs.

[Apache PredictionIO](https://predictionio.apache.org/) is an open source machine learning framework for developers, data scientists, and end users. It supports event collection, deployment of algorithms, evaluation, querying predictive results via REST APIs. It is based on scalable open source services like Hadoop, HBase (and other DBs), Elasticsearch, Spark and implements what is called a Lambda Architecture.

[Cluster Manager for Apache Kafka(CMAK)](https://github.com/yahoo/CMAK) is a tool for managing [Apache Kafka](https://kafka.apache.org/) clusters.

[BigDL](https://bigdl-project.github.io/) is a distributed deep learning library for Apache Spark. With BigDL, users can write their deep learning applications as standard Spark programs, which can directly run on top of existing Spark or Hadoop clusters.

[Koalas](https://pypi.org/project/koalas/) is project makes data scientists more productive when interacting with big data, by implementing the pandas DataFrame API on top of Apache Spark.

[Apache Spark™ MLflow](https://mlflow.org/) is an open source platform to manage the ML lifecycle, including experimentation, reproducibility, deployment, and a central model registry. MLflow currently offers four components:

**[MLflow Tracking](https://mlflow.org/docs/latest/tracking.html)**: Record and query experiments: code, data, config, and results.

**[MLflow Projects](https://mlflow.org/docs/latest/projects.html)**: Package data science code in a format to reproduce runs on any platform.

**[MLflow Models](https://mlflow.org/docs/latest/models.html)**: Deploy machine learning models in diverse serving environments.

**[Model Registry](https://mlflow.org/docs/latest/model-registry.html)**: Store, annotate, discover, and manage models in a central repository.

[Eclipse Deeplearning4J (DL4J)](https://deeplearning4j.konduit.ai/) is a set of projects intended to support all the needs of a JVM-based(Scala, Kotlin, Clojure, and Groovy) deep learning application. This means starting with the raw data, loading and preprocessing it from wherever and whatever format it is in to building and tuning a wide variety of simple and complex deep learning networks.

[Numba](https://github.com/numba/numba) is an open source, NumPy-aware optimizing compiler for Python sponsored by Anaconda, Inc. It uses the LLVM compiler project to generate machine code from Python syntax. Numba can compile a large subset of numerically-focused Python, including many NumPy functions. Additionally, Numba has support for automatic parallelization of loops, generation of GPU-accelerated code, and creation of ufuncs and C callbacks.

[Chainer](https://chainer.org/) is a Python-based deep learning framework aiming at flexibility. It provides automatic differentiation APIs based on the define-by-run approach (dynamic computational graphs) as well as object-oriented high-level APIs to build and train neural networks. It also supports CUDA/cuDNN using [CuPy](https://github.com/cupy/cupy) for high performance training and inference.

[cuML](https://github.com/rapidsai/cuml) is a suite of libraries that implement machine learning algorithms and mathematical primitives functions that share compatible APIs with other RAPIDS projects. cuML enables data scientists, researchers, and software engineers to run traditional tabular ML tasks on GPUs without going into the details of CUDA programming. In most cases, cuML's Python API matches the API from scikit-learn.

## Online ML Learning Resources

[Machine Learning by Stanford University from Coursera](https://www.coursera.org/learn/machine-learning)

[Machine Learning Courses Online from Coursera](https://www.coursera.org/courses?query=machine%20learning&)

[Machine Learning Courses Online from Udemy](https://www.udemy.com/topic/machine-learning/)

[Learn Machine Learning with Online Courses and Classes from edX](https://www.edx.org/learn/machine-learning)

# Robotics
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/96352533-b55fb380-1078-11eb-874c-f165cbcce899.png">
</p>

## Tools for Robotics

[ROS](https://www.ros.org/) is robotics middleware. Although ROS is not an operating system, it provides services designed for a heterogeneous computer cluster such as hardware abstraction, low-level device control, implementation of commonly used functionality, message-passing between processes, and package management.

[ROS2](https://index.ros.org/doc/ros2/) is a set of [software libraries and tools](https://github.com/ros2) that help you build robot applications. From drivers to state-of-the-art algorithms, and with powerful developer tools, ROS has what you need for your next robotics project. And it’s all open source.

[Robot Framework](https://robotframework.org/) is a generic open source automation framework. It can be used for test automation and robotic process automation. It has easy syntax, utilizing human-readable keywords. Its capabilities can be extended by libraries implemented with Python or Java.

[The Robotics Library (RL)](https://github.com/roboticslibrary/rl) is a self-contained C++ library for robot kinematics, motion planning and control. It covers mathematics, kinematics and dynamics, hardware abstraction, motion planning, collision detection, and visualization.RL runs on many different systems, including Linux, macOS, and Windows. It uses CMake as a build system and can be compiled with Clang, GCC, and Visual Studio.

[MoveIt](https://moveit.ros.org/) is the most widely used software for manipulation and has been used on over 100 robots. It provides an easy-to-use robotics platform for developing advanced applications, evaluating new designs and building integrated products for industrial, commercial, R&D, and other domains.

[AutoGluon](https://autogluon.mxnet.io/index.html) is toolkit for [Deep learning](https://gitlab.com/maos20008/intro-to-machine-learning) that automates machine learning tasks enabling you to easily achieve strong predictive performance in your applications. With just a few lines of code, you can train and deploy high-accuracy deep learning models on tabular, image, and text data.

[Gazebo](http://gazebosim.org/) accurately and efficiently simulates indoor and outdoor robots. You get a robust physics engine, high-quality graphics, and programmatic and graphical interfaces.

[Robotics System Toolbox](https://www.mathworks.com/products/robotics.html) provides tools and algorithms for designing, simulating, and testing manipulators, mobile robots, and humanoid robots. For manipulators and humanoid robots, the toolbox includes algorithms for collision checking, trajectory generation, forward and inverse kinematics, and dynamics using a rigid body tree representation.
For mobile robots, it includes algorithms for mapping, localization, path planning, path following, and motion control. The toolbox provides reference examples of common industrial robot applications. It also includes a library of
commercially available industrial robot models that you can import, visualize, and simulate.

[Intel Robot DevKit](https://github.com/intel/robot_devkit) is the tool to generate Robotics Software Development Kit (RDK) designed for autonomous devices, including the ROS2 core and capacibilities packages like perception, planning, control driver etc. It provides flexible build/runtime configurations to meet different autonomous requirement on top of diversity hardware choices, for example use different hareware engine CPU/GPU/VPU to accelerate AI related features.

[Arduino](https://www.arduino.cc/) is an open-source platform used for building electronics projects. Arduino consists of both a physical programmable circuit board (often referred to as a microcontroller) and a piece of software, or IDE (Integrated Development Environment) that runs on your computer, used to write and upload computer code to the physical board.

[ArduPilot](https://ardupilot.org/ardupilot/index.html) enables the creation and use of trusted, autonomous, unmanned vehicle systems for the peaceful benefit of all. ArduPilot provides a comprehensive suite of tools suitable for almost any vehicle and application.

[AirSim](https://github.com/Microsoft/AirSim) is a simulator for drones, cars and more, built on Unreal Engine (we now also have an experimental Unity release). It is open-source, cross platform, and supports hardware-in-loop with popular flight controllers such as PX4 for physically and visually realistic simulations.

[F´ (F Prime)](https://github.com/nasa/fprime) is a component-driven framework that enables rapid development and deployment of spaceflight and other embedded software applications. Originally developed at the Jet Propulsion Laboratory, F´ has been successfully deployed on several space applications.

[The JPL Open Source Rover](https://github.com/nasa-jpl/open-source-rover) is an open source, build it yourself, scaled down version of the 6 wheel rover design that JPL uses to explore the surface of Mars. The Open Source Rover is designed almost entirely out of consumer off the shelf (COTS) parts. This project is intended to be a teaching and learning experience for those who want to get involved in mechanical engineering, software, electronics, or robotics.

[Light Detection and Ranging(LiDAR)](https://en.wikipedia.org/wiki/Lidar) is a remote sensing method that uses light in the form of a pulsed laser at an object, and uses the time and wavelength of the reflected beam of light to estimate the distance and in some applications ([Laser Imaging](https://en.wikipedia.org/wiki/Laser_scanning)), to create a 3D representation of the object and its surface characteristics. This technology is commonly used in aircraft and self-driving vehicles.

[AliceVision](https://github.com/alicevision/AliceVision) is a Photogrammetric Computer Vision Framework which provides a 3D Reconstruction and Camera Tracking algorithms. AliceVision aims to provide strong software basis with state-of-the-art computer vision algorithms that can be tested, analyzed and reused. The project is a result of collaboration between academia and industry to provide cutting-edge algorithms with the robustness and the quality required for production usage.

[CARLA](https://github.com/carla-simulator/carla) is an open-source simulator for autonomous driving research. CARLA has been developed from the ground up to support development, training, and validation of autonomous driving systems. In addition to open-source code and protocols, CARLA provides open digital assets (urban layouts, buildings, vehicles) that were created for this purpose and can be used freely. The simulation platform supports flexible specification of sensor suites and environmental conditions.

[ROS bridge](https://github.com/carla-simulator/ros-bridge) is a package to bridge ROS for CARLA Simulator.

[ROS-Industrial](https://rosindustrial.org/) is an open source project that extends the advanced capabilities of ROS software to manufacturing.

[AWS RoboMaker](https://aws.amazon.com/robomaker/) is the most complete cloud solution for robotic developers to simulate, test and securely deploy robotic applications at scale. RoboMaker provides a fully-managed, scalable infrastructure for simulation that customers use for multi-robot simulation and CI/CD integration with regression testing in simulation.

[Microsoft Robotics Developer Studio](https://www.microsoft.com/en-us/download/details.aspx?id=29081)  is a free .NET-based programming environment for building robotics applications.

[Visual Studio Code Extension for ROS](https://github.com/ms-iot/vscode-ros) is an extension provides support for Robot Operating System (ROS) development.

[Azure Kinect ROS Driver](https://github.com/microsoft/azure_kinect_ros_driver) is a node which publishes sensor data from the [Azure Kinect Developer Kit](https://azure.microsoft.com/en-us/services/kinect-dk/) to the [Robot Operating System (ROS)](http://www.ros.org/). Developers working with ROS can use this node to connect an Azure Kinect Developer Kit to an existing ROS installation.

[Azure IoT Hub for ROS](https://github.com/microsoft/ros_azure_iothub) is a ROS package works with the Microsoft Azure IoT Hub service to relay telemetry messages from the Robot to Azure IoT Hub or reflect properties from the Digital Twin to the robot using dynamic reconfigure.

[ROS 2 with ONNX Runtime](https://github.com/ms-iot/ros_msft_onnx) is a program that uses ROS 2 to run on different hardware platforms using their respective AI acceleration libraries for optimized execution of the ONNX model.

[Azure Cognitive Services LUIS ROS Node](https://github.com/ms-iot/ros_msft_luis) is a ROS node that bridges between ROS and the Azure Language Understanding Service. it can be configured to process audio directly from a microphone, or can subscribe to a ROS audio topic, then processes speech and generates "intent" ROS messages which can be processed by another ROS node to generate ROS commands.

## Robotics Learning Resources

[Robotics courses from Coursera](https://www.edx.org/learn/robotics)

[Learn Robotics with Online Courses and Classes from edX](https://www.edx.org/learn/robotics)

[Top Robotics Courses Online from Udemy](https://www.udemy.com/topic/robotics/)

[Free Online AI & Robotics Courses](https://www.futurelearn.com/subjects/it-and-computer-science-courses/ai-and-robotics)

[REC Foundation Robotics Industry Certification](https://www.roboticseducation.org/industry-certifications/)

[Carnegie Mellon Robotics Academy](https://www.cmu.edu/roboticsacademy/Training/Certifications.html)

[RIA Robotic Integrator Certification Program](https://www.robotics.org/robotics/integrator-certification)

[AWS RoboMaker – Develop, Test, Deploy, and Manage Intelligent Robotics Apps](https://aws.amazon.com/blogs/aws/aws-robomaker-develop-test-deploy-and-manage-intelligent-robotics-apps/)

[Microsoft AI School](https://aischool.microsoft.com/en-us/home)

[Language Understanding (LUIS) for Azure Cognitive Services](https://docs.microsoft.com/en-us/azure/cognitive-services/luis/what-is-luis)

[Azure VM templates to bootstrap ROS and ROS 2 environments](https://ms-iot.github.io/ROSOnWindows/ROSAtMS/AzureVM.html)

[Google Robotics Research](https://research.google/teams/brain/robotics/)

# Open Source Security
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/96352529-af69d280-1078-11eb-9e87-8a73f48af246.png">
</p>

[Open Source Security Foundation (OpenSSF)](https://openssf.org/) is a cross-industry collaboration that brings together leaders to improve the security of open source software by building a broader community, targeted initiatives, and best practices. The OpenSSF brings together open source security initiatives under one foundation to accelerate work through cross-industry support. Along with the Core Infrastructure Initiative and the Open Source Security Coalition, and will include new working groups that address vulnerability disclosures, security tooling and more.

## Security Standards, Frameworks and Benchmarks

[STIGs Benchmarks - Security Technical Implementation Guides](https://public.cyber.mil/stigs/)

[CIS Benchmarks - CIS Center for Internet Security](https://www.cisecurity.org/cis-benchmarks/)

[NIST - Current FIPS](https://www.nist.gov/itl/current-fips)

[ISO Standards Catalogue](https://www.iso.org/standards.html)

[Common Criteria for Information Technology Security Evaluation (CC)](https://www.commoncriteriaportal.org/cc/) is an international standard (ISO / IEC 15408) for computer security. It allows an objective evaluation to validate that a particular product satisfies a defined set of security requirements.

[ISO 22301](https://www.iso.org/en/contents/data/standard/07/51/75106.html) is the international standard that provides a best-practice framework for implementing an optimised BCMS (business continuity management system).

[ISO27001](https://www.iso.org/isoiec-27001-information-security.html) is the international standard that describes the requirements for an ISMS (information security management system). The framework is designed to help organizations manage their security practices in one place, consistently and cost-effectively.

[ISO 27701](https://www.iso.org/en/contents/data/standard/07/16/71670.html) specifies the requirements for a PIMS (privacy information management system) based on the requirements of ISO 27001.
It is extended by a set of privacy-specific requirements, control objectives and controls. Companies that have implemented ISO 27001 will be able to use ISO 27701 to extend their security efforts to cover privacy management.

[EU GDPR (General Data Protection Regulation)](https://gdpr.eu/) is a privacy and data protection law that supersedes existing national data protection laws across the EU, bringing uniformity by introducing just one main data protection law for companies/organizations to comply with.

[CCPA (California Consumer Privacy Act)](https://www.oag.ca.gov/privacy/ccpa) is a data privacy law that took effect on January 1, 2020 in the State of California. It applies to businesses that collect California residents’ personal information, and its privacy requirements are similar to those of the EU’s GDPR (General Data Protection Regulation).

[Payment Card Industry (PCI) Data Security Standards (DSS)](https://docs.microsoft.com/en-us/microsoft-365/compliance/offering-pci-dss) is a global information security standard designed to prevent fraud through increased control of credit card data.

[SOC 2](https://www.aicpa.org/interestareas/frc/assuranceadvisoryservices/aicpasoc2report.html) is an auditing procedure that ensures your service providers securely manage your data to protect the interests of your comapny/organization and the privacy of their clients.

[NIST CSF](https://www.nist.gov/national-security-standards) is a voluntary framework primarily intended for critical infrastructure organizations to manage and mitigate cybersecurity risk based on existing best practice.

## Security Tools

[AppArmor](https://www.apparmor.net/) is an effective and easy-to-use Linux application security system. AppArmor proactively protects the operating system and applications from external or internal threats, even zero-day attacks, by enforcing good behavior and preventing both known and unknown application flaws from being exploited. AppArmor supplements the traditional Unix discretionary access control (DAC) model by providing mandatory access control (MAC). It has been included in the mainline Linux kernel since version 2.6.36 and its development has been supported by Canonical since 2009.

[SELinux](https://github.com/SELinuxProject/selinux) is a security enhancement to Linux which allows users and administrators more control over access control. Access can be constrained on such variables as which users and applications can access which resources. These resources may take the form of files. Standard Linux access controls, such as file modes (-rwxr-xr-x) are modifiable by the user and the applications which the user runs. Conversely, SELinux access controls are determined by a policy loaded on the system which may not be changed by careless users or misbehaving applications.

[Control Groups(Cgroups)](https://www.redhat.com/sysadmin/cgroups-part-one) is a Linux kernel feature that allows you to allocate resources such as CPU time, system memory, network bandwidth, or any combination of these resources for user-defined groups of tasks (processes) running on a system.

[EarlyOOM](https://github.com/rfjakob/earlyoom) is a daemon for Linux that enables users to more quickly recover and regain control over their system in low-memory situations with heavy swap usage.

[Libgcrypt](https://www.gnupg.org/related_software/libgcrypt/) is a general purpose cryptographic library originally based on code from GnuPG.

[Kali Linux](https://www.kali.org/)  is an open source project that is maintained and funded by Offensive Security, a provider of world-class information security training and penetration testing services.

[Pi-hole](https://pi-hole.net/) is a [DNS sinkhole](https://en.wikipedia.org/wiki/DNS_Sinkhole) that protects your devices from unwanted content, without installing any client-side software, intended for use on a private network. It is designed for use on embedded devices with network capability, such as the Raspberry Pi, but it can be used on other machines running Linux and cloud implementations.

[Aircrack-ng](https://www.aircrack-ng.org/) is a network software suite consisting of a detector, packet sniffer, WEP and WPA/WPA2-PSK cracker and analysis tool for 802.11 wireless LANs. It works with any wireless network interface controller whose driver supports raw monitoring mode and can sniff 802.11a, 802.11b and 802.11g traffic.

[Burp Suite](https://portswigger.net/burp) is a leading range of cybersecurity tools.

[KernelCI](https://foundation.kernelci.org/) is a community-based open source distributed test automation system focused on upstream kernel development. The primary goal of KernelCI is to use an open testing philosophy to ensure the quality, stability and long-term maintenance of the Linux kernel.

[Continuous Kernel Integration project](https://github.com/cki-project) helps find bugs in kernel patches before they are commited to an upstram kernel tree. We are team of kernel developers, kernel testers, and automation engineers.

[eBPF](https://ebpf.io) is a revolutionary technology that can run sandboxed programs in the Linux kernel without changing kernel source code or loading kernel modules. By making the Linux kernel programmable, infrastructure software can leverage existing layers, making them more intelligent and feature-rich without continuing to add additional layers of complexity to the system.

[Cilium](https://cilium.io/) uses eBPF to accelerate getting data in and out of L7 proxies such as Envoy, enabling efficient visibility into API protocols like HTTP, gRPC, and Kafka.

[Hubble](https://github.com/cilium/hubble) is a Network, Service & Security Observability for Kubernetes using eBPF.

[Istio](https://istio.io/) is an open platform to connect, manage, and secure microservices. Istio's control plane provides an abstraction layer over the underlying cluster management platform, such as Kubernetes and Mesos.

[Certgen](https://github.com/cilium/certgen) is a convenience tool to generate and store certificates for Hubble Relay mTLS.

[Scapy](https://scapy.net/) is a python-based interactive packet manipulation program & library.

[syzkaller](https://github.com/google/syzkaller) is an unsupervised, coverage-guided kernel fuzzer.

[SchedViz](https://github.com/google/schedviz) is a tool for gathering and visualizing kernel scheduling traces on Linux machines.

[oss-fuzz](https://google.github.io/oss-fuzz/) aims to make common open source software more secure and stable by combining modern fuzzing techniques with scalable, distributed execution.

[OSSEC](https://www.ossec.net/) is a free, open-source host-based intrusion detection system. It performs log analysis, integrity checking, Windows registry monitoring, rootkit detection, time-based alerting, and active response.

[Metasploit Project](https://www.metasploit.com/) is a computer security project that provides information about security vulnerabilities and aids in penetration testing and IDS signature development.

[Wfuzz](https://github.com/xmendez/wfuzz) was created to facilitate the task in web applications assessments and it is based on a simple concept: it replaces any reference to the FUZZ keyword by the value of a given payload.

[Nmap](https://nmap.org/) is a security scanner used to discover hosts and services on a computer network, thus building a "map" of the network.

[Patchwork](https://github.com/getpatchwork/patchwork) is a web-based patch tracking system designed to facilitate the contribution and management of contributions to an open-source project.

[pfSense](https://www.pfsense.org/) is a free and open source firewall and router that also features unified threat management, load balancing, multi WAN, and more.

[Snowpatch](https://github.com/ruscur/snowpatch) is a continuous integration tool for projects using a patch-based, mailing-list-centric git workflow. This workflow is used by a number of well-known open source projects such as the Linux kernel.

[Snort](https://www.snort.org/) is an open-source, free and lightweight network intrusion detection system (NIDS) software for Linux and Windows to detect emerging threats.

[Wireshark](https://www.wireshark.org/) is a free and open-source packet analyzer. It is used for network troubleshooting, analysis, software and communications protocol development, and education.

[OpenSCAP](https://www.open-scap.org/) is U.S. standard maintained by [National Institute of Standards and Technology (NIST)](https://www.nist.gov/). It provides multiple tools to assist administrators and auditors with assessment, measurement, and enforcement of security baselines. OpenSCAP maintains great flexibility and interoperability by reducing the costs of performing security audits. Whether you want to evaluate DISA STIGs, NIST‘s USGCB, or Red Hat’s Security Response Team’s content, all are supported by OpenSCAP.

[Tink](https://github.com/google/tink) is a multi-language, cross-platform, open source library that provides cryptographic APIs that are secure, easy to use correctly, and harder to misuse.

[OWASP](https://www.owasp.org/index.php/Main_Page) is an online community, produces freely-available articles, methodologies, documentation, tools, and technologies in the field of web application security.

[Open Vulnerability and Assessment Language](https://oval.mitre.org/) is a community effort to standardize how to assess and report upon the machine state of computer systems. OVAL includes a language to encode system details, and community repositories of content. Tools and services that use OVAL provide enterprises with accurate, consistent, and actionable information to improve their security.

[ClamAV](https://www.clamav.net/) is an open source antivirus engine for detecting trojans, viruses, malware & other malicious threats.

## Open Source Security Learning Resources

[Microsoft Open Source Software Security](https://www.microsoft.com/en-us/securityengineering/opensource)

[Cloudflare Open Source Security](https://cloudflare.github.io)

[The Seven Properties of Highly Secure Devices](https://www.microsoft.com/en-us/research/publication/seven-properties-highly-secure-devices/)

[How Layer 7 of the Internet Works](https://www.cloudflare.com/learning/ddos/what-is-layer-7/)

[The 7 Kinds of Security](https://www.veracode.com/sites/default/files/Resources/eBooks/7-kinds-of-security.pdf)

[The Libgcrypt Reference Manual](https://www.gnupg.org/documentation/manuals/gcrypt/)

[The Open Web Application Security Project(OWASP) Foundation Top 10](https://owasp.org/www-project-top-ten/)

[Best Practices for Using Open Source Code from The Linux Foundation](https://www.linuxfoundation.org/blog/2017/11/best-practices-using-open-source-code/)

[AWS Certified Security - Specialty Certification](https://aws.amazon.com/certification/certified-security-specialty/)

[Microsoft Certified: Azure Security Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer)

[Google Cloud Certified Professional Cloud Security Engineer](https://cloud.google.com/certification/cloud-security-engineer)

[Cisco Security Certifications](https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/security.html)

[The Red Hat Certified Specialist in Security: Linux](https://www.redhat.com/en/services/training/ex415-red-hat-certified-specialist-security-linux-exam)

[Linux Professional Institute LPIC-3 Enterprise Security Certification](https://www.lpi.org/our-certifications/lpic-3-303-overview)

[Cybersecurity Training and Courses from IBM Skills](https://www.ibm.com/skills/topics/cybersecurity/)

[Cybersecurity Courses and Certifications by Offensive Security](https://www.offensive-security.com/courses-and-certifications/)

[RSA Certification Program](https://community.rsa.com/community/training/certification)

[Check Point Certified Security Expert(CCSE) Certification](https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Expert%20(CCSE)%20R80.x)

[Check Point Certified Security Administrator(CCSA) Certification](https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Admin%20(CCSA)%20R80.x)

[Check Point Certified Security Master (CCSM) Certification](https://training-certifications.checkpoint.com/#/courses/Check%20Point%20Certified%20Master%20(CCSM)%20R80.x)

[Certified Cloud Security Professional(CCSP) Certification](https://www.isc2.org/Certifications/CCSP)

[Certified Information Systems Security Professional (CISSP) Certification](https://www.isc2.org/Certifications/CISSP)

[CCNP Routing and Switching](https://learningnetwork.cisco.com/s/ccnp-enterprise)

[Certified Information Security Manager(CISM)](https://www.isaca.org/credentialing/cism)

[Wireshark Certified Network Analyst (WCNA)](https://www.wiresharktraining.com/certification.html)

[Juniper Networks Certification Program Enterprise (JNCP)](https://www.juniper.net/us/en/training/certification/)

[Security Training Certifications and Courses from Udemy](https://www.udemy.com/courses/search/?src=ukw&q=secuirty)

[Security Training Certifications and Courses from Coursera](https://www.coursera.org/search?query=security&)

[Security Certifications Training from Pluarlsight](https://www.pluralsight.com/browse/information-cyber-security/security-certifications)

# Differential Privacy
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/103486336-fd59c100-4db1-11eb-9780-a0b90bd5db1f.png">
</h1>

[Differential Privacy](https://www.microsoft.com/en-us/ai/ai-lab-differential-privacy) is a system that simultaneously enables researchers and analysts to extract useful insights from datasets containing personal information and offers stronger privacy protections. This is achieved by introducing "statistical noise".

[Statistical Noise](https://news.microsoft.com/on-the-issues/2020/08/27/statistical-noise-data-differential-privacy/) is a process that small aletrations to masked datasets. The statistical noise hides identifiable characteristics of individuals, ensuring that the privacy of personal information is protected, but it's small enough to not materially impact the accuracy of the answers extracted by analysts and researchers.

[Laplacian Noise](https://en.wikipedia.org/wiki/Laplace_distribution) is a mechanism that adds Laplacian-distributed noise to a function.

<p align="center">
<img src="https://user-images.githubusercontent.com/45159366/103486337-ff238480-4db1-11eb-9895-f7f49cc5715a.png">
<br />
Above is a simple diagram of how Differential Privacy-Preserving Data Sharing and Data Mining protects a User's Data
</p>

## Tools

[PySyft](https://github.com/OpenMined/PySyft) is a Python library for secure and private Deep Learning. PySyft decouples private data from model training, using [Federated Learning](https://ai.googleblog.com/2017/04/federated-learning-collaborative.html), [Differential Privacy](https://www.microsoft.com/en-us/ai/ai-lab-differential-privacy), and Encrypted Computation (like [Multi-Party Computation (MPC)](https://multiparty.org) and [Homomorphic Encryption (HE)](https://www.microsoft.com/en-us/research/project/homomorphic-encryption/) within the main Deep Learning frameworks like [PyTorch](https://pytorch.org/) and [TensorFlow](https://www.tensorflow.org/).

[TensorFlow Privacy](https://github.com/tensorflow/privacy) is a  Python library that includes implementations of TensorFlow optimizers for training machine learning models with differential privacy. The library comes with tutorials and analysis tools for computing the privacy guarantees provided.

[TensorFlow Federated (TFF)](https://github.com/tensorflow/federated) is an open-source framework for machine learning and other computations on decentralized data. TFF has been developed to facilitate open research and experimentation with [Federated Learning (FL)](https://ai.googleblog.com/2017/04/federated-learning-collaborative.html), an approach to machine learning where a shared global model is trained across many participating clients that keep their training data locally.

[Privacy on Beam](https://github.com/google/differential-privacy/tree/main/privacy-on-beam) is an end-to-end differential privacy solution built on [Apache Beam](https://beam.apache.org/documentation/). It is intended to be usable by all developers, regardless of their differential privacy expertise.

[PyDP](https://github.com/OpenMined/PyDP) is a Python wrapper for Google's Differential Privacy project.

[PennyLane](https://pennylane.ai) is a cross-platform Python library for [differentiable programming](https://en.wikipedia.org/wiki/Differentiable_programming) of quantum computers. By training a quantum computer the same way as a neural network.

[BoTorch](https://botorch.org) is a library for Bayesian Optimization built on PyTorch.

[PyTorch Geometric (PyG)](https://github.com/rusty1s/pytorch_geometric) is a geometric deep learning extension library for [PyTorch](https://pytorch.org/).

[Skorch](https://github.com/skorch-dev/skorch) is a scikit-learn compatible neural network library that wraps PyTorch.

[Diffprivlib](https://github.com/IBM/differential-privacy-library) is the IBM Differential Privacy Library for experimenting with, investigating and developing applications in, differential privacy.

[Opacus](https://opacus.ai/) is a library that enables training PyTorch models with differential privacy. It supports training with minimal code changes required on the client, has little impact on training performance and allows the client to online track the privacy budget expended at any given moment.

[Smart Noise](https://github.com/opendifferentialprivacy/smartnoise-sdk) is a toolkit that uses state-of-the-art differential privacy (DP) techniques to inject noise into data, to prevent disclosure of sensitive information and manage exposure risk.


## Privacy Learning Resources

[Differential Privacy Blog Series by the National Institute of Standards and Technology(NIST)](https://www.nist.gov/itl/applied-cybersecurity/privacy-engineering/collaboration-space/focus-areas/de-id/dp-blog)

[Apple's Differential Privacy Overview](https://www.apple.com/privacy/docs/Differential_Privacy_Overview.pdf)

[Learning with Privacy at Scale with Apple Machine Learning](https://machinelearning.apple.com/research/learning-with-privacy-at-scale)

[Microsoft Research Differential Privacy Overview](https://www.microsoft.com/en-us/research/publication/differential-privacy/)

[Responsible Machine Learning with Microsoft Azure](https://azure.microsoft.com/en-us/services/machine-learning/responsibleml/)

[Responsible AI Resources with Microsoft AI](https://www.microsoft.com/en-us/ai/responsible-ai-resources)

[Preserve data privacy by using differential privacy and the SmartNoise package](https://docs.microsoft.com/en-us/azure/machine-learning/concept-differential-privacy)

[Open Differential Privacy(OpenDP) Initiative by Microsoft and Harvard](https://projects.iq.harvard.edu/opendp)

[Google's Differential Privacy Library](https://github.com/google/differential-privacy)

[Computing Private Statistics with Privacy on Beam from Google Codelabs](https://codelabs.developers.google.com/codelabs/privacy-on-beam/#0)

[Introducing TensorFlow Privacy: Learning with Differential Privacy for Training Data](https://blog.tensorflow.org/2020/06/introducing-new-privacy-testing-library.html)

[TensorFlow Federated: Machine Learning on Decentralized Data](https://www.tensorflow.org/federated/)

[Federated Analytics: Collaborative Data Science without Data Collection](https://ai.googleblog.com/2020/05/federated-analytics-collaborative-data.html)

[Differentially-Private Stochastic Gradient Descent(DP-SGD)](https://github.com/tensorflow/privacy/blob/master/tutorials/walkthrough/README.md)

[Learning Differential Privacy from Harvard University Privacy Tools Project](https://privacytools.seas.harvard.edu/differential-privacy)

[Harvard University Privacy Tools Project Courses & Educational Materials](https://privacytools.seas.harvard.edu/courses-educational-materials)

[The Weaknesses of Differential Privacy course on Coursera](https://www.coursera.org/lecture/data-results/weaknesses-of-differential-privacy-50Y9k)

[The Differential Privacy of Bayesian Inference](https://privacytools.seas.harvard.edu/publications/differential-privacy-bayesian-inference)

[Simultaneous private learning of multiple concepts](https://privacytools.seas.harvard.edu/publications/simultaneous-private-learning-multiple-concepts)

[The Complexity of Computing the Optimal Composition of Differential Privacy](https://privacytools.seas.harvard.edu/publications/complexity-computing-optimal-composition-differential-privacy)

[Order revealing encryption and the hardness of private learning](https://privacytools.seas.harvard.edu/publications/order-revealing-encryption-and-hardness-private-learning)

[SAP HANA data anonymization using SAP Software Solutions](https://www.sap.com/cmp/dg/crm-xt17-ddm-data-anony/index.html)

[SAP HANA Security using their In-Memory Database](https://www.sap.com/products/hana/features/security.html)

[DEFCON Differential Privacy Training Launch](https://opensource.googleblog.com/2020/08/defcon-differential-privacy-training.html)

[Secure and Private AI course on Udacity](https://www.udacity.com/course/secure-and-private-ai--ud185)

[Differential Privacy - Security and Privacy for Big Data - Part 1 course on Coursera](https://www.coursera.org/learn/security-privacy-big-data)

[Differential Privacy - Security and Privacy for Big Data - Part 2 course on Coursera](https://www.coursera.org/learn/security-privacy-big-data-protection)

[Certified Ethical Emerging Technologist Professional Certificate course on Coursera](https://www.coursera.org/professional-certificates/certified-ethical-emerging-technologist)


# Cloud Native Development
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/90199045-6a7ba400-dd88-11ea-96d6-81b90d370946.png">
</p>

## Cloud Native Learning Resources

[CNCF Cloud Native Interactive Landscape](https://landscape.cncf.io/)

[Build Cloud-Native applications in Microsoft Azure](https://azure.microsoft.com/en-us/overview/cloudnative/)

[Cloud-Native application development for Google Cloud](https://cloud.google.com/solutions/cloud-native-app-development?hl=he)

[Cloud-Native development for Amazon Web Services](https://aws.amazon.com/blogs/apn/journey-to-being-cloud-native-how-and-where-should-you-start/)

[Cloud Native Applications with VMware Tanzu](https://tanzu.vmware.com/cloud-native)

[Cloud Native Computing Foundation Training and Certification Program](https://www.cncf.io/certification/training/)

[Cloud Foundry Developer Training and Certification Program](https://www.cloudfoundry.org/get-started/)

[Cloud-Native Architecture Course on Pluralsight](https://www.pluralsight.com/courses/cloud-native-architecture-big-picture)

[AWS Fundamentals: Going Cloud-Native on Coursera](https://www.coursera.org/learn/aws-fundamentals-going-cloud-native)

[Developing Cloud-Native Apps w/ Microservices Architectures course on Udemy](https://www.udemy.com/course/developing-cloud-native-applications-microservices-architectures/)

[How load balancing works for cloud native applications with Azure Application Gateway on Linkedin Learning](https://www.linkedin.com/learning/azure-for-developers-optimize-with-azure-application-gateway/how-load-balancing-works-for-cloud-native-applications)

[Developing Cloud Native Applications course on edX](https://www.edx.org/course/developing-cloud-native-applications)

[Cloud Native courses from IBM](https://www.ibm.com/cloud/learn/cloud-native)


<h1 align="center">
 <img src="https://user-images.githubusercontent.com/45159366/110991307-55202580-8329-11eb-9de4-31aba0a2daff.png">
  <br />
  Cloud Native Architecture
</h1>

## DevOps

**Application Framework**

[Spring Boot](https://spring.io/projects/spring-boot) is an open-source micro framework maintained by Pivotal, which was acquired by VMware in 2019. It provides Java developers with a platform to get started with an auto configurable production-grade Spring application.

[Apache Mesos](http://mesos.apache.org/) is a cluster manager that provides efficient resource isolation and sharing across distributed applications, or frameworks. It can run Hadoop, Jenkins, Spark, Aurora, and other frameworks on a dynamically shared pool of nodes.

[Apache Spark](https://spark.apache.org/) is a unified analytics engine for big data processing, with built-in modules for streaming, SQL, machine learning and graph processing.

[Apache Hadoop](http://hadoop.apache.org/) is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models. It is designed to scale up from single servers to thousands of machines, each offering local computation and storage. Rather than rely on hardware to deliver high-availability, the library itself is designed to detect and handle failures at the application layer, so delivering a highly-available service on top of a cluster of computers, each of which may be prone to failures.

**Runtime Platform**

[BOSH](https://www.cloudfoundry.org/bosh/) is a tool that prepares your infrastructure for what needs to be managed. BOSH espouses software engineering best practices, such as continuous delivery, by making it easy to create software releases that automatically update complex distributed systems with simple commands.Due to the flexibility and power of BOSH, Google and VMware made it the heart of the Kubo project, now called the Cloud Foundry Container Runtime, based on Kubernetes.

**Infrastructure Automatation**

[Maven](https://maven.apache.org/) is a build automation tool used primarily for Java projects. Maven can also be used to build and manage projects written in C#, Ruby, Scala, and other languages. The Maven project is hosted by the Apache Software Foundation.

[Gradle](https://gradle.org/) is an open-source build-automation system that builds upon the concepts of Apache Ant and Apache Maven and introduces a Groovy-based domain-specific language instead of the XML form used by Apache Maven for declaring the project configuration.

[Chef](https://www.chef.io/) is an effortless Infrastructure Suite offers visibility into security and compliance status across all infrastructure and makes it easy to detect and correct issues long before they reach production.

[Puppet](https://puppet.com/) is an open source tool that makes continuous integration and delivery of your software on traditional or containerized infrastructure easy by pulling together all your existing tools and giving you flexibility to deploy your way.

[Ansible](https://www.ansible.com/) is an open-source software provisioning, configuration management, and application-deployment tool. It runs on many Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows.

[Salt](https://www.saltstack.com/) is Python-based, open-source software for event-driven IT automation, remote task execution, and configuration management. Supporting the "Infrastructure as Code" approach to data center system and network deployment and management, configuration automation, SecOps orchestration, vulnerability remediation, and hybrid cloud control.

[Terraform](https://www.terraform.io/) is an open-source infrastructure as code software tool created by HashiCorp.It enables users to define and provision a datacenter infrastructure using a high-level configuration language known as Hashicorp Configuration Language (HCL), or optionally JSON.

**Cloud Infrastructure**

[Amazon web service(AWS)](https://aws.amazon.com) is a platform that offers flexible, reliable, scalable, easy-to-use and cost-effective cloud computing solutions. The AWS platform is developed with a combination of infrastructure as a service (IaaS), platform as a service (PaaS) and packaged software as a service (SaaS) offerings.

[Microsoft Azure](https://azure.microsoft.com/en-us/) is a cloud computing service created by Microsoft for building, testing, deploying, and managing applications and services through Microsoft-managed data centers.

[Azure DevOps](https://azure.microsoft.com/en-us/services/devops/?nav=min) is a set of services for teams to share code, track work, and ship software; CLIs Build, deploy, diagnose, and manage multi-platform, scalable apps and services; Azure Pipelines Continuously build, test, and deploy to any platform and cloud; Azure Lab Services Set up labs for classrooms, trials, development and testing, and other scenarios.

[Azure Draft](https://draft.sh/) is a tool for developers to create cloud-native applications on Kubernetes.

[Google Cloud Platform](https://cloud.google.com/) integrates industry-leading tools(data management, hybrid & multi-cloud, and AI & ML) with Cloud Storage for enhanced support with everything from security and data transfer, to data backup and archive. Expand all . Backup, archival, and disaster recovery. Along with File systems and gateways.

[OpenStack](https://www.openstack.org/) is a free and open-source software platform for cloud computing, mostly deployed as infrastructure-as-a-service that controls large pools of compute, storage, and networking resources throughout a datacenter, managed through a dashboard or via the OpenStack API. OpenStack works with popular enterprise and open source technologies making it ideal for heterogeneous infrastructure.

[Cloud Foundry](https://www.cloudfoundry.org/) is an open source, multi cloud application platform as a service that makes it faster and easier to build, test, deploy and scale applications, providing a choice of clouds, developer frameworks, and application services. It is an open source project and is available through a variety of private cloud distributions and public cloud instances.


## Continuous Integration/Continuous Delivery

[Bamboo](https://www.atlassian.com/software/bamboo) is a continuous integration (CI) server that can be used to automate the release management for a software application, creating a continuous delivery pipeline.

[Drone](https://drone.io/) is a Continuous Delivery system built on container technology. Drone uses a simple YAML configuration file, a superset of docker-compose, to define and execute Pipelines inside Docker containers.

[Travis CI](https://travis-ci.org/) is a hosted continuous integration service used to build and test software projects hosted at GitHub.

[Circle CI](https://circleci.com/) is a continuous integration and continuous delivery platform that helps software teams work smarter, faster.

[Team City](https://www.jetbrains.com/teamcity/) is a build management and continuous integration server from JetBrains.

[Shippable](https://www.shippable.com/) simplifies DevOps and makes it systematic with an Assembly Line platform that is heterogeneous, flexible, and provides complete visibility across your DevOps workflows.

[Spinnaker](https://www.spinnaker.io/) is an open source, multi-cloud continuous delivery platform for releasing software changes with high velocity and confidence.

[Prow](https://jenkins-x.io/docs/reference/components/prow/) is a Kubernetes based CI/CD system. Jobs can be triggered by various types of events and report their status to many different services. In addition to job execution, Prow provides GitHub automation in the form of policy enforcement, chat-ops via /foo style commands, and automatic PR merging. Prow has a microservice architecture implemented as a collection of container images that run as Kubernetes deployments.

## Microservices

[AWS ECS](https://aws.amazon.com/ecs/) is a highly scalable, high-performance container orchestration service that supports Docker containers and allows you to easily run and scale containerized applications on AWS. Amazon ECS eliminates the need for you to install and operate your own container orchestration software, manage and scale a cluster of virtual machines, or schedule containers on those virtual machines.

[AWS CodeBuild](https://aws.amazon.com/codebuild/) is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy. With CodeBuild, you don't need to provision, manage, and scale your own build servers.

[CFEngine](https://cfengine.com/) is an open-source configuration management system, written by Mark Burgess.Its primary function is to provide automated configuration and maintenance of large-scale computer systems, including the unified management of servers, desktops, consumer and industrial devices, embedded networked devices, mobile smartphones, and tablet computers.

[Octpus Deploy](https://octopus.com/) is the deployment automation server for your entire team, designed to make it easy to orchestrate releases and deploy applications, whether on-premises or in the cloud.

[AWS CodeDeploy](https://aws.amazon.com/codedeploy/) is a fully managed deployment service that automates software deployments to a variety of compute services such as Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers. AWS CodeDeploy makes it easier for you to rapidly release new features, helps you avoid downtime during application deployment, and handles the complexity of updating your applications.

[AWS Lambda](https://aws.amazon.com/lambda/) is an event-driven, serverless computing platform provided by Amazon as a part of the Amazon Web Services. It is a computing service that runs code in response to events and automatically manages the computing resources required by that code.

[Traefik](https://traefik.io/traefik/) is an open-source Edge Router that makes publishing your services a fun and easy experience. It receives requests on behalf of your system and finds out which components are responsible for handling them. What sets Traefik apart, besides its many features, is that it automatically discovers the right configuration for your services.

## Containers

[Kubernetes](https://kubernetes.io/) is an open-source container-orchestration system for automating application deployment, scaling, and management. It was originally designed by Google, and is now maintained by the Cloud Native Computing Foundation.

[Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine/) is a managed, production-ready environment for deploying containerized applications.

[OpenShift](https://www.openshift.com/) is focused on security at every level of the container stack and throughout the application lifecycle. It includes long-term, enterprise support from one of the leading Kubernetes contributors and open source software companies.

[Rancher](https://rancher.com/) is a complete software stack for teams adopting containers. It addresses the operational and security challenges of managing multiple Kubernetes clusters, while providing DevOps teams with integrated tools for running containerized workloads.

[Docker](https://www.docker.com/) is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels. All containers are run by a single operating-system kernel and are thus more lightweight than virtual machines.

[Rook](https://rook.io/) is an open source cloud-native storage orchestrator for Kubernetes that turns distributed storage systems into self-managing, self-scaling, self-healing storage services. It automates the tasks of a storage administrator: deployment, bootstrapping, configuration, provisioning, scaling, upgrading, migration, disaster recovery, monitoring, and resource management.

[Podman(the POD MANager)](https://github.com/containers/podman) is a tool for managing [OCI](https://opencontainers.org/) containers and pods.

[Rkt](https://coreos.com/rkt/) is a pod-native container engine for Linux. It is composable, secure, and built on standards.


# DevOps Development
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/96352525-abd64b80-1078-11eb-95c8-e29d4c592bec.png">
</p>


## DevOps Tools

[GitHub](https://github.com/) provides hosting for software development version control using Git. It offers all of the distributed version control and source code management functionality of Git as well as adding its own features. It provides access control and several collaboration features such as bug tracking, feature requests, task management, and wikis for every project.

[GitHub Codespaces](https://docs.github.com/en/free-pro-team@latest/github/developing-online-with-codespaces) is an integrated development environment(IDE) on GitHub. That allows developers to develop entirely in the cloud using Visual Studio and Visual Studio Code.

[GitHub Actions](https://docs.github.com/en/actions) will automate, customize, and execute your software development workflows right in your repository with GitHub Actions. You can discover, create, and share actions to perform any job you'd like, including CI/CD, and combine actions in a completely customized workflow.[GitHub Actions for Azure](https://docs.microsoft.com/en-us/azure/developer/github/github-actions) you can create workflows that you can set up in your repository to build, test, package, release and deploy to Azure.Learn more about all other integrations with Azure.

[GitLab](https://about.gitlab.com/) is a web-based DevOps lifecycle tool that provides a Git-repository manager providing wiki, issue-tracking and CI/CD pipeline features, using an open-source license, developed by GitLab Inc.

[Jenkins](https://jenkins.io/) is a free and open source automation server. Jenkins helps to automate the non-human part of the software development process, with continuous integration and facilitating technical aspects of continuous delivery.

[Bitbucket](https://bitbucket.org/) is a web-based version control repository hosting service owned by Atlassian, for source code and development projects that use either Mercurial or Git revision control systems. Bitbucket offers both commercial plans and free accounts. It offers free accounts with an unlimited number of private repositories. Bitbucket integrates with other Atlassian software like Jira, HipChat, Confluence and Bamboo.

[Bamboo](https://www.atlassian.com/software/bamboo) is a continuous integration (CI) server that can be used to automate the release management for a software application, creating a continuous delivery pipeline.

[Codecov](https://codecov.io/) is the leading, dedicated code coverage solution. It provides highly integrated tools to group, merge, archive and compare coverage reports. Whether your team is comparing changes in a pull request or reviewing a single commit, Codecov will improve the code review workflow and quality.

[Drone](https://drone.io/) is a Continuous Delivery system built on container technology. Drone uses a simple YAML configuration file, a superset of docker-compose, to define and execute Pipelines inside Docker containers.

[Travis CI](https://travis-ci.org/) is a hosted continuous integration service used to build and test software projects hosted at GitHub.

[Circle CI](https://circleci.com/) is a continuous integration and continuous delivery platform that helps software teams work smarter, faster.

[Zuul-CI](https://zuul-ci.org/index.html) is a program that drives continuous integration, delivery, and deployment systems with a focus on project gating and interrelated projects. Using the same [Ansible playbooks](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html) to deploy your system and run your tests.

[Artifactory](https://jfrog.com/artifactory/) is a Universal Artifact Repository Manager developed by JFrog. It supports all major packages, enterprise ready security, clustered, HA, Docker registry, multi-site replication and scalable.

[Azure DevOps](https://azure.microsoft.com/en-us/services/devops/?nav=min) is a set of services for teams to share code, track work, and ship software; CLIs Build, deploy, diagnose, and manage multi-platform, scalable apps and services; Azure Pipelines Continuously build, test, and deploy to any platform and cloud; Azure Lab Services Set up labs for classrooms, trials, development and testing, and other scenarios.

[Team City](https://www.jetbrains.com/teamcity/) is a build management and continuous integration server from JetBrains.

[Shippable](https://www.shippable.com/) simplifies DevOps and makes it systematic with an Assembly Line platform that is heterogeneous, flexible, and provides complete visibility across your DevOps workflows.

[Spinnaker](https://www.spinnaker.io/) is an open source, multi-cloud continuous delivery platform for releasing software changes with high velocity and confidence.

[AWS CodeBuild](https://aws.amazon.com/codebuild/) is a fully managed continuous integration service that compiles source code, runs tests, and produces software packages that are ready to deploy. With CodeBuild, you don't need to provision, manage, and scale your own build servers.

[Selenium](https://www.seleniumhq.org/) is a free (open source) automated testing suite for web applications across different browsers and platforms.

[Cucumber](https://cucumber.io/) is a tool based on Behavior Driven Development (BDD) framework which is used to write acceptance tests for the web application. It allows automation of functional validation in easily readable and understandable format (like plain English) to Business Analysts, Developers, and Testers.

[JUnit](https://junit.org/junit5/) is a unit testing framework for the Java programming language.

[Mocha](https://mochajs.org/) is a JavaScript test framework for Node.js programs, featuring browser support, asynchronous testing, test coverage reports, and use of any assertion library.

[Karma](https://karma-runner.github.io/latest/index.html) is a simple tool that allows you to execute JavaScript code in multiple real browsers.

[Jasmine](https://jasmine.github.io/) is an open source testing framework for JavaScript. It aims to run on any JavaScript-enabled platform, to not intrude on the application nor the IDE, and to have easy-to-read syntax.

[Maven](https://maven.apache.org/) is a build automation tool used primarily for Java projects. Maven can also be used to build and manage projects written in C#, Ruby, Scala, and other languages. The Maven project is hosted by the Apache Software Foundation.

[Gradle](https://gradle.org/) is an open-source build-automation system that builds upon the concepts of Apache Ant and Apache Maven and introduces a Groovy-based domain-specific language instead of the XML form used by Apache Maven for declaring the project configuration.

[Chef](https://www.chef.io/) is an effortless Infrastructure Suite offers visibility into security and compliance status across all infrastructure and makes it easy to detect and correct issues long before they reach production.

[Puppet](https://puppet.com/) is an open source tool that makes continuous integration and delivery of your software on traditional or containerized infrastructure easy by pulling together all your existing tools and giving you flexibility to deploy your way.

[Ansible](https://www.ansible.com/) is an open-source software provisioning, configuration management, and application-deployment tool. It runs on many Unix-like systems, and can configure both Unix-like systems as well as Microsoft Windows.

[KubeInit](https://github.com/kubeinit/kubeinit) provides Ansible playbooks and roles for the deployment and configuration of multiple Kubernetes distributions.

[Salt](https://www.saltstack.com/) is Python-based, open-source software for event-driven IT automation, remote task execution, and configuration management. Supporting the "Infrastructure as Code" approach to data center system and network deployment and management, configuration automation, SecOps orchestration, vulnerability remediation, and hybrid cloud control.

[Terraform](https://www.terraform.io/) is an open-source infrastructure as code software tool created by HashiCorp.It enables users to define and provision a datacenter infrastructure using a high-level configuration language known as Hashicorp Configuration Language (HCL), or optionally JSON.

[Consul](https://www.consul.io) is a service networking solution to connect and secure services across any runtime platform and public or private cloud.

[Packer](https://www.packer.io/) is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

[Nomad](https://www.nomadproject.io/) is a highly available, distributed, data-center aware cluster and application scheduler designed to support the modern datacenter with support for long-running services, batch jobs, and much more.

[Vagrant](https://www.vagrantup.com/) is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time and increases production parity.

[Vault](https://www.hashicorp.com/products/vault/) is a tool for securely accessing secrets. A secret is anything that you want to tightly control access to, such as API keys, passwords, certificates, and more. Vault provides a unified interface to any secret, while providing tight access control and recording a detailed audit log.

[CFEngine](https://cfengine.com/) is an open-source configuration management system, written by Mark Burgess.Its primary function is to provide automated configuration and maintenance of large-scale computer systems, including the unified management of servers, desktops, consumer and industrial devices, embedded networked devices, mobile smartphones, and tablet computers.

[Octpus Deploy](https://octopus.com/) is the deployment automation server for your entire team, designed to make it easy to orchestrate releases and deploy applications, whether on-premises or in the cloud.

[AWS CodeDeploy](https://aws.amazon.com/codedeploy/) is a fully managed deployment service that automates software deployments to a variety of compute services such as Amazon EC2, AWS Fargate, AWS Lambda, and your on-premises servers. AWS CodeDeploy makes it easier for you to rapidly release new features, helps you avoid downtime during application deployment, and handles the complexity of updating your applications.

[Kubernetes](https://kubernetes.io/) is an open-source container-orchestration system for automating application deployment, scaling, and management. It was originally designed by Google, and is now maintained by the Cloud Native Computing Foundation.

[Docker](https://www.docker.com/) is a set of platform as a service products that use OS-level virtualization to deliver software in packages called containers. Containers are isolated from one another and bundle their own software, libraries and configuration files; they can communicate with each other through well-defined channels. All containers are run by a single operating-system kernel and are thus more lightweight than virtual machines.

[PowerShell/PowerShell Core](https://docs.microsoft.com/en-us/powershell/) is a cross-platform (Windows, Linux, and macOS) automation and configuration tool/framework that works well with your existing tools and is optimized for dealing with structured data (e.g. JSON, CSV, XML, etc.), REST APIs, and object models. It includes a command-line shell, an associated scripting language and a framework for processing cmdlets.

[Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/) creates virtual machines on Windows 10. Hyper-V can be enabled in many ways including using the Windows 10 control panel, PowerShell or using the Deployment Imaging Servicing and Management tool (DISM).

[Cloud Hypervisor](https://github.com/cloud-hypervisor/cloud-hypervisor) is an open source Virtual Machine Monitor (VMM) that runs on top of [KVM](https://www.kernel.org/doc/Documentation/virtual/kvm/api.txt). The project focuses on exclusively running modern, cloud workloads, on top of a limited set of hardware architectures and platforms. Cloud workloads refers to those that are usually run by customers inside a cloud provider. Cloud Hypervisor is implemented in [Rust](https://www.rust-lang.org/) and is based on the [rust-vmm](https://github.com/rust-vmm) crates.

[VMware vSphere Hypervisor](https://www.vmware.com/products/vsphere-hypervisor.html) is a bare-metal hypervisor that virtualizes servers; allowing you to consolidate your applications while saving time and money managing your IT infrastructure.

[VMware vSphere](https://www.vmware.com/products/vsphere.html) is the industry-leading compute virtualization platform, and your first step to application modernization. It has been rearchitected with native Kubernetes to allow customers to modernize the 70 million+ workloads now running on vSphere.

[VMware Tanzu](https://tanzu.vmware.com/tanzu) is a centralized management platform for consistently operating and securing your Kubernetes infrastructure and modern applications across multiple teams and private/public clouds.

[Rancher](https://rancher.com/) is a complete software stack for teams adopting containers. It addresses the operational and security challenges of managing multiple Kubernetes clusters, while providing DevOps teams with integrated tools for running containerized workloads.

[K3s](https://github.com/rancher/k3s) is a highly available, certified Kubernetes distribution designed for production workloads in unattended, resource-constrained, remote locations or inside IoT appliances.

[Rook](https://rook.io/) is an open source cloud-native storage orchestrator for Kubernetes that turns distributed storage systems into self-managing, self-scaling, self-healing storage services. It automates the tasks of a storage administrator: deployment, bootstrapping, configuration, provisioning, scaling, upgrading, migration, disaster recovery, monitoring, and resource management.

[Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine/) is a managed, production-ready environment for deploying containerized applications.

[Anthos](https://cloud.google.com/anthos/docs/concepts/overview) is a modern application management platform that provides a consistent development and operations experience for cloud and on-premises environments.

[AWS ECS](https://aws.amazon.com/ecs/) is a highly scalable, high-performance container orchestration service that supports Docker containers and allows you to easily run and scale containerized applications on AWS. Amazon ECS eliminates the need for you to install and operate your own container orchestration software, manage and scale a cluster of virtual machines, or schedule containers on those virtual machines.

[Apache Mesos](http://mesos.apache.org/) is a cluster manager that provides efficient resource isolation and sharing across distributed applications, or frameworks. It can run Hadoop, Jenkins, Spark, Aurora, and other frameworks on a dynamically shared pool of nodes.

[Apache Spark](https://spark.apache.org/) is a unified analytics engine for big data processing, with built-in modules for streaming, SQL, machine learning and graph processing.

[Apache Hadoop](http://hadoop.apache.org/) is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models. It is designed to scale up from single servers to thousands of machines, each offering local computation and storage. Rather than rely on hardware to deliver high-availability, the library itself is designed to detect and handle failures at the application layer, so delivering a highly-available service on top of a cluster of computers, each of which may be prone to failures.

[Microsoft Azure](https://azure.microsoft.com/en-us/) is a cloud computing service created by Microsoft for building, testing, deploying, and managing applications and services through Microsoft-managed data centers.

[Azure Functions](https://azure.microsoft.com/en-us/services/functions/) is a solution for easily running small pieces of code, or "functions," in the cloud. You can write just the code you need for the problem at hand, without worrying about a whole application or the infrastructure to run it.

[Rkt](https://coreos.com/rkt/) is a pod-native container engine for Linux. It is composable, secure, and built on standards.

[AWS Lambda](https://aws.amazon.com/lambda/) is an event-driven, serverless computing platform provided by Amazon as a part of the Amazon Web Services. It is a computing service that runs code in response to events and automatically manages the computing resources required by that code.

[Helm](https://helm.sh/) is the Kubernetes Package Manager.

[Kubespray](https://kubespray.io/) is a tool that combines Kubernetes and Ansible to easily install Kubernetes clusters that can be deployed on [AWS](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/aws.md), GCE, [Azure](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/azure.md), [OpenStack](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/openstack.md), [vSphere](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/vsphere.md), [Packet](https://github.com/kubernetes-sigs/kubespray/blob/master/docs/packet.md) (bare metal), Oracle Cloud Infrastructure (Experimental), or Baremetal

[Red Hat OpenShift](https://www.openshift.com/) is focused on security at every level of the container stack and throughout the application lifecycle. It includes long-term, enterprise support from one of the leading Kubernetes contributors and open source software companies.

[OpenShift Hive](https://github.com/openshift/hive) is an operator which runs as a service on top of Kubernetes/OpenShift. The Hive service can be used to provision and perform initial configuration of OpenShift 4 clusters.

[OKD](https://okd.io/) is a community distribution of Kubernetes optimized for continuous application development and multi-tenant deployment. OKD adds developer and operations-centric tools on top of Kubernetes to enable rapid application development, easy deployment and scaling, and long-term lifecycle maintenance for small and large teams.

[Odo](https://odo.dev/) is a fast, iterative, and straightforward CLI tool for developers who write, build, and deploy applications on Kubernetes and OpenShift.

[Kata Operator](https://github.com/openshift/kata-operator) is an operator to perform lifecycle management (install/upgrade/uninstall) of [Kata Runtime](https://katacontainers.io/) on Openshift as well as Kubernetes cluster.

[Knative](https://knative.dev/) is a Kubernetes-based platform to build, deploy, and manage modern serverless workloads. Knative takes care of the operational overhead details of networking, autoscaling (even to zero), and revision tracking.

[Etcd](https://etcd.io/) is a distributed key-value store that provides a reliable way to store data that needs to be accessed by a distributed system or cluster of machines. Etcd is used as the backend for service discovery and stores cluster state and configuration for Kubernetes.

[OpenStack](https://www.openstack.org/) is a free and open-source software platform for cloud computing, mostly deployed as infrastructure-as-a-service that controls large pools of compute, storage, and networking resources throughout a datacenter, managed through a dashboard or via the OpenStack API. OpenStack works with popular enterprise and open source technologies making it ideal for heterogeneous infrastructure.

[Cloud Foundry](https://www.cloudfoundry.org/) is an open source, multi cloud application platform as a service that makes it faster and easier to build, test, deploy and scale applications, providing a choice of clouds, developer frameworks, and application services. It is an open source project and is available through a variety of private cloud distributions and public cloud instances.

[Splunk](https://www.splunk.com/) software is used for searching, monitoring, and analyzing machine-generated big data, via a Web-style interface.

[Prometheus](https://prometheus.io/) is a free software application used for event monitoring and alerting. It records real-time metrics in a time series database (allowing for high dimensionality) built using a HTTP pull model, with flexible queries and real-time alerting.

[Loki](https://grafana.com/oss/loki/) is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus. It is designed to be very cost effective and easy to operate. It does not index the contents of the logs, but rather a set of labels for each log stream.

[Thanos](https://thanos.io/) is a set of components that can be composed into a highly available metric system with unlimited storage capacity, which can be added seamlessly on top of existing Prometheus deployments.

[Container Storage Interface (CSI)](https://www.architecting.it/blog/container-storage-interface/) is an API that lets container orchestration platforms like Kubernetes seamlessly communicate with stored data via a plug-in.

[OpenEBS](https://openebs.io/) is a Kubernetes-based tool to create stateful applications using Container Attached Storage.

[ElasticSearch](https://www.elastic.co/) is a search engine based on the Lucene library. It provides a distributed, multitenant-capable full-text search engine with an HTTP web interface and schema-free JSON documents. Elasticsearch is developed in Java.

[Logstash](https://www.elastic.co/products/logstash) is a tool for managing events and logs. When used generically, the term encompasses a larger system of log collection, processing, storage and searching activities.

[Kibana](https://www.elastic.co/products/kibana) is an open source data visualization plugin for Elasticsearch. It provides visualization capabilities on top of the content indexed on an Elasticsearch cluster. Users can create bar, line and scatter plots, or pie charts and maps on top of large volumes of data.

[New Relic](https://newrelic.com/) is a SaaS-based monitoring tool that fully supports the way DevOps teams work in the modern enterprise by streamlining your workflows with today's collaboration software and orchestration tools like Puppet, Chef, and Ansible.

[Nagios](https://www.nagios.org/) is a free and open source computer-software application that monitors systems, networks and infrastructure. Nagios offers monitoring and alerting services for servers, switches, applications and services. It alerts users when things go wrong and alerts them a second time when the problem has been resolved.

[SonarQube](https://www.sonarqube.org/) is an open-source platform developed by SonarSource for continuous inspection of code quality to perform automatic reviews with static analysis of code to detect bugs, code smells, and security vulnerabilities on 20+ programming languages.

[Genie](https://netflix.github.io/genie) is a federated job orchestration engine developed by Netflix. Genie provides REST APIs to run a variety of big data jobs like Hadoop, Pig, Hive, Spark, Presto, Sqoop and more. It also provides APIs for managing the metadata of many distributed processing clusters and the commands and applications which run on them.

[Inviso](https://github.com/Netflix/inviso) is a lightweight tool that provides the ability to search for Hadoop jobs, visualize the performance, and view cluster utilization.

[Fenzo](https://github.com/Netflix/Fenzo) is a scheduler Java library for Apache Mesos frameworks that supports plugins for scheduling optimizations and facilitates cluster autoscaling.

[Dynomite](https://github.com/Netflix/dynomite) is a thin, distributed dynamo layer for different storage engines and protocols, which includes [Redis](http://redis.io/) and [Memcached](http://www.memcached.org/). Dynomite supports multi-datacenter replication and is designed for High Availability(HA).

[Dyno](https://github.com/Netflix/dynomite) is a tool that is used to scale a Java client application utilizing [Dynomite](https://github.com/Netflix/dynomite).

[Raigad](https://github.com/Netflix/Raigad) is a process/tool that runs alongside Elasticsearch to automate backup/recovery, Deployments and Centralized Configuration management.

[Priam](https://github.com/Netflix/Priam) is a process/tool that runs alongside Apache Cassandra to automate backup/recovery, Deployments and Centralized Configuration management.

[Chaos Monkey](https://github.com/Netflix/chaosmonkey) is a resiliency tool  used to randomly terminates virtual machine instances and containers that run inside of your production environment. Chaos Monkey should work with any backend that [Spinnaker](http://www.spinnaker.io/) supports (AWS, Google Compute Engine, Microsoft Azure, Kubernetes, and Cloud Foundry).

[Falcor](https://netflix.github.io/falcor/) is a JavaScript library for efficient data fetching. Falcor lets you represent all your remote data sources as a single domain model via a virtual JSON graph, whether in memory on the client or over the network on the server.

[Restify](https://github.com/restify/node-restify) is a framework, utilizing [connect](https://github.com/senchalabs/connect) style middleware for building REST APIs.

[Traefik](https://traefik.io/traefik/) is an open source Edge Router that makes publishing your services a fun and easy experience. It receives requests on behalf of your system and finds out which components are responsible for handling them. What sets Traefik apart, besides its many features, is that it automatically discovers the right configuration for your services.

[Jira](https://www.atlassian.com/software/jira) is a proprietary issue tracking product developed by Atlassian that allows bug tracking and agile project management.

[Pivotal Tracker](https://www.pivotaltracker.com/) is the agile project management tool of choice for developers around the world for real-time collaboration around a shared, prioritized backlog.

[Trello](https://trello.com/) is a web-based Kanban-style list-making application that gives you perspective over all your projects, at work and at home.

[Microsoft Teams](https://teams.microsoft.com/start) is the hub for team collaboration in Office 365 that integrates the people, content, and tools your team needs to be more engaged and effective.

[Slack](https://slack.com/) is a cloud-based proprietary instant messaging platform developed by Slack Technologies.

[OpsGenie](https://www.opsgenie.com/) is a cloud-based service for dev & ops teams, providing reliable alerts, on-call schedule management and escalations. OpsGenie integrates with monitoring tools & services, ensures the right people are notified.

[Pagerduty](https://www.pagerduty.com/) automates processes built on best practices, allowing you to focus on higher value parts of incident response. Granular and scalable permissions enable teams to administer and operate independently while controlling visibility.

[Veracode](https://www.veracode.com/) is a leading provider of enterprise-class application security, seamlessly integrating agile security solutions for organizations around the globe. In addition to application security services and secure devops services, Veracode provides a full security assessment to ensure your website and applications are secure, and ensures full enterprise data protection.

## DevOps Learning Resources

[DevOps Engineering on AWS from AWS Training](https://aws.amazon.com/training/course-descriptions/devops-engineering/)

[AWS Certified DevOps Engineer - Professional from A Cloud Guru](https://acloud.guru/learn/aws-certified-devops-engineer-professional)

[Microsoft Certified: DevOps Engineer Expert Cert.](https://docs.microsoft.com/en-us/learn/certifications/devops-engineer)

[Introduction to Azure DevOps from A Cloud Guru](https://acloud.guru/learn/introduction-to-azure-devops)

[Architecting with Google Compute Engine](https://google.qwiklabs.com/courses/1421?utm_source=gcp_training&utm_medium=website&utm_campaign=cgc)

[Architecting with Google Kubernetes Engine in Google Cloud](https://google.qwiklabs.com/courses/1232?utm_source=gcp_training&utm_medium=website&utm_campaign=cgc)

[VMware Training and Certification Program](https://www.vmware.com/education-services/certification.html)

[Cloudera Certification Program](https://www.cloudera.com/about/training/certification.html)

[Salesforce Certification Program](https://trailhead.salesforce.com/credentials/administratoroverview)

[Salesforce Superbadges](https://trailhead.salesforce.com/superbadges)

[Red Hat Training and Certification Program](https://www.redhat.com/en/services/training-and-certification)

[Linux Foundation Training and Certification Program](https://training.linuxfoundation.org/certification/)

[Linux Professional Institute(LPI) Training and Certification](https://www.lpi.org)

[Learn DevOps with Online Courses and Lessons from edX](https://www.edx.org/learn/devops)

[Top DevOps Courses Online from Udemy](https://www.udemy.com/topic/devops/)

[Devops Courses from Coursera](https://www.coursera.org/courses?languages=en&query=devops)


# Networking
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/82833053-d1687b80-9e71-11ea-8c6d-074100f2f54b.png">
  <br />
</p>

## Networking Learning Resources

[AWS Certified Security - Specialty Certification](https://aws.amazon.com/certification/certified-security-specialty/)

[Microsoft Certified: Azure Security Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer)

[Google Cloud Certified Professional Cloud Security Engineer](https://cloud.google.com/certification/cloud-security-engineer)

[Cisco Security Certifications](https://www.cisco.com/c/en/us/training-events/training-certifications/certifications/security.html)

[The Red Hat Certified Specialist in Security: Linux](https://www.redhat.com/en/services/training/ex415-red-hat-certified-specialist-security-linux-exam)

[Linux Professional Institute LPIC-3 Enterprise Security Certification](https://www.lpi.org/our-certifications/lpic-3-303-overview)

[Cybersecurity Training and Courses from IBM Skills](https://www.ibm.com/skills/topics/cybersecurity/)

[Cybersecurity Courses and Certifications by Offensive Security](https://www.offensive-security.com/courses-and-certifications/)

[Citrix Certified Associate – Networking(CCA-N)](http://training.citrix.com/cms/index.php/certification/networking/)

[Citrix Certified Professional – Virtualization(CCP-V)](https://www.globalknowledge.com/us-en/training/certification-prep/brands/citrix/section/virtualization/citrix-certified-professional-virtualization-ccp-v/)

[CCNP Routing and Switching](https://learningnetwork.cisco.com/s/ccnp-enterprise)

[Certified Information Security Manager(CISM)](https://www.isaca.org/credentialing/cism)

[Wireshark Certified Network Analyst (WCNA)](https://www.wiresharktraining.com/certification.html)

[Juniper Networks Certification Program Enterprise (JNCP)](https://www.juniper.net/us/en/training/certification/)

[Networking courses and specializations from Coursera](https://www.coursera.org/browse/information-technology/networking)

[Network & Security Courses from Udemy](https://www.udemy.com/courses/it-and-software/network-and-security/)

[Network & Security Courses from edX](https://www.edx.org/learn/cybersecurity)

  ## Tools & Networking Concepts

    • Connection: In networking, a connection refers to pieces of related information that are transferred through a network. This generally infers that a connection is built before the data transfer (by following the procedures laid out in a protocol) and then is deconstructed at the at the end of the data transfer.

    • Packet: A packet is, generally speaking, the most basic unit that is transferred over a network. When communicating over a network, packets are the envelopes that carry your data (in pieces) from one end point to the other.

Packets have a header portion that contains information about the packet including the source and destination, timestamps, network hops. The main portion of a packet contains the actual data being transferred. It is sometimes called the body or the payload.

    • Network Interface: A network interface can refer to any kind of software interface to networking hardware. For instance, if you have two network cards in your computer, you can control and configure each network interface associated with them individually.

A network interface may be associated with a physical device, or it may be a representation of a virtual interface. The "loop-back" device, which is a virtual interface to the local machine, is an example of this.

    • LAN: LAN stands for "local area network". It refers to a network or a portion of a network that is not publicly accessible to the greater internet. A home or office network is an example of a LAN.

    • WAN: WAN stands for "wide area network". It means a network that is much more extensive than a LAN. While WAN is the relevant term to use to describe large, dispersed networks in general, it is usually meant to mean the internet, as a whole.
If an interface is connected to the WAN, it is generally assumed that it is reachable through the internet.

    • Protocol: A protocol is a set of rules and standards that basically define a language that devices can use to communicate. There are a great number of protocols in use extensively in networking, and they are often implemented in different layers.

Some low level protocols are TCP, UDP, IP, and ICMP. Some familiar examples of application layer protocols, built on these lower protocols, are HTTP (for accessing web content), SSH, TLS/SSL, and FTP.

    • Port: A port is an address on a single machine that can be tied to a specific piece of software. It is not a physical interface or location, but it allows your server to be able to communicate using more than one application.

    • Firewall: A firewall is a program that decides whether traffic coming into a server or going out should be allowed. A firewall usually works by creating rules for which type of traffic is acceptable on which ports. Generally, firewalls block ports that are not used by a specific application on a server.

    • NAT: Network address translation is a way to translate requests that are incoming into a routing server to the relevant devices or servers that it knows about in the LAN. This is usually implemented in physical LANs as a way to route requests through one IP address to the necessary backend servers.

    • VPN: Virtual private network is a means of connecting separate LANs through the internet, while maintaining privacy. This is used as a means of connecting remote systems as if they were on a local network, often for security reasons.

## Network Layers

	While networking is often discussed in terms of topology in a horizontal way, between hosts, its implementation is layered in a vertical fashion throughout a computer or network. This means is that there are multiple technologies and protocols that are built on top of each other in order for communication to function more easily. Each successive, higher layer abstracts the raw data a little bit more, and makes it simpler to use for applications and users. It also allows you to leverage lower layers in new ways without having to invest the time and energy to develop the protocols and applications that handle those types of traffic.

	As data is sent out of one machine, it begins at the top of the stack and filters downwards. At the lowest level, actual transmission to another machine takes place. At this point, the data travels back up through the layers of the other computer. Each layer has the ability to add its own "wrapper" around the data that it receives from the adjacent layer, which will help the layers that come after decide what to do with the data when it is passed off.

	One method of talking about the different layers of network communication is the OSI model. OSI stands for Open Systems Interconnect.This model defines seven separate layers. The layers in this model are:

    • Application: The application layer is the layer that the users and user-applications most often interact with. Network communication is discussed in terms of availability of resources, partners to communicate with, and data synchronization.

    • Presentation: The presentation layer is responsible for mapping resources and creating context. It is used to translate lower level networking data into data that applications expect to see.

    • Session: The session layer is a connection handler. It creates, maintains, and destroys connections between nodes in a persistent way.

    • Transport: The transport layer is responsible for handing the layers above it a reliable connection. In this context, reliable refers to the ability to verify that a piece of data was received intact at the other end of the connection. This layer can resend information that has been dropped or corrupted and can acknowledge the receipt of data to remote computers.

    • Network: The network layer is used to route data between different nodes on the network. It uses addresses to be able to tell which computer to send information to. This layer can also break apart larger messages into smaller chunks to be reassembled on the opposite end.

    • Data Link: This layer is implemented as a method of establishing and maintaining reliable links between different nodes or devices on a network using existing physical connections.

    • Physical: The physical layer is responsible for handling the actual physical devices that are used to make a connection. This layer involves the bare software that manages physical connections as well as the hardware itself (like Ethernet).

The TCP/IP model, more commonly known as the Internet protocol suite, is another layering model that is simpler and has been widely adopted.It defines the four separate layers, some of which overlap with the OSI model:

    • Application: In this model, the application layer is responsible for creating and transmitting user data between applications. The applications can be on remote systems, and should appear to operate as if locally to the end user.
The communication takes place between peers network.

    • Transport: The transport layer is responsible for communication between processes. This level of networking utilizes ports to address different services. It can build up unreliable or reliable connections depending on the type of protocol used.

    • Internet: The internet layer is used to transport data from node to node in a network. This layer is aware of the endpoints of the connections, but does not worry about the actual connection needed to get from one place to another. IP addresses are defined in this layer as a way of reaching remote systems in an addressable manner.

    • Link: The link layer implements the actual topology of the local network that allows the internet layer to present an addressable interface. It establishes connections between neighboring nodes to send data.

## Interfaces
Interfaces are networking communication points for your computer. Each interface is associated with a physical or virtual networking device. Typically, your server will have one configurable network interface for each Ethernet or wireless internet card you have. In addition, it will define a virtual network interface called the "loopback" or localhost interface. This is used as an interface to connect applications and processes on a single computer to other applications and processes. You can see this referenced as the "lo" interface in many tools.

## Protocols
Networking works by piggybacks on a number of different protocols on top of each other. In this way, one piece of data can be transmitted using multiple protocols encapsulated within one another.

Media access control is a communications protocol that is used to distinguish specific devices. Each device is supposed to get a unique MAC address during the manufacturing process that differentiates it from every other device on the internet. Addressing hardware by the MAC address allows you to reference a device by a unique value even when the software on top may change the name for that specific device during operation. Media access control is one of the only protocols from the link layer that you are likely to interact with on a regular basis.

The IP protocol is one of the fundamental protocols that allow the internet to work. IP addresses are unique on each network and they allow machines to address each other across a network. It is implemented on the internet layer in the IP/TCP model. Networks can be linked together, but traffic must be routed when crossing network boundaries. This protocol assumes an unreliable network and multiple paths to the same destination that it can dynamically change between. There are a number of different implementations of the protocol. The most common implementation today is IPv4, although IPv6 is growing in popularity as an alternative due to the scarcity of IPv4 addresses available and improvements in the protocols capabilities.

ICMP: internet control message protocol is used to send messages between devices to indicate the availability or error conditions. These packets are used in a variety of network diagnostic tools, such as ping and traceroute. Usually ICMP packets are transmitted when a packet of a different kind meets some kind of a problem. Basically, they are used as a feedback mechanism for network communications.

TCP: Transmission control protocol is implemented in the transport layer of the IP/TCP model and is used to establish reliable connections. TCP is one of the protocols that encapsulates data into packets. It then transfers these to the remote end of the connection using the methods available on the lower layers. On the other end, it can check for errors, request certain pieces to be resent, and reassemble the information into one logical piece to send to the application layer. The protocol builds up a connection prior to data transfer using a system called a three-way handshake. This is a way for the two ends of the communication to acknowledge the request and agree upon a method of ensuring data reliability. After the data has been sent, the connection is torn down using a similar four-way handshake. TCP is the protocol of choice for many of the most popular uses for the internet, including WWW, FTP, SSH, and email. It is safe to say that the internet we know today would not be here without TCP.

UDP: User datagram protocol is a popular companion protocol to TCP and is also implemented in the transport layer. The fundamental difference between UDP and TCP is that UDP offers unreliable data transfer. It does not verify that data has been received on the other end of the connection. This might sound like a bad thing, and for many purposes, it is. However, it is also extremely important for some functions. It’s not required to wait for confirmation that the data was received and forced to resend data, UDP is much faster than TCP. It does not establish a connection with the remote host, it simply fires off the data to that host and doesn't care if it is accepted or not. Since UDP is a simple transaction, it is useful for simple communications like querying for network resources. It also doesn't maintain a state, which makes it great for transmitting data from one machine to many real-time clients. This makes it ideal for VOIP, games, and other applications that cannot afford delays.

HTTP: Hypertext transfer protocol is a protocol defined in the application layer that forms the basis for communication on the web. HTTP defines a number of functions that tell the remote system what you are requesting. For instance, GET, POST, and DELETE all interact with the requested data in a different way.

[JSON Web Token (JWT)](https://jwt.io) is a compact URL-safe means of representing claims to be transferred between two parties. The claims in a JWT are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS).

[OAuth 2.0](https://oauth.net/2/) is an open source authorization framework that enables applications to obtain limited access to user accounts on an HTTP service, such as Amazon, Google, Facebook, Microsoft, Twitter GitHub, and DigitalOcean. It works by delegating user authentication to the service that hosts the user account, and authorizing third-party applications to access the user account.

FTP: File transfer protocol is in the application layer and provides a way of transferring complete files from one host to another. It is inherently insecure, so it is not recommended for any externally facing network unless it is implemented as a public, download-only resource.

DNS: Domain name system is an application layer protocol used to provide a human-friendly naming mechanism for internet resources. It is what ties a domain name to an IP address and allows you to access sites by name in your browser.

SSH: Secure shell is an encrypted protocol implemented in the application layer that can be used to communicate with a remote server in a secure way. Many additional technologies are built around this protocol because of its end-to-end encryption and ubiquity. There are many other protocols that we haven't covered that are equally important. However, this should give you a good overview of some of the fundamental technologies that make the internet and networking possible.

## Virtualization

[KVM (for Kernel-based Virtual Machine)](https://www.linux-kvm.org/page/Main_Page) is a full virtualization solution for Linux on x86 hardware containing virtualization extensions (Intel VT or AMD-V). It consists of a loadable kernel module, kvm.ko, that provides the core virtualization infrastructure and a processor specific module, kvm-intel.ko or kvm-amd.ko.

[QEMU](https://www.qemu.org) is a fast processor emulator using a portable dynamic translator. QEMU emulates a full system, including a processor and various peripherals. It can be used to launch a different Operating System without rebooting the PC or to debug system code.

[Hyper-V](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/) enables running virtualized computer systems on top of a physical host. These virtualized systems can be used and managed just as if they were physical computer systems, however they exist in virtualized and isolated environment. Special software called a hypervisor manages access between the virtual systems and the physical hardware resources. Virtualization enables quick deployment of computer systems, a way to quickly restore systems to a previously known good state, and the ability to migrate systems between physical hosts.

[VirtManager](https://github.com/virt-manager/virt-manager) is a graphical tool for managing virtual machines via libvirt. Most usage is with QEMU/KVM virtual machines, but Xen and libvirt LXC containers are well supported. Common operations for any libvirt driver should work.

[oVirt](https://www.ovirt.org) is an open-source distributed virtualization solution, designed to manage your entire enterprise infrastructure. oVirt uses the trusted KVM hypervisor and is built upon several other community projects, including libvirt, Gluster, PatternFly, and Ansible.Founded by Red Hat as a community project on which Red Hat Enterprise Virtualization is based allowing for centralized management of virtual machines, compute, storage and networking resources, from an easy-to-use web-based front-end with platform independent access.

[Xen](https://github.com/xen-project/xen) is focused on advancing virtualization in a number of different commercial and open source applications, including server virtualization, Infrastructure as a Services (IaaS), desktop virtualization, security applications, embedded and hardware appliances, and automotive/aviation.

[Ganeti](https://github.com/ganeti/ganeti) is a virtual machine cluster management tool built on top of existing virtualization technologies such as Xen or KVM and other open source software. Once installed, the tool assumes management of the virtual instances (Xen DomU).

[Packer](https://www.packer.io/) is an open source tool for creating identical machine images for multiple platforms from a single source configuration. Packer is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

[Vagrant](https://www.vagrantup.com/) is a tool for building and managing virtual machine environments in a single workflow. With an easy-to-use workflow and focus on automation, Vagrant lowers development environment setup time, increases production parity, and makes the "works on my machine" excuse a relic of the past. It provides easy to configure, reproducible, and portable work environments built on top of industry-standard technology and controlled by a single consistent workflow to help maximize the productivity and flexibility of you and your team.

[VMware Workstation](https://www.vmware.com/products/workstation-pro.html) is a hosted hypervisor that runs on x64 versions of Windows and Linux operating systems; it enables users to set up virtual machines on a single physical machine, and use them simultaneously along with the actual machine.

# Databases
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

<p align="center">
 <img src="https://user-images.githubusercontent.com/45159366/111918157-fcdfd680-8a40-11eb-96e9-7fecb43ea0eb.png">
  <br />
</p>


## Database Learning Resources

[SQL](https://en.wikipedia.org/wiki/SQL) is a standard language for storing, manipulating and retrieving data in relational databases.

[SQL Tutorial by W3Schools](https://www.w3schools.com/sql/)

[Learn SQL Skills Online from Coursera](https://www.coursera.org/courses?query=sql)

[SQL Courses Online from Udemy](https://www.udemy.com/topic/sql/)

[SQL Online Training Courses from LinkedIn Learning](https://www.linkedin.com/learning/topics/sql)

[Learn SQL For Free from Codecademy](https://www.codecademy.com/learn/learn-sql)

[GitLab's SQL Style Guide](https://about.gitlab.com/handbook/business-ops/data-team/platform/sql-style-guide/)

[OracleDB SQL Style Guide Basics](https://oracle.readthedocs.io/en/latest/sql/basics/style-guide.html)

[Tableau CRM: BI Software and Tools](https://www.salesforce.com/products/crm-analytics/overview/)

[Databases on AWS](https://aws.amazon.com/products/databases/)

[Best Practices and Recommendations for SQL Server Clustering in AWS EC2.](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/aws-sql-clustering.html)

[Connecting from Google Kubernetes Engine to a Cloud SQL instance.](https://cloud.google.com/sql/docs/mysql/connect-kubernetes-engine)

[Educational Microsoft Azure SQL resources](https://docs.microsoft.com/en-us/sql/sql-server/educational-sql-resources?view=sql-server-ver15)

[MySQL Certifications](https://www.mysql.com/certification/)

[SQL vs. NoSQL Databases: What's the Difference?](https://www.ibm.com/cloud/blog/sql-vs-nosql)

[What is NoSQL?](https://aws.amazon.com/nosql/)

## Databases and Tools

[Azure Data Studio](https://github.com/Microsoft/azuredatastudio) is an open source data management tool that enables working with SQL Server, Azure SQL DB and SQL DW from Windows, macOS and Linux.

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)  is the intelligent, scalable, relational database service built for the cloud. It’s evergreen and always up to date, with AI-powered and automated features that optimize performance and durability for you. Serverless compute and Hyperscale storage options automatically scale resources on demand, so you can focus on building new applications without worrying about storage size or resource management.

[Azure SQL Managed Instance](https://azure.microsoft.com/en-us/services/azure-sql/sql-managed-instance/) is a fully managed SQL Server Database engine instance that's hosted in Azure and placed in your network. This deployment model makes it easy to lift and shift your on-premises applications to the cloud with very few application and database changes. Managed instance has split compute and storage components.

[Azure Synapse Analytics](https://azure.microsoft.com/en-us/services/synapse-analytics/) is a limitless analytics service that brings together enterprise data warehousing and Big Data analytics. It gives you the freedom to query data on your terms, using either serverless or provisioned resources at scale. It brings together the best of the SQL technologies used in enterprise data warehousing, Spark technologies used in big data analytics, and Pipelines for data integration and ETL/ELT.

[MSSQL for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql) is an extension for developing Microsoft SQL Server, Azure SQL Database and SQL Data Warehouse everywhere with a rich set of functionalities.

[SQL Server Data Tools (SSDT)](https://docs.microsoft.com/en-us/sql/ssdt/download-sql-server-data-tools-ssdt) is a development tool for building SQL Server relational databases, Azure SQL Databases, Analysis Services (AS) data models, Integration Services (IS) packages, and Reporting Services (RS) reports. With SSDT, a developer can design and deploy any SQL Server content type with the same ease as they would develop an application in Visual Studio or Visual Studio Code.

[Bulk Copy Program](https://docs.microsoft.com/en-us/sql/tools/bcp-utility) is a command-line tool that comes with Microsoft SQL Server. BCP, allows you to import and export large amounts of data in and out of SQL Server databases quickly snd efficeiently.

[SQL Server Migration Assistant](https://www.microsoft.com/en-us/download/details.aspx?id=54258) is a tool from Microsoft that simplifies database migration process from Oracle to SQL Server, Azure SQL Database, Azure SQL Database Managed Instance and Azure SQL Data Warehouse.

[SQL Server Integration Services](https://docs.microsoft.com/en-us/sql/integration-services/sql-server-integration-services?view=sql-server-ver15) is a development platform for building enterprise-level data integration and data transformations solutions. Use Integration Services to solve complex business problems by copying or downloading files, loading data warehouses, cleansing and mining data, and managing SQL Server objects and data.

[SQL Server Business Intelligence(BI)](https://www.microsoft.com/en-us/sql-server/sql-business-intelligence) is a collection of tools in Microsoft's SQL Server for transforming raw data into information businesses can use to make decisions.

[Tableau](https://www.tableau.com/) is a Data Visualization software used in relational databases, cloud databases, and spreadsheets. Tableau was acquired by [Salesforce in August 2019](https://investor.salesforce.com/press-releases/press-release-details/2019/Salesforce-Completes-Acquisition-of-Tableau/default.aspx).

[DataGrip](https://www.jetbrains.com/datagrip/) is a professional DataBase IDE developed by Jet Brains that provides context-sensitive code completion, helping you to write SQL code faster. Completion is aware of the tables structure, foreign keys, and even database objects created in code you're editing.

[RStudio](https://rstudio.com/) is an integrated development environment for R and Python, with a console, syntax-highlighting editor that supports direct code execution, and tools for plotting, history, debugging and workspace management.

[MySQL](https://www.mysql.com/) is a fully managed database service to deploy cloud-native applications using the world's most popular open source database.

[PostgreSQL](https://www.postgresql.org/) is a powerful, open source object-relational database system with over 30 years of active development that has earned it a strong reputation for reliability, feature robustness, and performance.

[Amazon DynamoDB](https://aws.amazon.com/dynamodb/) is a key-value and document database that delivers single-digit millisecond performance at any scale. It is a fully managed, multiregion, multimaster, durable database with built-in security, backup and restore, and in-memory caching for internet-scale applications.

[FoundationDB](https://www.foundationdb.org/) is an open source distributed database designed to handle large volumes of structured data across clusters of commodity servers. It organizes data as an ordered key-value store and employs ACID transactions for all operations. It is especially well-suited for read/write workloads but also has excellent performance for write-intensive workloads. FoundationDB was acquired by [Apple in 2015](https://techcrunch.com/2015/03/24/apple-acquires-durable-database-company-foundationdb/).

[CouchbaseDB](https://www.couchbase.com/) is an open source distributed [multi-model NoSQL document-oriented database](https://en.wikipedia.org/wiki/Multi-model_database). It creates a key-value store with managed cache for sub-millisecond data operations, with purpose-built indexers for efficient queries and a powerful query engine for executing SQL queries.

[IBM DB2](https://www.ibm.com/analytics/db2) is a collection of hybrid data management products offering a complete suite of AI-empowered capabilities designed to help you manage both structured and unstructured data on premises as well as in private and public cloud environments. Db2 is built on an intelligent common SQL engine designed for scalability and flexibility.

[MongoDB](https://www.mongodb.com/) is a document database meaning it stores data in JSON-like documents.

[OracleDB](https://www.oracle.com/database/) is a powerful fully managed database helps developers manage business-critical data with the highest availability, reliability, and security.

[MariaDB](https://mariadb.com/) is an enterprise open source database solution for modern, mission-critical applications.

[SQLite](https://sqlite.org/index.html) is a C-language library that implements a small, fast, self-contained, high-reliability, full-featured, SQL database engine.SQLite is the most used database engine in the world. SQLite is built into all mobile phones and most computers and comes bundled inside countless other applications that people use every day.

[SQLite Database Browser](https://sqlitebrowser.org/) is an open source SQL tool that allows users to create, design and edits SQLite database files. It lets users show a log of all the SQL commands that have been issued by them and by the application itself.

[dbWatch](https://www.dbwatch.com/) is a complete database monitoring/management solution for SQL Server, Oracle, PostgreSQL, Sybase, MySQL and Azure. Designed for proactive management and automation of routine maintenance in large scale on-premise, hybrid/cloud database environments.

[Cosmos DB Profiler](https://hibernatingrhinos.com/products/cosmosdbprof) is a real-time visual debugger allowing a development team to gain valuable insight and perspective into their usage of Cosmos DB database. It identifies over a dozen suspicious behaviors from your application’s interaction with Cosmos DB.

[Adminer](https://www.adminer.org/) is an SQL management client tool for managing databases, tables, relations, indexes, users. Adminer has support for all the popular database management systems such as MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Firebird, SimpleDB, Elasticsearch and MongoDB.

[DBeaver](https://dbeaver.io/) is an open source database tool for developers and database administrators. It offers supports for JDBC compliant databases such as MySQL, Oracle, IBM DB2, SQL Server, Firebird, SQLite, Sybase, Teradata, Firebird, Apache Hive, Phoenix, and Presto.

[DbVisualizer](https://dbvis.com/) is a SQL management tool that allows users to manage a wide range of databases such as Oracle, Sybase, SQL Server, MySQL, H3, and SQLite.

[AppDynamics Database](https://www.appdynamics.com/supported-technologies/database) is a management product for Microsoft SQL Server. With AppDynamics you can monitor and trend key performance metrics such as resource consumption, database objects, schema statistics and more, allowing you to proactively tune and fix issues in a High-Volume Production Environment.

[Toad](https://www.quest.com/toad/) is a SQL Server DBMS toolset developed by Quest. It increases productivity by using extensive automation, intuitive workflows, and built-in expertise. This SQL management tool resolve issues, manage change and promote the highest levels of code quality for both relational and non-relational databases.

[Lepide SQL Server](https://www.lepide.com/sql-storage-manager/) is an open source storage manager utility to analyse the performance of SQL Servers. It provides a complete overview of all configuration and permission changes being made to your SQL Server environment through an easy-to-use, graphical user interface.

[Sequel Pro](https://sequelpro.com/) is a fast MacOS database management tool for working with MySQL. This SQL management tool helpful for interacting with your database by easily to adding new databases, new tables, and new rows.


## Contribute

- [x] If would you like to contribute to this guide simply make a [Pull Request](https://github.com/mikeroyal/NixOS-Guide/pulls).


## License
[Back to the Top](https://github.com/mikeroyal/NixOS-Guide#table-of-contents)

Distributed under the [Creative Commons Attribution 4.0 International (CC BY 4.0) Public License](https://creativecommons.org/licenses/by/4.0/).
