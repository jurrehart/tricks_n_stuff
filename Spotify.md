# Spotify

## Linux
### Greyed out playlist
The greyed out playlist is due to network manager connectivity check settings it points defualt to a gnome URL that sporadicly does not respond, this leads Spotify client tot grey out  the playlists
To fiz create the follwoing file `/etc/NetworkManager/conf.d/20-connectivity.conf` with the following contents
```
[connectivity]
uri=http://www.archlinux.org/check_network_status.txt 
interval=0
```
Then restart network manager `systemctl restart NetworkManager`

All should be good now

## FreeBSD
By default spotify will not work on FreeBSD. But there's this awsome repo [mrclksr/linux-browser-installer](https://github.com/mrclksr/linux-browser-installer).
It's a shell script to install Chrome,Brave or Vivaldi in a Ubuntu Jail where the browser is ran with the linuxalator. 
