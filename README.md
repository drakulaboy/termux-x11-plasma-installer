First we need to install X11-repo, execute following to install it
`pkg update ; pkg install x11-repo`
after we need to install Wayland
`pkg install xwayland`
then download this repo and install termux-x11 package
`dpkg -i --force-depends termux-x11.deb`
then install install termux-x11.apk file and open it
Set bigger resolution for better fps
*Open Termux:X11 app ,go to Preferences,and disable "Show additional keyboard"
run this command one time in termux to allow external apps to interact with termux
`
value="true"; key="allow-external-apps"; file="/data/data/com.termux/files/home/.termux/termux.properties"; mkdir -p "$(dirname "$file")"; chmod 700 "$(dirname "$file")"; if ! grep -E '^'"$key"'=.*' $file &>/dev/null; then [[ -s "$file" && ! -z "$(tail -c 1 "$file")" ]] && newline=$'\n' || newline=""; echo "$newline$key=$value" >> "$file"; else sed -i'' -E 's/^'"$key"'=.*/'"$key=$value"'/' $file; fi
`
install Plasma from github
```
apt update
apt install aria2 -y
aria2c https://ghproxy.com/github.com/kde-yyds/termux-x11-plasma-installer/raw/master/install.sh
chmod +x install.sh
./install.sh
```
Waaaaaait a little bit....more)
if you want english language run in termux
`sed -i 's/zh_CN/en_US/g' /data/data/com.termux/files/home/containers/scripts/archlinuxarm_plasma.sh`
and
`sed -i 's/zh_CN/en_US/g' /data/data/com.termux/files/home/containers/scripts/debianbullseye_xrenderkwin_xfce4-panel.sh`
then you can start it
start the Wayland with 
`termux-x11 :1`
open new session from the left side of termux and start Plasma with
`DISPLAY=:1 plasma`
Open Termux:X11 app
TADAAA
# About the project
Easy install and run with termux-x11 the KDE Plasma 5.26
![](https://ghproxy.com/github.com/kde-yyds/termux-x11-plasma-installer/raw/master/1.jpg)
Stable 60 FPS  
# Install and Launch

If the installation has been stopped for some reason run again ./install.sh to intall from where it stopped
![](https://ghproxy.com/github.com/kde-yyds/termux-x11-plasma-installer/raw/master/2.jpg)
