<meta charset="utf-8"/>

# Installation

_Home Alarm_ runs on AppDeamon, so you have to have installed it in your HA environment.

## HACS

To install _Home Alarm_ easily I recommend to install it by HACS. You need to enable AppDeamon Apps in your HACS integration and then search the repository by name.

## Manual

To install _Home Alarm_ manually you have to download the `home_alarm` directory inside `apps` folder, copy it to your `/config/appdeamon/apps` directory in HA and rename it to `home-alarm`. You must restart AppDeamon.

# Updates

When updating the app is important to restart AppDeamon integration from Supervisor.

# What's next?

:arrow_right: [configuration](config/index.md)
