---
layout: plain
permalink: /:title/
category: research

meta:
  keywords: "Structured Light, Geometric Camer Calibration, Projector Calibration, Projection Mapping"

project:
  title: "Structured Light Calibration"
  url: "https://willynolan.com/structured-light-calibration"
  logo_type: "video"
  logo: "/assets/media/research/structured-light-calibration/logo.webm"
  logo_backup: "/assets/media/research/structured-light-calibration/logo.mp4"
---
<p>
There is a rich body of research surrounding camera calibration.  The process is usually broken up into 
<em>geometric</em> and <em>radiometric / photometric</em> calibration.
</p>

<p>
Projectors can essentially be thought of the inverse of a camera.  Instead of projecting a scene onto an image plane, 
they project an image plane onto an environment.
</p>

<p>
Due to this similarity, projector calibration is also a topic of interest in the interactive computer graphics field.
In a projection mapping context, usually what is meant by "projector calibration" is "putting content where it supposed 
to go in a real, 3D environment".
</p>

<p>
There are many strategies for performing camera calibration, but using structured light is a popular one.
</p>

<p>
It is built into both the <a href="https://madmapper.com">MadMapper</a> and <a href="https://www.disguise.one/en/">
disguise</a> software programs.
</p>

<p>
In this research, <a href="http://www.michaelwalczyk.com/">Mike Walczyk</a> and I explored the structured light 
process based on its original academic paper.
</p>

<p>
To explain this process imagine there is a room and for some reason you want to project an image directly where two 
walls meet.
</p>

<img class="research-post" src="/assets/media/research/structured-light-calibration/first.jpg" alt="Example room" height="442" width="500">

<p>
In the above picture that would be a corner of the room, for instance the corner located at the top of the above image.
For illustration purposes let's say the image you want to project is this simple checkerboard image with the letter F
to show distortion:
</p>

<img class="research-post" src="/assets/media/research/structured-light-calibration/second.jpg" alt="Content to project" height="500" width="500">

<p>
If you project that image directly onto the corner, the image will show obvious distortion.
</p>

<img class="research-post" src="/assets/media/research/structured-light-calibration/third.jpg" alt="Example Room" height="360" width="640">

<p>
Using structured light, which is essentially the simultaneous projection and photographing of different black and white 
images, this problem can be fixed.
</p>

<img class="research-post" src="/assets/media/research/structured-light-calibration/fifth.jpg" alt="Example Room" height="144" width="215">

<p>
A structured light process allows for the acquisition of a complete mapping (which the source paper refers to 
as $R$) from the camera pixels to the projector pixels.
</p>

<p>
This can be used to project content without distortion from the position of the viewer.
At the end of the process this image can look correct.
</p>

<img class="research-post" src="/assets/media/research/structured-light-calibration/fourth.jpg" alt="Final result" height="360" width="640">

<p>
Our research included a Python implementation as well as a projector/camera simulated.
</p>

<p>
The algorithm implemented was based on the academic paper:
</p>

<ul class="last-paragraph">
    <li><a href="https://ieeexplore.ieee.org/document/1240253">
        Multi-projectors for Arbitrary Surfaces Without Explicit Calibration nor Reconstruction</a> by J. -P Tardif et al.
    </li>
</ul>