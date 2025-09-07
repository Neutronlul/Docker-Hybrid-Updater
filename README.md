[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
[![GitHub stars](https://img.shields.io/github/stars/Neutronlul/Docker-Hybrid-Updater.svg?style=flat&logo=github)](https://github.com/Neutronlul/Docker-Hybrid-Updater/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Neutronlul/Docker-Hybrid-Updater.svg?style=flat&logo=github)](https://github.com/Neutronlul/Docker-Hybrid-Updater/network)
[![GitHub issues](https://img.shields.io/github/issues/Neutronlul/Docker-Hybrid-Updater.svg?style=flat&logo=github)](https://github.com/Neutronlul/Docker-Hybrid-Updater/issues)
[![GitHub last commit](https://img.shields.io/github/last-commit/Neutronlul/Docker-Hybrid-Updater.svg?style=flat&logo=github)](https://github.com/Neutronlul/Docker-Hybrid-Updater/commits)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://github.com/Neutronlul/Docker-Hybrid-Updater/graphs/commit-activity)
[![Docker Compose](https://img.shields.io/badge/docker--compose-blue.svg?logo=docker)](https://docs.docker.com/compose/)
[![Docker Swarm](https://img.shields.io/badge/docker--swarm-blue.svg?logo=docker)](https://docs.docker.com/engine/swarm/)

# Docker Hybrid Updater 


Orchestrates [Watchtower](https://github.com/containrrr/watchtower/) and [Gantry](https://github.com/shizunge/gantry) via [swarm-cronjob](https://github.com/crazy-max/swarm-cronjob) for auto-updating of Docker standalone containers AND swarm services.
## Environment Variable Reference


| Key                  | Default    | Description                                                                                                                                |
| :------------------- | :--------: | :----------------------------------------------------------------------------------------------------------------------------------------- |
| `SCHEDULE`           |            | **Required**. Must be in [6-parameter CRON](https://pkg.go.dev/github.com/robfig/cron?utm_source=godoc#hdr-CRON_Expression_Format) format. |
| `SCHEDULE_GANTRY`    | `SCHEDULE` | If you want to stagger/offset Gantry from Watchtower. Same format as `SCHEDULE`.                                                           |
| `WATCHTOWER_CLEANUP` | `true`     | See [Watchtower docs](https://containrrr.dev/watchtower/arguments/#cleanup).                                                               |
| `WATCHTOWER_TIMEOUT` | `60s`      | See [Watchtower docs](https://containrrr.dev/watchtower/arguments/#wait_until_timeout).                                                    |
| `TZ`                 | `UTC`      | Timezone. Must be in [tz database identifier](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) format.                        |
