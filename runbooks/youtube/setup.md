# Live Streaming Setup

## Hardware
- Speaker Laptop
- Streaming Laptop
- Power Cables
- Video Adaptors for Hooking Streaming Laptop to venue AV System
- USB/USBc Hub
  - [Multi-Port](https://www.amazon.co.uk/Multi-port-Adapter-Delivery-MacBook-Spectre-Grey/dp/B07CPRWL41/ref=sr_1_3?keywords=usbc+hub&qid=1568149666&s=computers&sr=1-3) 
- Camera for Recording Speaker
  - Logitech HD Pro Webcam C920 [Amazon](https://www.amazon.co.uk/Logitech-Calling-Recording-Microphones-Adjustable/dp/B006A2Q81M/ref=sr_1_3?keywords=Logitech+HD+Pro+Webcam+C920&qid=1568149155&s=gateway&sr=8-3)
  - DSLR would also work for higher quality
- A video capture passthrough device (used to stream slides to streaming laptop) <br/>The video capture device allows to send the speaker's laptop screen/slides to the streaming laptop, and from the card itself output that same signal unchanged to the projector. What this passthrough allows to do is to configure the former input on OBS as a video signal that can be then mixed on the fly with the webcam one, creating that nice "picture in picture" effect, where the main content is the slide, with the additional speaker live video in the corner.
  - [Mirbox](https://www.amazon.co.uk/MiraBox-Capture-30FPS-1080P-Passthrough/dp/B07R5T29KN/ref=sr_1_1?keywords=Mirabox+USB-C+Capture+Card%2C+4K+30FPS%2CHD+1080P+60FPS%2CHDMI+Game+Video+Capture+Card+with+Mic+Input+and+HDMI+Passthrough+-+Compatible+with+Windows%2C+Linux%2C+macOS%2C+OBS+Streaming+for+PS3+PS4+Xbox+Wii+U&linkCode=g13&qid=1566382602&s=computers&sr=1-1)
  - [HDMI to USB3.0 Video Capture Dongle](https://www.dx.com/p/hdmi-to-usb3-0-video-capture-dongle-1080p-60-hz-audio-video-hd-capture-adapter-2023773)
  - [Cam Link](https://www.amazon.co.uk/Elgato-Cam-Link-Broadcast-AmazonBasics/dp/B07V6LNJWQ/ref=sr_1_3?keywords=elgato+camlink+4k&qid=1568149490&s=computers&sr=1-3) `// @domgreen I believe this does not allow what I mentioned`
- Wireless Mic + Receiver
  - [Fifine UHF Wireless Lavalier Microphone System with Bodypack Transmitter](https://www.amazon.co.uk/dp/B076X2P99W/ref=pe_1909131_77697001_tnp_email_TE_AMZLdp_1): this setup requires for the venue to still make their own mics available as after we tested the mic output for the room we realised the quality was quite bad. We might want to invest on a professional wireless mic and buy instead a USB sound-card to connect the analogue mic to, and use it for both the room and the live stream.

## Software
- [OBS Studio](https://obsproject.com/)
  - OBS is the main software we need to setup live streaming and recording
  - Scenes
    - Create a 'Holding Page' scene
      - Add a source for the `Holding Page` background image.
      - This is used whilst we are waiting to go live so that people know we will be live shortly
    - Create a 'LiveStream' scene
      - Add a source for the background image, this will be the backing of the video and we will overlay the other sources ontop.
      - We use a modified version of one of our slides taken from the standard Go slide deck  
      - Add a source `Speaker Laptop` this will come from one of the adaptors above
      - Add a source from a video capture device such as an external web cam.
