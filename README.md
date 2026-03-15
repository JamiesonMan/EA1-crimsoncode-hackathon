# EA1-crimsoncode-hackathon
Extracurricular Assignment 1: Specifically for CPT_S427 to demonstrate an activity I participated in. That being Crimson Code 2026.

Project Description:
  The theme of the hackathion was "reinvent the wheel" me and my teammates worked on reinventing the Smart Ring Doorbell system to adaptively add facial recognition to new
  doorstep occupants. When an occupant enters the screen ideally the flask web interface would show you the contact's name, the time of some event (an event is a timestamped moment when
  someone enters or leaves frame), and the event description itself.

  What was unique about our project was that we had an edge raspberry Pi device working during our demo to capture live video. We utilized Youtube's infinite cloud storage and had the 
  PI device send an RMTP stream up to Youtube. From there we could simply embed the stream using an iFrame and capture frames off the stream programatically for inference on the backend.

  Hardware:
    Raspberry Pi Zero 2W
    Raspberry Pi Camera Module NoIR Wide (No Infared lens to support night vision)
    850nm IR Light
    Ethernet
    Usb C --> Ethernet Adapter
    Pi MicroUSB power cord.

  We utilized an SSH into Kamiak HPC provided for the event to train our models to recognize faces.

  What we actually finished developing:
    A working flask based web app to show the stream and live event tracking and event history.
    An AI model that was pretrained to detect humans in frame and basic events only identifying if someone came into view vs left view.
    We also finished an AI model that could detect our faces accurately but did not have enough time to tie the model into our web application for live inference.
    Additionally, we did not leave the Web application with the capabilities of adding new unrecognized faces to the model.

  Our algorithm for doing so would have consisted of:
    Someone enters frame as detected by the pretrained model.
    We capture bursts of images which auto crop to their face and transpose those subimages into our face recognition model we trained using pytorch.
    Our model then determines with some confidence if they are unknown or one of the known faces.
    If unknown continue collecting bursts of images for the future if the admin user decides to connect a name to this face.
    Autonomously train on the new face.

Code repositiory from the hackathon:
  https://github.com/Tallented-Code-bot/CrimsonCode-2026
  Note that AI LLM were permitted for use during the hackathon, we used various AI models to streamline development whilst we tackled Model creation and hardware implementations.

Members:
  Jamieson Mansker (ME)
  Noah Manuel
  Owen Moore
  Calvin Tallent

  
  
