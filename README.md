# Pulse Workspace App Configs

Copyright (c) 2017 by Pulse Secure, LLC. All rights reserved


A repository for known app-configs using the appconfig.org schema.


## Installing Requirements

To install project requirements, use pip:

```
pip install -r requirements.txt
```

## Downloading App Config XML

To download existing app config XML specify the `APP_CONFIG_ROOT` URL when running the download script:

```
APP_CONFIG_ROOT=https://... ./bin/download
```


## Generating App Config From JSON

Some app vendors only publish app config schema as a webpage and we construct the XML manually.

First create a json file in `./apps/` with the name of the package as the file name:

```
    ./apps/com.example.myapp.json
```

The data structure should be a dictionary where the keys are the config key and the value is a data
structure like this:


```
  "my_config_key": {
    "description": "Description of this key.",
    "group": "Group",
    "title": "Config Key Title", 
    "type": "(string|boolean|integer)"
  }
```