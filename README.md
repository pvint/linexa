Linexa - Simple Philips Hue emulator for accepting commands from an Amazon Echo to control whatever from a Linux device.

Primary purpose: Control LED lighting on a Raspberry Pi using voice commands to Alexa without using any heavy libraries or applications.

Goals: K.I.S.S.
- To be configured by simple plain-text config file
- If there's any heavy lifting to do, do it on the script that is called by this

I summary, this daemon should:
1. On startup read the config file and have "devices" ready for an Echo to discover (or other assistant device)
2. Listen and reply to the UPNP broadcasts
3. Listen to HTTP requests to do *whatever*, and simply do *whatever*
4. Keep it light and fast


Note: Totally inspired by https://github.com/bwssytems/ha-bridge  This thing is really really great! My main motivation for doing this is that ha-bridge relies on using the web interface to make config changes and that doesn't tend to work for me.
