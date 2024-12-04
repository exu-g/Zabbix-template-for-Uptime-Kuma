# Zabbix Template for Uptime Kuma monitoring

## Overview

For Zabbix version: 6.4 and higher.

HTTP is using for Uptime Kuma monitoring.

This template is developed for monitoring state and latenct of all Uptime Kuma monitors:

- Monitor state
- Monitor latency

LLD using for monitors discovery.

This template was tested on:

Uptime Kuma

- Version: 1.23.11
- Frontend Version: 1.23.11

## Setup

Add API key:

![API key setup](https://github.com/volodinaleksey/Zabbix-template-for-Uptime-Kuma/assets/82817077/a12895e1-c8cd-4cd0-9542-e31d4a6e1134)

## Author

Aleksey Volodin

## Macros used

Default macros values should be adjusted according your environment.

| Macro               | Value                                        | Description                                    |
| ------------------- | -------------------------------------------- | ---------------------------------------------- |
| {$KUMA.API.KEY}     | uk2_vWYsS2n-ozz6L6uw5uX5TYTA9McsytTHRoLNmeMC | Uptime Kuma API key.                           |
| {$KUMA.METRICS.URL} | https://example.com/metrics                  | Your metrics URL. (https://[YOUR URL]/metrics) |

## Template links

There are no template links in this template.

## Discovery rules

| Name                   | Description                      | Type       | Key and additional info |
| ---------------------- | -------------------------------- | ---------- | ----------------------- |
| Kuma metrics discovery | Discover all Uptime Kuma metrics | HTTP Agent | kuma.metrics.discover   |

## Items collected

- Monitor status
- Response time

## Triggers

- Monitor is down
