---
category: research

meta:
  keywords: Respectrable, Ableton, Max, Max for Live
  description: Respectrable project overview

project:
  title: Respectrable
  preview_main: "/assets/media/research/respectrable/preview.webm"
  preview_backup: "/assets/media/research/respectrable/preview.mp4"

figures:
  - type: figure
    content:
      - src: "/assets/media/research/respectrable/first.jpg"
        alt: "Live Object Model Diagram"
        caption: Live Object Model Diagram
        width: 1280
        height: 750

  - type: figure
    content:
      - src: "/assets/media/research/respectrable/second.jpg"
        alt: "Screenshot of Respectrable being developed"
        caption: Screenshot of Respectrable being developed
        width: 1280
        height: 750

  - type: video
    id: "354581391"

sections:
  -
    - p: "Although most Ableton Live users probably only use it to make music, it was also one of the first Digital 
Audio Workstations (DAW) to offer a fully programmatic interface and probably still offers the best live 
performance abilities of any DAW."

  -
    - p: 'Live officially supports programmatic access to every knob, button and and slider through the 
<a href="https://docs.cycling74.com/max8/vignettes/live_object_model">Live Object Model (LOM)</a>.'

    - p: "As is shown in the first figure, the LOM can be a bit of a maze because of the large number of 
parameters available in Live."

    - p: "There is a learning curve to figuring out how the object hierarchy works but, 
once figured out, each and every property of a Live set is reachable programmatically."

    - p: 'The repeated necessity of a scriptable, real-time audio engine, and specifically one that could be used 
wirelessly through <a href="http://opensoundcontrol.org/introduction-osc"> Open Sound Control</a> (OSC) led to
the creation of <a href="https://github.com/computersarecool/respectrable">Respectrable</a>.'

  -
    - p: "Respectrable is a Max for Live device that facilitates easily accessing the Live Object Model through 
Javascript or Max objects."

    - p: "The featured video shows a very simple example of bi-directional control between Live and a graphical 
application."
---