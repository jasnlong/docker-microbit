# docker-microbit
This is a Docker image build for pxt-microbit editor on node.js server.

pxt-microbit is a Microsoft Programming Experience Toolkit (PXT) target that allows you to program a BBC micro:bit. More detail see https://github.com/Microsoft/pxt-microbit

To run the editor, you must mapping tcp 80 port when run the container first time, use command below:
```
docker run -p 80:80 --device /dev/ttyUSB0:/dev/ttyUSB0 --name microbit -d leejoneshane/microbit
```
If the dev server is running then go to http://docker_host_ip

To use pxt, please read the [documents](https://makecode.com/cli). ex: monitor UART
```
docker exec microbit serial
```
