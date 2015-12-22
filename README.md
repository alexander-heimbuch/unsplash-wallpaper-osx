# Random Unsplash Wallpapers for OSX
Grabs a random image from [unsplash.it](https://unsplash.it) and places it as your default wallpaper every time you run it. All images are stored in ``~/backgrounds``.

Simple automator application that encapsulates the following bash script:

```
TIMESTAMP=$(date +%s)

mkdir -p ~/backgrounds
cd ~/backgrounds
curl -o $TIMESTAMP.png "https://unsplash.it/2560/1600/?random"
osascript -e "tell application \"System Events\" to set picture of every desktop to \"~/backgrounds/$TIMESTAMP.png\""
```
