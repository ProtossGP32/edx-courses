# Using Python for Research
## About this repository
This repository uses Git LFS to store media files, such as videos and subtitles from the classes. If you want to also download them you must initialize LFS in your local copy of the repository.

### Git LFS
Home page: [[LINK]](https://git-lfs.com)

#### Installing and initializing
Follow the instructions in the homepage to install and initialize `git-lfs` in your repository:

```bash
# Initialize Git LFS - This updates the .gitattributes file
$ git lfs install
Updated git hooks.
Git LFS initialized.
```

#### Configuring
GitHub article: [[LINK]](https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage)



## Required resources
### Anaconda
Installation instructions: [here](https://docs.anaconda.com/free/anaconda/install/linux/)

Installing on Debian:

```bash
# Replace <INSTALLER_VERSION> with the version of the installer file you want to download
# For example, https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh
# All installers can be found at repo.anaconda.com/archive/
curl -O https://repo.anaconda.com/archive/Anaconda3-<INSTALLER_VERSION>-Linux-x86_64.sh
```

Anaconda used in this course: 2023.09-0

```bash
# Download installer
curl -O https://repo.anaconda.com/archive/Anaconda3-2023.09-0-Linux-x86_64.sh
# Execute script
bash ~/Downloads/Anaconda3-2023.09-0-Linux-x86_64.sh
```

Make sure you have enough space on disk for the installation and choose FAT or exFAT filesystem disks. Errors appeared when trying to use NTFS filesystem.