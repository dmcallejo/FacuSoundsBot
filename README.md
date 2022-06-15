# FacuSoundsBot
Bot de Telegram con sonidos de Facu Díaz. Basado en el proyecto de azero-dev/FacuSounds

[![Build Status](https://travis-ci.org/dmcallejo/facusoundsbot.svg?branch=master)](https://travis-ci.org/dmcallejo/facusoundsbot) [![Docker Automated build](https://img.shields.io/docker/automated/dmcallejo/facusoundsbot.svg)](https://hub.docker.com/r/dmcallejo/facusoundsbot/) [![Docker Build Status](https://img.shields.io/docker/build/dmcallejo/facusoundsbot.svg)](https://hub.docker.com/r/dmcallejo/facusoundsbot/) [![Docker Pulls](https://img.shields.io/docker/pulls/dmcallejo/facusoundsbot.svg)](https://hub.docker.com/r/dmcallejo/facusoundsbot)

Todos los audios deben ser comprimidos con estos parámetros:
```
ffmpeg -i $INPUT -map_metadata -1 -ac 1 -map 0:a -codec:a libopus -b:a 128k -vbr off -ar 48000 $OUTPUT
```

Comando para comando externo en Audacity:
```
ffmpeg -i pipe:0 -map_metadata -1 -ac 1 -map 0:a -codec:a libopus -b:a 128k -vbr off -ar 48000 "%f"
```
