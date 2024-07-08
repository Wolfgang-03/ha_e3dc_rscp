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

and restart home assistent to force loading this yaml-file. 
