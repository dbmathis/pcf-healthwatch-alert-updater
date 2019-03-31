
# PCF Healthwatch Alert Updater

A simple shell script to update PCF healthwatch alerts.


## Installation

### Install dependencies cf-uaac and jq.

#### uaac:
https://github.com/cloudfoundry/cf-uaac

#### jq:
https://stedolan.github.io/jq/download


### Install updater
```
$ git clone https://github.com/dbmathis/pcf-healthwatch-alert-updater.git
$ cd pcf-healthwatch-alert-updater
$ chmod +x hw-alert-updater.sh
```

## Target CF UAA and fetch a client token for healthwatch api admin.
```
$ uaac target <cf-uaa> [--skip-ssl-validation]
$ uaac token client get healthwatch_api_admin -s <secret>
```
  
## Usage
```
Usage: hw-alert-update.sh [OPTION]...

  -a|--api      STRING  healthwatch-api.SYSTEM-DOMAIN/v1/alert-configurations
  -c|--critical NUM     critical threshold
  -w|--warning  NUM     warning threshold
  -t|--type     STRING  threeshold type
  -q|--query    REGEX   alert query search string  
  -h|--help|-?          show this help 
```

## Maintainer

* [David Mathis](https://github.com/dbmathis)


## Support

This is a community supported cloud foundry tool. Opening issues for questions, feature requests and/or bugs is the best path to getting "support".


## PCF Documentation

- [Configuring-PCF-Healthwatch-Alerts](https://docs.pivotal.io/pcf-healthwatch/1-2/api/alerts.html):
