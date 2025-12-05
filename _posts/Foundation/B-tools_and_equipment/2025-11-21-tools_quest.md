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
flowchart LR
    subgraph Day_1[Day 1-7 Computer Setup]
        A[Days 1-3<br/><br/>Created Github and Slack account<br/>Joined Open Coding Society Slack<br/>Discussed PII<br/>Cloned OpenCS repo<br/>Set up Github Pages<br/>Made issues on repo<br/>Used vscode.dev web client to edit repo files<br/>Taught how to do basic things like modify text and what files correspond to webpage]:::dayuno
        B[Days 4-7<br/><br/>Installed different ways of accessing Linux<br/>WSL, Homebrew, Kasm <br/>Pulled Github repo to Linux<br/>Edited repo in VSCode app<br/>Figured out how to access localhost using VSCode app and make command<br/>Learned to commit and push changes]:::daydos
        C[Days 8-9<br/>Website File editing<br/><br/>Taught how to create files in repositories<br/>Reflected on journey through days 1-7<br/>Learn basic Mermaid and Markdown which was optional<br/>Read troubleshooting guide]:::daytres
    end
A --> B
B --> C
```
**NOTE:** `For days 1-3, the top-down lines are listed in chronological order(top is the earliest, bottom is the latest)`