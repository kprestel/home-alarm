:bell: _Home Alarm_ allows you to use any media player such as Alexa or Google Home to make them act as an alarm system at home. It also supports the notification system to alert you if you are not at home.

# Documentation

This security system keep listening the window and door sensors that are installed in your smart home system and the safe mode input.

If the safe mode is active and some of windows or doors are opened, the user has a few seconds to indentify himself into the system. ([see link](identification.md))

If the user cannot identify himself into the system, the alarm will be fired on the media player and the user will be notified that an unathorized user has been entered to his house.

# Example

This is a quick example about how to configure the application with 2 Alexas as media players, 2 window/door sensors and 1 motion sensor.

```yaml
home_alarm:
  module: home_alarm
  class: HomeAlarm
  sensors:
    - binary_sensor.livingroom_window_contact
    - binary_sensor.entrance_door_contact
    - binary_sensor.entrance_motion_occupancy
  safe_mode: input_boolean.safe_mode
  alerts:
    - id: media_player
      sound: amzn_sfx_scifi_alarm_04
      loop_delay: 4
      media_players:
        - media_player.alexa
        - media_player.alexa2
    - id: notifier
      notifiers:
        - notify.mobile_app_iphone
        - notify.notifier
```
