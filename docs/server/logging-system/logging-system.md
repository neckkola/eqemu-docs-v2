---
tags:
  - Logs
  - Logging
---


# Logging System

!!! info

    EQEmu used to have many different logging systems in its past. 

    They all were configured differently, all had different configuration formats. 

    In 2015 - a much needed massive overhaul to our logging was made and it has been one of the most valuable things to our project to date.

## Features

* [x] Logging levels (General, Moderate, Detail)
* [x] Hot-Reload of log settings
* [x] In game, real time server logs
* [x] Categories (Spells, Merchants, Loot etc.)

## Output Formats

* [x] Console
* [x] File
* [x] In game (gmsay)

Can easily be extended to be implemented with other output sinks

## Debug Levels

| **Level** |  | **Description** |
| :--- | :--- | :--- |
| General | 1 | Low-Level general debugging, useful info on single line |
| Moderate | 2 | Informational based - used in functions |
| Detail | 3 | Use this for extreme detail in logging, usually in extreme debugging in the stack or interprocess communication |

Debug levels are PER category, so if you wanted to set for example, level 3 debugging enabled to gmsay (In Game) but only 1 to your console, you put respectively 1 in your console field and 3 in gmsay for whatever category it is your enable

## Settings

All settings are managed in **logsys_categories** database table

When a process boots up, such as **zone/world/ucs/queryserv/etc**. These settings will load and whatever applies to the server category wise is what it will use as **rules** to understand where to send output, as well as what level of information (high or low) to display

!!! info

      Please note that **log_to_gmsay** is only available for zone-level debugging

      As of 2021 it is available in world as well if you have rule **WorldGMSayLogging** enabled (enabled by default)


## In-Game Commands

| **Command**        | **Description** |
|:-------------------| :--- |
| #logs              | Displays usage menu |
| #logs reload       | Reload all settings in world and all zone processes with what is defined in the database |
| #logs list         | Shows current log settings and categories loaded into the current process' memory |
| #logs set [console |file|gmsay] | Sets log settings during the lifetime of the zone |

```text
#logs set [gmsay|file|console] [category_id] [log_level]
```

## File Logs

* All **zone logs** go underneath a respective **logs/zone/**
  * All zones, once booted up, will have a name that actually means something to a server administrator:
    * nexus_version_0_inst_id_0_port_7000_20084.log
    * nexus_version_0_inst_id_0_port_7000_24356.log
    * zone_20084.log - A zone that has been booted up as a dynamic, but not assigned to any logical zone yet
* Crash Logs will make their way underneath `logs/crash`
* All other process logs go to the top level of logs, this may change
* Naming Convention:
  * Unless a zone is using zone properties for the file name, most processes will look like the following convention
    * process_name_process_id.log

## Logging Output Examples

### In Game Messages (gmsay)

![](https://github.com/EQEmu/Server/wiki/images/FaWAgAq.gif?raw=true)

### Windows Console of Zone

![](https://camo.githubusercontent.com/e632e54b062cb1574fe7228a8b96ec448f4566aa/68747470733a2f2f692e696d6775722e636f6d2f6f6b57673279382e706e67)

### Linux Console

![](https://camo.githubusercontent.com/f850f759deb0332226829d2f6c806885f08e7a6b/68747470733a2f2f692e696d6775722e636f6d2f5343396c4f344e2e706e67)

