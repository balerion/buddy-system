# Buddy System
buddy system for raspberry pis to check on each other for life

each rpi:
- waits for watchdog ping from all rpis on list
- checks that all rpis on their list are alive
- for every watchdog triggered sends telegram message
- for every watchdog triggered sends alarm to all rpis on list
- adds rpi to list if receives a new ping
- sends a ping containing time to reset watchdog for

hard parts:
- safe com protocol for sending and receiving pings and alarms
- sending telegram messages without being written to first

