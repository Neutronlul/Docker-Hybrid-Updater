[![GPLv3 License](https://img.shields.io/badge/License-GPL%20v3-yellow.svg)](https://opensource.org/licenses/)
# Docker Hybrid Updater 


Orchestrates [Watchtower](https://github.com/containrrr/watchtower/) and [Gantry](https://github.com/shizunge/gantry) via [swarm-cronjob](https://github.com/crazy-max/swarm-cronjob) for auto updating of Docker standalone containers AND swarm services.
## Environment Variable Reference


| Key                  | Default    | Description                                                                                                                                |
| :------------------- | :--------: | :----------------------------------------------------------------------------------------------------------------------------------------- |
| `SCHEDULE`           |            | **Required**. Must be in [6-parameter CRON](https://pkg.go.dev/github.com/robfig/cron?utm_source=godoc#hdr-CRON_Expression_Format) format. |
| `SCHEDULE_GANTRY`    | `SCHEDULE` | If you want to stagger/offset Gantry from Watchtower. Same format as `SCHEDULE`.                                                           |
| `WATCHTOWER_CLEANUP` | `true`     | See [Watchtower docs](https://containrrr.dev/watchtower/arguments/#cleanup).                                                               |
| `WATCHTOWER_TIMEOUT` | `60s`      | See [Watchtower docs](https://containrrr.dev/watchtower/arguments/#wait_until_timeout).                                                    |
| `TZ`                 | `UTC`      | Timezone. Must be in [tz database identifier](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) format.                        |
