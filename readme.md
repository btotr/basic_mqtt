#Basic MQTT setup

##prerequisite 
- mosquitto (act as a broker 'brew install mosquitto' on a mac)
- webpack (npm install -g webpack)

## install
```
npm install
webpack node_modules/mqtt/mqtt.js ./browserMqtt.js --output-library mqtt
```

## run

```
mosquitto -c ./mosquitto.conf
python -m SimpleHTTPServer
```

## usage

open you web browser on the following address: http://localhost:8000/

```
mosquitto_pub -t "mqtt/demo" -m "message payload" -q 1
```