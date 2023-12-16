


## connect to wifi
nmcli dev status

nmcli radio wifi
nmcli radio wifi on

nmcli dev wifi rescan
nmcli dev wifi list

sudo nmcli --ask dev wifi connect [SSID]

nmcli con show

## maintenance
paru
journalctl --vacuum-time=4weeks
paccache -ruk0
sudo reflector --protocol https --verbose --latest 25 --sort rate --save /etc/pacman.d/mirrorlist
pacman -Rns $(pacman -Qdtq)
