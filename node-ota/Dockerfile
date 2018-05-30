FROM resin/raspberry-pi-alpine-python:3.6-slim

ADD send_ota.py /
ADD firmware.bin /

RUN pip install paho-mqtt

CMD [ "python", "send_ota.py", "--broker", "agile-kura", "--intopic", "sensor_node_in", "--outtopic", "sensor_node_out", "--bin", "firmware.bin", "--id", "0x01" ]