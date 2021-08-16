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
