# ha_e3dc_rscp
Automations for E3DC Wallboxes with Home Assistant

You must add the folowing in your configuration.yaml

```
homeassistant:
  # load all packages from subdir packages
  packages: !include_dir_named packages
```

and put the e3dc_automation.yaml in the directory 

/config/packages/

and restart home assistent to force loading this yaml-file. Afterwards creat an automation wich calls the script "s10e_pro_wallboxes_check_status" every 2 minutes or whatever you want. Something like this:

```
alias: E3DC Wallbox - Automatisierung
description: ""
trigger:
  - platform: time_pattern
    minutes: /2
    seconds: "20"
condition: []
action:
  - service: script.s10e_pro_wallboxes_check_status
    metadata: {}
    data: {}
mode: single
```
