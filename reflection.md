# Reflection

## Activity Description
  We attempted to reinvent the ring door bell camera at the Crimson Code Hackathon. The theme was "Reinvent the Wheel". Although we did not win, we did partially implement our initial idea. Specifically we wished to allow dynamic contact list of recognized faces and timestamped events identifying the contacts within frame. We used a physical edge device and found strategies to avoid locally saving video footage and instead use other methods.
## Technical Decisions
THe raspberry pi zero 2w is a great module for handling 1080p video footage. We decided to use 720p footage to increase fps to 60 frames with minimum thermal problems.
We also used a heatsink and attatched it to the small PI device utilizing also a simple copper plating and thermal paste to the CPU itself.

We initially setup the PI device and attempted to connect to the WSU Guest Wifi and immediately were stumped on why a connection would not work.
This problem also did not work on the WSU Enterprise network for WSU Wireless.

To resolve this soltion as soon as possible I had the idea to configure my laptop to share its connection to the WiFi for the specific ethernet connection between the PI device and the laptop. After configuring this on my windows machine, the PI device correctly routed to the laptop and used its connection to the WSU Wireless WiFi.
We suspected perhaps that WSU configured their network to restrict the raspberry PI OS. 
## Contributions
I brought all the hardware used regarding the PI device and the camera. Additionally, I tackled the idea of using YouTube to hold our live video footage free of charge.
Additionally I worked on implementing the Flask Application and created the schema for the sqlite database we used. I was not involved in the Kamiak job creation, or pytorch implementation.
I also created systemd services and timers on the PI device to auto send RMTP stream to youtube. Additionally to capture thermal activity and log that incase of a shutdown we would know if it was from thermal problems.
## Quality Assessment
We did successfully build a web app that showed the lvie stream in real time. Additionally, we successfully attached a pretrained human recognizer model to trigger an event occuring. We successfully created a stand alone model which detected faces that we personally trained and collected data for. Although we could not fully integrate this into our web interface. Overall our project was technically unqiue due to the hardware edge device we used. Many other groups were fully software based.
