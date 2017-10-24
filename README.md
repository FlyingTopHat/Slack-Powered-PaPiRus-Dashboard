# Slack Powered PaPiRus Dashboard

Uses a Raspberry Pi with a PaPiRus display as a dashboard for displaying data from a Slack channel.
## Setup the Raspberry Pi

1. Follow the [getting started guide](https://www.raspberrypi.org/learning/hardware-guide/).
2. Configure the Raspberry Pi so it is accessible via SSH

## Providing the Slack API token

### Command-line

```
ansible-playbook -i hosts -e "slack_token=<TOKEN HERE>" site.yml
```

### JSON file

`secrets.yml`
```
{
  slack_token: "<TOKEN HERE>"
}

```

```
$ ansible-playbook -i hosts -e "@secrets.json" site.yml
```
