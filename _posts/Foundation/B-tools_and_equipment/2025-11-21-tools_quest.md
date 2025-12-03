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

`This visual will help remind me of Tools and their relationship to my Development Journey.`

```mermaid
flowchart LR
    %% GitHub Sources
    subgraph GitHub_Pages[GitHub: Open-Coding-Society/pages]
        A[Repo: pages]:::repo
    end

    subgraph GitHub_Template[GitHub:]
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

`This diagram will show what we did over the past few weeks.`

```mermaid
flowchart TD
    subgraph Day_1[Day 1-3 Account Creation and Morals]
        A[Created Github and Slack account<br/>Joined Open Coding Society Slack<br/>Discussed PII<br/>Cloned OpenCS repo<br/>Set up Github Pages]:::dayuno
end 
    subgraph Day_2[Day 4-7 OS setup]
        B[Installed different ways  <br/>WSL, Homebrew, Kasm, <br/>Pulled Github repo to Linux]:::daydos
end
    subgraph 
```