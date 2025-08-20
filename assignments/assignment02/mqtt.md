# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output

```
:\Users\thana\Desktop\My_Work\IOT\Iot-class-2025-gateway\app\publisher_qos.py:20: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[16:01:06] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
Enter message to publish: [16:01:06] DEBUG | Received CONNACK (0, 0)
yipeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee
Enter QoS level (0, 1, 2): 2
[16:01:12] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301046'', ... (60 bytes)
[16:01:12] PUBLISH REQUESTED | QoS=2 | Message='yipeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee' | msgid=1      
Enter message to publish: [16:01:12] DEBUG | Received PUBREC (Mid: 1)
[16:01:12] DEBUG | Sending PUBREL (Mid: 1)
[16:01:12] DEBUG | Received PUBCOMP (Mid: 1)
[16:01:12] PUBLISHED | msgid=1

```

## Subscriber_qos.py Output

```
c:\Users\thana\Desktop\My_Work\IOT\Iot-class-2025-gateway\app\subscriber_qos.py:25: DeprecationWarning: Callback API version 1 is deprecated, update to latest version
  client = mqtt.Client()
[16:00:35] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[16:00:35] DEBUG | Received CONNACK (0, 0)
[16:00:35] Connected with result code 0
[16:00:35] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301046', 2)]
[16:00:35] DEBUG | Received SUBACK
[16:01:12] DEBUG | Received PUBLISH (d0, q2, r0, m1), 'test/qos/6510301046', ...  (60 bytes)
[16:01:12] DEBUG | Sending PUBREC (Mid: 1)
[16:01:12] DEBUG | Received PUBREL (Mid: 1)
[16:01:12] RECEIVED | QoS=2 | Topic=test/qos/6510301046 | Message=yipeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeeee | msgid=1
[16:01:12] DEBUG | Sending PUBCOMP (Mid: 1)
```