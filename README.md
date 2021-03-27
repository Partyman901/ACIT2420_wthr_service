# ACIT2420_wthr_service

wthr - A service that writes the weekly forecast onto a text file every hour

## Installation
1. Extract the zip file into a directory
2. Move the service and timer files using "mv wthr.service /etc/systemd/system" and "mv wthr.timer /etc/systemd/system"
3. Change directories into /etc/systemd/system
4. Open the service file for editing using sudo vim wthr.service
5. Enter INSERT mode by pressing "i"
6. Change ExecStart to the location of where the write_wttr file is located (e.g ExecStart=/home/username/directory/write_wttr)
7. Change WorkingDirectory to the directory of where write_wttr file is located (e.g WorkingDirectory=/home/username/directory)
8. Press ESC and enter :wq to save and exit

## Usage
You can start this service by simply typing "sudo systemctl start wthr.timer".
Whenever a new hour starts, a text file named todaysWeather.txt will be written to the directory you configured in WorkingDirectory in wther.service

