# lfs-example

## Setup

```
# Enable LFS on the repo:
git lfs install

# Track all JPEG files as LFS:
git lfs track '*.jpg' # Creates the .gitattributes file

# Commit .gitattributes file:
git add .gitattributes
git commit -m "Add .gitattributes"

# Commit a JPEG file:
git add image.jpg
git commit -m "Add an image"

# Check if LFS is configured:
test -f .gitattributes && cat .gitattributes | grep filter=lfs

# List any files tracked as LFS:
git ls-files ':(attr:filter=lfs)'
```
