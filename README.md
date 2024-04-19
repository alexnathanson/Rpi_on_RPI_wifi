# Rpi_on_RPI_wifi

Network info for connecting a Raspberry Pi to RPI's wifi network. This should work with both rpi_wpa2 and eduroam networks.

Edit the wpa_supplicant file.

`sudo nano /etc/wpa_supplicant/wpa_supplicant.conf`

Add this to the file. Note that identity is just your username NOT username@rpi.edu.

```
network={
        ssid="rpi_wpa2"
        scan_ssid=1
        key_mgmt=WPA-EAP
        identity="****"
        password="******"
        eap=PEAP
        phase1="peaplabel=0"
        phase2="auth=MSCHAPV2"
}

```

Reboot
`sudo reboot`
