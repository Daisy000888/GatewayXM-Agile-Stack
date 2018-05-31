FROM resin/raspberry-pi-alpine-python:3.6-slim

ENV FW_FILE = "firmware_v2.bin"
ENV FW_ID = "0x01"

ADD send_ota.py /
ADD {$FW_FILE} /

RUN pip install paho-mqtt

CMD [ "python", "send_ota.py", "--broker", "agile-kura", "--intopic", "sensor_node_in", "--outtopic", "sensor_node_out", "--bin", {$FW_FILE}, "--id", {$FW_ID} ]
