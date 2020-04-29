---
layout: project_image_and_vimeo
permalink: /:title/
category: research

meta:
  keywords: "Image Manipulation, Image Processing, Research, Image Blending, Blending"

project:
  title: "Pyramid Blending"
  url: "https://willynolan.com/pyramid-blending"
  logo_type: "video"
  logo: "/assets/media/research/pyramid-blending/logo.webm"
  logo_backup: "/assets/media/research/pyramid-blending/logo.mp4"

images:
  - image:
    url: "/assets/media/research/pyramid-blending/first.png"
    alt: "Demonstration of pyramid blending on the beach and sky"
  - image:
    url: "/assets/media/research/pyramid-blending/second.png"
    alt: "Demonstration of pyramid blending on the beach and sky"
  - image:
    url: "/assets/media/research/pyramid-blending/third.png"
    alt: "Demonstration of pyramid blending on the beach and sky"
videos:
---
<p>
Representing an image as a <a href="https://en.wikipedia.org/wiki/Pyramid_(image_processing)"> pyramid </a> has a 
number of uses in image processing.  The general process is to downsize and blur an image multiple times creating a stack 
(or pyramid) of images each at a lower resolution. The resulting pyramid can be used for things such as object 
recognition at different scales and certain types of compression.
</p>

<p>
In this application the image pyramid is used to create a blended image.  The smaller and more blurry images in the 
pyramid serve as a low-pass filtered version of the image. A stack of these forms a Gaussian pyramid.
The Gaussian pyramid can be used to create a high-pass filtered version of the image called a Laplacian pyramid.
The formula for a Laplacian pyramid at a level $i$ is given as:
</p>

<p>
$$
\begin{aligned}
L_{i} = G_{i} - (K * G_{i})
\end{aligned}
$$
</p>

<p>
Where $K$ is the downsize and blur operator and $G_{i}$ represents an image from the Gaussian pyramid at level $i$.
Expanding and adding images from the Laplacian pyramid can recreate the original image with no data loss.
</p>

<p>
Effectively this means that a wider blend region can be used in low-frequency content and a 
narrower blend region can be used in high-frequency content such as edges.
</p>

<p>
This technique can be used to avoid a halo effect in images which make blend regions more noticeable.
</p>

<p>
This project implements the following academic papers:
<ul>
    <li>
        <a href="https://ieeexplore.ieee.org/document/1095851/authors#authors">The Laplacian Pyramid as a Compact Image Code</a>
    </li>
    <li>
        <a href="http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.56.690">A Multiresolution Spline With Application to Image Mosaics</a>
     </li>
</ul>

<p>
Both of which were authored by Peter Burt and Edward Adelson
</p>