# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
[15:36:33] DEBUG | Sending PUBLISH (d0, q1, r0, m365), 'b'test/qos/6510301046/temperature'', ... (5 bytes)
[15:36:33] PUBLISH REQUESTED | SID=6510301046 | temperature=27.75 | QoS=1 | msgid=365
[15:36:33] DEBUG | Sending PUBLISH (d0, q1, r0, m366), 'b'test/qos/6510301046/humidity'', ... (5 bytes)
[15:36:33] PUBLISH REQUESTED | SID=6510301046 | humidity=41.61 | QoS=1 | msgid=366
[15:36:33] DEBUG | Sending PUBLISH (d0, q1, r0, m367), 'b'test/qos/6510301046/pressure'', ... (7 bytes)
[15:36:33] PUBLISH REQUESTED | SID=6510301046 | pressure=1016.92 | QoS=1 | msgid=367
[15:36:33] DEBUG | Sending PUBLISH (d0, q1, r0, m368), 'b'test/qos/6510301046/fan_speed'', ... (1 bytes)
[15:36:33] PUBLISH REQUESTED | SID=6510301046 | fan_speed=3 | QoS=1 | msgid=368
[15:36:33] DEBUG | Received PUBACK (Mid: 365)
[15:36:33] PUBLISHED | msgid=365
[15:36:33] DEBUG | Received PUBACK (Mid: 366)
[15:36:33] PUBLISHED | msgid=366
[15:36:33] DEBUG | Received PUBACK (Mid: 367)
[15:36:33] PUBLISHED | msgid=367
[15:36:33] DEBUG | Received PUBACK (Mid: 368)
[15:36:33] PUBLISHED | msgid=368
```

## Subscriber_qos.py Output

```
[15:36:33] DEBUG | Received PUBLISH (d0, q1, r0, m320), 'test/qos/6510301046/humidity', ...  (5 bytes)
[15:36:33] RECEIVED | humidity: 41.61 | QoS=1
[15:36:33] DEBUG | Sending PUBACK (Mid: 320)
[15:36:33] DEBUG | Received PUBLISH (d0, q1, r0, m321), 'test/qos/6510301046/pressure', ...  (7 bytes)
[15:36:33] RECEIVED | pressure: 1016.92 | QoS=1
[15:36:33] DEBUG | Sending PUBACK (Mid: 321)
[15:36:33] DEBUG | Received PUBLISH (d0, q1, r0, m322), 'test/qos/6510301046/fan_speed', ...  (1 bytes)
[15:36:33] RECEIVED | fan_speed: 3 | QoS=1
[15:36:33] DEBUG | Sending PUBACK (Mid: 322)
```