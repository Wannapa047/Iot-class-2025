# Exploring MQTT QoS Levels

Experiment with QoS 0, 1, and 2.
Observe how message delivery changes based on QoS settings.

## Publisher_qos.py output
[16:57:00] DEBUG | Sending PUBLISH (d0, q2, r0, m1), 'b'test/qos/6510301019/temperature'', ... (5 bytes)
[16:57:00] PUBLISH REQUESTED | QoS=2 | Message='hello' | msgid=1
Enter message to publish: [16:57:00] DEBUG | Received PUBREC (Mid: 1)
[16:57:00] DEBUG | Sending PUBREL (Mid: 1)
[16:57:00] DEBUG | Received PUBCOMP (Mid: 1)
[16:57:00] PUBLISHED | msgid=1
[16:57:54] DEBUG | Sending PINGREQ
[16:57:54] DEBUG | Received PINGRESP
[16:58:03] DEBUG | failed to receive on socket: [Errno 104] Connection reset by peer
[16:58:04] DEBUG | Connection failed, retrying
[16:58:06] DEBUG | Connection failed, retrying
[16:58:10] DEBUG | Connection failed, retrying

## Subscriber_qos.py Output

  client = mqtt.Client()
[17:02:28] DEBUG | Sending CONNECT (u0, p0, wr0, wq0, wf0, c1, k60) client_id=b''
[17:02:28] DEBUG | Received CONNACK (0, 0)
[17:02:28] Connected with result code 0
[17:02:28] DEBUG | Sending SUBSCRIBE (d0, m1) [(b'test/qos/6510301019/#', 2)]
[17:02:28] DEBUG | Received SUBACK
[17:02:46] DEBUG | Received PUBLISH (d0, q2, r0, m1), 'test/qos/6510301019/temperature', ...  (5 bytes)
[17:02:46] DEBUG | Sending PUBREC (Mid: 1)
[17:02:46] DEBUG | Received PUBREL (Mid: 1)
[17:02:46] RECEIVED | QoS=2 | Topic=test/qos/6510301019/temperature | Message=hello | msgid=1
[17:02:46] DEBUG | Sending PUBCOMP (Mid: 1)