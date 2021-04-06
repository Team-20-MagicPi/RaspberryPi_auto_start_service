# RaspberryPi_auto_start_service
create a new service to enable auto start of the program

## step 1
create a `xx.service` file. The codes are as follows:
```
[Unit]
Description=<Your description>
[Service]
ExecStart=<The absolute address of the executable file>
[Install]
WantedBy=multi-user.target
```

## step 2
copy it to `/etc/systemd/system`

## step 3
Elevate permissions
`chmod u+x <name of the service>`

## step 4
now it can be enabled via system service
`sudo systemctl start xx.service`

