# git-lfs

## Installation

1. Download the tar file for your ubuntu from [here](https://git-lfs.com/).

2. Locate to the directory and unzip it.

```
cd ~/Downloads/
tar -xzvf git-lfs-linux-amd64-vx.x.x.tar.gz
cd git-lfs-x.x.x/
```

3. Run the script:

```
sudo chmod 777 install.sh
./install.sh
```

## Implementation

Run the following commands in the repository.

```
git init
git lfs install
git lfs track "*.psd"
```

```
git add .
git commit -m "first commit"
git remote add origin <repolink>
git push -u origin master
```

## Errors

```
remote: error: GH001: Large files detected. You may want to try Git Large File Storage - https://git-lfs.github.com.<br>
remote: error: Trace: 63a488b53055cc71938b40da95b11be9<br>
remote: error: See http://git.io/iEPt8g for more information.<br>
remote: error: File vanilla-app.zip is 129.25 MB; this exceeds GitHub's file size limit of 100.00 MB
To <file name> <br>
! [remote rejected] master -> master (pre-receive hook declined) error: failed to push some refs to  <file name> <br>
```

Remove the large files from being tracked, it won't remove it from your device. Use `git rm --cached <filename>`

Add the name of the file or folder in the `.gitignore` file to prevent it from being tracked.

```
touch .gitignore
vim .gitignore
```

Add file names in the `.gitignore`:

```
vanilla-app.zip
```

Now run again the following commands:

```
git add .
git commit -m "second commit"
git push -u origin main
```
