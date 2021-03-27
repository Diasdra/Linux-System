# Weather Script with Timer
---

## Weather Script using *systemd* on Linux OS

Weather file is refershed every 60mins for the destination determined from host IP address. To use the service, you will need to configure the wttr_script, wttr_script.service, and wttr_script.timer with the instructions below:

wttr_script
1. Confirm or create a `bin` folder in your `$HOME` directory 
2. Place wttr_script file in bin directory
3. Run script to create a weather file that will hold the data for the weather

wttr_script.timer and wttr_script.service

1.Save wttr_script.timer and wttr_script.service inside `$HOME` directory 
2.Copy the files into your /etc/systemd/system directory -`sudo cp wttr_script.service /etc/systemd/system/wttr_script.service` and `sudo cp wttr_script.timer /etc/systemd/system/wttr_script.timer`
3.Reload system daemons - `sudo systemctl daemon-reload`
4.Enable timer to run on boot - `sudo systemctl enable --now wttr_script.timer`

---
Congratulations, your service is now installed!
