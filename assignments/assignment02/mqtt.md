# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output
hello
Enter QoS level (0, 1, 2): 2
[15:16:14] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301019/temperature'', ... (5 bytes)
[15:16:14] PUBLISH REQUESTED | QoS=2 | Message='hello' | msgid=1
Enter message to publish: [15:16:14] DEBUG | Received PUBREC (Mid: 1)
[15:16:14] DEBUG | Sending PUBREL (Mid: 1)
[15:16:14] DEBUG | Received PUBCOMP (Mid: 1)
[15:16:14] PUBLISHED | msgid=1
[15:17:09] DEBUG | Sending PINGREQ
[15:17:09] DEBUG | Received PINGRESP
source .venv/bin/activate

## Subscriber_qos.py Output

[15:12:12] SUBSCRIBED to test/qos/172.30.15.67 with QoS=2
[15:12:12] DEBUG | Received SUBACK
[15:13:13] DEBUG | Sending PINGREQ
[15:13:13] DEBUG | Received PINGRESP
[15:14:13] DEBUG | Sending PINGREQ
[15:14:13] DEBUG | Received PINGRESP