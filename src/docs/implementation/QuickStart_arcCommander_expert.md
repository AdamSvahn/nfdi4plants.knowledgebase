---
layout: docs
title: ARC Commander QuickStart (Expert Version)
published: 2022-12-20
author: "Dominik Brilhaus"
author_orcid: https://orcid.org/0000-0001-9021-3197
author_github: brilator
add toc: false
add support: false
add sidebar: _sidebars/mainSidebar.md
article_status: published
todo:
---

## Checkpoint

:white_check_mark: You know how to use a command line or terminal  
:white_check_mark: You have created an ARC before  
:white_check_mark: The latest version of the [ARC Commander](https://github.com/nfdi4plants/arcCommander/releases) as well as [git](https://git-scm.com/downloads) and [git LFS](https://git-lfs.github.com/) are installed on your computer  
:white_check_mark: You have a [DataPLANT](https://register.nfdi4plants.org) account  
:white_check_mark: Your computer is linked to the [DataHUB](https://git.nfdi4plants.org) via an ssh key or a personal access token  

> :rocket: Voila! You are ready to follow these few steps to create a minimal ARC sharable via DataPLANT's DataHUB.

1. Visit the [DataHUB](https://git.nfdi4plants.org), create a new repository and copy the URL to your ARC (`https://git.nfdi4plants.org/<YourUserName>/<YourARC>.git`) to your clipboard.
2. Replace the `<variables>` in the following code block with your information and execute it in your command line.

```bash
# Create and navigate to your ARC folder
mkdir <path/to/YourARCFolder>
cd <path/to/YourARCFolder>

# Setup the ARC structure with one study and one assay
arc init
arc i create -i <YourInvestigationID>
arc a add -s <YourStudyID> -a <YourAssayID>

arc sync -f -r https://git.nfdi4plants.org/<YourUserName>/<YourARC> -m "initialize ARC structure"
```

```bash
# Even if you linked to the DataHUB, you might have to repeat this step before syncing
arc remote accesstoken get -s https://git.nfdi4plants.org
```
