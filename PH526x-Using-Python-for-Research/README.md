# Using Python for Research
## About this repository
This repository uses Git LFS to store media files, such as videos and subtitles from the classes. If you want to also download them you must initialize LFS in your local copy of the repository.

### Git LFS
Home page: [[LINK]](https://git-lfs.com)

#### Installing and initializing
Follow the instructions in the homepage to install and initialize `git-lfs` in your repository:

```bash
# Initialize Git LFS
$ git lfs install
Updated git hooks.
Git LFS initialized.
```

#### Configuring
GitHub article: [[LINK]](https://docs.github.com/en/repositories/working-with-files/managing-large-files/configuring-git-large-file-storage)

In this repository, we want all files in `**/media` folders to be stored in the LFS, so we launch:

```bash
$ git lfs track "**/media/*"
```

This will create a `.gitattributes` file that must be added to Git before adding and pushing any file to the LFS:

```bash
$ git add .gitattributes
```

Now you can add the `media` folders for commit and check if they're correctly tracked by LFS with `git lfs ls-files`:

```bash
$ git add .
# Ensure that the expected files are include in LFS
$ git lfs ls-files
7f85a1e5ae * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.mp4
a5f737acad * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.srt
02cd65e5d5 * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.txt
65ada7275d * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.mp4
886c390149 * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.srt
21349873e8 * PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.txt
```

You can also use `git lfs status` to check the files pending to commit and whether they are tracked by LFS or not:

```bash
$ git lfs status
On branch main
Objects to be pushed to origin/main:


Objects to be committed:

	PH526x-Using-Python-for-Research/README.md (Git: 1c35fe1)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/README.md (Git: 4a7b48b)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/README.md (Git: e1fbe49)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.mp4 (LFS: 7f85a1e)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.srt (LFS: a5f737a)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.1-python-basics.txt (LFS: 02cd65e)
  PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.mp4 (LFS: 65ada72)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.srt (LFS: 886c390)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/media/1.1.2-objects.txt (LFS: 2134987)
	PH526x-Using-Python-for-Research/week-1-Basics-of-Python-3/part-1-objects-and-methods/scripts/data-attribute-vs-method.ipynb (Git: e3b0c44)

Objects not staged for commit:


```

> [!WARNING]
>
> TODO: Explain how to enable Git LFS when cloning the repository

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

> [!WARNING]
>
> TODO: Explain how to properly create or recreate a conda environment