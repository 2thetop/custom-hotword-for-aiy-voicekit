# custom-hotword-for-aiy-voicekit
Snowboy API for AIY Voice Kit

# Before How to use
Buy The AIY Voice Kit and complete the tutorial.

https://aiyprojects.withgoogle.com/voice/

Are you work your voice kit this program?
```
src/examples/voice/assistant_grpc_demo.py
```
If the demo has worked,next step.

# How to install

```
cd /home/pi/
# libatlas-base-dev need snowboy module.
sudo apt-get install libatlas-base-dev
git clone https://github.com/senyoltw/custom-hotword-for-aiy-voicekit

# copy snowboy module and sample program.
cp -ipr custom-hotword-for-aiy-voicekit/mod AIY-projects-python/src/
cp -ip custom-hotword-for-aiy-voicekit/assistant_grpc_demo_snowboy.py AIY-projects-python/src/examples/voice/
```

# How to use

```
cd AIY-voice-kit-python
src/examples/voice/assistant_grpc_demo_snowboy.py src/mod/resources/snowboy.umdl
```
Say "snowboy" and talk your google assistant!

sample log
```
pi@raspberrypi:~/AIY-voice-kit-python $ src/examples/voice/assistant_grpc_demo_snowboy.py src/mod/resources/snowboy.umdl
/opt/aiy/projects-python/src/aiy/_drivers/_led.py:51: RuntimeWarning: This channel is already in use, continuing anyway.  Use GPIO.setwarnings(False) to disable warnings.
  GPIO.setup(channel, GPIO.OUT)
[2018-05-29 03:27:47,216] INFO:recorder:started recording
Speak own hotword and speak
[2018-05-29 03:27:48,858] INFO:snowboy:Keyword 1 detected at time: 2018-05-29 03:27:48
Listening...
[2018-05-29 03:27:52,702] INFO:speech:transcript: what
[2018-05-29 03:27:52,707] INFO:speech:transcript: what's
[2018-05-29 03:27:52,709] INFO:speech:transcript: what to
[2018-05-29 03:27:52,711] INFO:speech:transcript: what is
[2018-05-29 03:27:52,713] INFO:speech:transcript: what city
[2018-05-29 03:27:52,715] INFO:speech:transcript: what did you
[2018-05-29 03:27:52,717] INFO:speech:transcript: what is your
[2018-05-29 03:27:52,719] INFO:speech:transcript: what did you want
[2018-05-29 03:27:52,721] INFO:speech:transcript: what is your name
[2018-05-29 03:27:52,722] INFO:speech:transcript: what  is your name
[2018-05-29 03:27:52,725] INFO:speech:transcript: what  is your name
[2018-05-29 03:27:52,727] INFO:speech:transcript: what is your name
[2018-05-29 03:27:52,729] INFO:speech:event_type: 1
[2018-05-29 03:27:52,735] INFO:speech:transcript: what is your name
You said " what is your name "
Speak own hotword and speak
```

# Make your own hotword
Make your own hotword this site. 
and download your voice kit [hotword].umdl
(how to make your hotword by snowboy, google it ^^!)

https://snowboy.kitt.ai/

and run program argument your hotword

```
cd AIY-voice-kit-python
src/examples/voice/assistant_grpc_demo_snowboy.py [hotword].umdl
```