# git-lfs

## Installation

1. Download the tar file for your ubuntu from [here](https://git-lfs.com/).

2. Locate to the directory and unzip it.

```bash
cd ~/Downloads/
tar -xzvf git-lfs-linux-amd64-vx.x.x.tar.gz
cd git-lfs-x.x.x/
```

3. Run the script:

```bash
sudo chmod +x install.sh
./install.sh
```

## Implementation

Run the following commands in the repository.

```bash
git init
git lfs install

# change largeFileName with the file name which exceeds 100Mb
git lfs track largeFileName
```

`.gitattributes` file will be created with `largeFile` name inside it.

```bash
sudo git add .
git commit -m "first commit"
git remote add origin <repolink>
git push -u origin main
```
