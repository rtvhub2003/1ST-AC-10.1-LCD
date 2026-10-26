# [1ST AC PROGRAMMING | 10.1" LCD DISPLAY]
##### [LINUX LAPTOP IS REQUIRED]

## 1. Access System | LAPTOP [TERMINAL1]
<br>
cmd: `ssh rtv@192.168.1.121`
<br>
passkey: `123`

## 2. Check, if already programmed or new system
<br>
cmd: `ls`

<br>
If, firstAc application is running, stop it
<br>
cmd: sudo systemctl stop start_app_audio

## 3. Go inside ac1 folder
<br>
cmd: cd ac1/
<br>
cmd: ls [check if file is existing]
<br>
cmd: mv lcd_pis_prod_3_g2l_ac1 lcd_pis_prod_3_g2l_ac1.old [rename file if existing]
<br>
cmd: ls [make sure file is renamed]

## 4. Transfer application | New Terminal [TERMINAL2] in LAPTOP
<br>
cmd: scp lcd_pis_prod_3_g2l_ac1 rtv@192.168.1.121:/home/rtv/ac1/
<br>
passkey: 123

## 5. Apply permssion | [TERMINAL1]
<br>
cmd: chmod a+x lcd_pis_prod_3_g2l_ac1

## 6. Fonts transfer
<br>
cmd: cd /usr/share/fonts/
<br>
cmd: sudo rm -r *
<br>
cmd: ls [make sure, everything is deleted]

cmd: sudo chown rtv:rtv /usr
<br>
cmd: sudo chown rtv:rtv /usr/share
<br>
cmd: sudo chown rtv:rtv /usr/share/fonts

cmd: scp -r fonts rtv@192.168.1.121:/usr/share/
<br>
passkey: 123
<br>

<br> [It may take a few seconds/minutes to transfer all fonts. Please keep patience here!]

## 7. Check if fonts in system
<br>
cmd: ls
<br>
cmd: ls /usr/share/fonts/

<br> ## 8. RESTART SYSTEM AND PROCEED WITH TEST POINTS MENTIONED BELOW


# [1ST AC TEST POINS]

## 1. Route Start: <br>
#### ..............> Route Status on MPU <br>
#### ..............> Route Status on 10.1" LCD (8 out of 8) <br>
#### ..............> Scrolling Headlines in (10.1") LCD <br>
#### ..............> DRM (MAP) in 10.1" LCD <br>
#### ..............> Slogans/Messages in 10.1" LCD as per MPU <br>
#### ..............> Brightness [Day/Night Mode] <br>
#### ..............> Alarms <br>
#### ..............> Emergency Messages <br>
#### ..............> Audio Check using AUX (AUDIO OUT) Ports <br>
#### ..............> Remove/power off intermedia device (10.1" LCD), and check remaining devices are receiving updates (may get delayed syncing) <br>
#### ..............> Power on the removed device, and check if it is synced with the other devices (Currently DRM Issues) <br>
#### ..............> [X] Turning device off (10.1") LCD, before route start, stuck in scanning mode <br>
#### ..............> Data <br>
#### ..............> <br>
