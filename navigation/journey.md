---
toc: false 
layout: post
title: Tools Journey 
description: Journey with development tools -- GitHub, Cloning, Virtual Environments, and Running a local website.
permalink: /tools/journey
---

## Visual Journey

The Linux kernel offers the best distributions for developers through it's open-source availability, allowing developers to modify critical system files to get programs to work and allowing many developing-related packages to be installed via package managers that anyone can put software on.  

![Tux the Linux Mascot]({{site.baseurl}}/images/about/tuz.png)

This visual will help remind me of Tools and their relationship to my Development Journey. 

```mermaid
flowchart LR
    %% GitHub Sources
    subgraph GitHub_Pages[GitHub: Open-Coding-Society/pages]
        A[Repo: pages]:::repo
    end

    subgraph GitHub_Template[GitHub: Open-Coding-Society/student]
        T[Template Repo: student]:::repo
    end

    subgraph GitHub_Student[GitHub: rsharma5128/student]
        B[Repo: student]:::repo
    end

    %% Local Computer
    subgraph Local[Local Computer]
        subgraph opencs_dir[opencs/ directory]
            C[pages/]:::local
            Ccmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
        subgraph user_dir[rsharma5128/ directory]
            D[student/]:::local
            Dcmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
    end

    %% Arrows: cloning
    A -.->|clone/pull only| C
    B <--> |clone, pull & push| D

    %% Arrows: template relationship
    T -.->|template→created| B

    %% Arrows: commands
    C --> Ccmd
    D <--> Dcmd

```

This diagram will show what we did over the past few weeks.

```mermaid
flowchart LR
    %% GitHub Sources
    subgraph GitHub_Pages[Account Creation]
        A[Created Github Account, discussed PII, created Slack account and enrolled in CS Slack, and cloned Open-Coding Society repository]:::repo
    end

    subgraph GitHub_Template[GitHub: Open-Coding-Society/student]
        T[Template Repo: student]:::repo
    end

    subgraph GitHub_Student[GitHub: rsharma5128/student]
        B[Repo: student]:::repo
    end

    %% Local Computer
    subgraph Local[Operating system setup]
        subgraph opencs_dir[Installed and set up Windows Subsystem for Linux(WSL) on Windows, installed Linux on school-issued machines, installed and set up Homebrew on MacOS devices, and set up Kasm web server on Chromebooks.]
            C[pages/]:::local
            Ccmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
        subgraph user_dir[rsharma5128/ directory]
            D[student/]:::local
            Dcmd[VSCode Prep<br/><br/>./scripts/venv.sh<br/>source venv/bin/activate<br/>code .]:::cmd
        end
    end

    %% Arrows: cloning
    A --> C
    B <--> D

    %% Arrows: template relationship
    T --> B

    %% Arrows: commands
    C --> Ccmd
    D <--> Dcmd

```