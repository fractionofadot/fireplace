# Automating my Fireplace

I was laying down on my couch after a long, exhausting day. It was cold and I wanted to turn on the fireplace. I was feeling too tired to get up and turn it on (or even get up to fetch the remote for it). I just wanted to tell my virtual assistant to "turn on the fireplace". And since that capability doesn't already exist, I decided to engineer a solution to do just that. 

Since my fireplace comes with a remote control, I decided to listen to the signals it emits and see if I can mimic them on command. 

I purchased some Software-Defined Radio (SDR) hardware (the NooElect NESDR Mini 2) to listen to the frequency that my remote control emits. After I installed the driver and SDR software called "CubicSDR", I was ready to go.

Normally I would locate the frequency information using the FCC number of the remote control. 

https://www.fcc.gov/oet/ea/fccid

But since the FCC id wasn't visible on the remote (the battery cover containing that information was missing), I opened it up and found the transmitter right away. It is a JD R315A. I looked up a datasheet for that transmitter and found the center frequency is 303.875MHz with a tolerance of +- 75 MHz.

So in CubicSDR I set my frequency to that range and pressed the "on" button on the controller.

