

# Bio-inspired underwater image enhancement


Following is a submission for the final project of [Natural and Artificial Vision](https://www.mccormick.northwestern.edu/computer-science/academics/courses/descriptions/396-19.html) course taught by [Dr. Emma Alexander](https://www.alexander.vision/emma) at Northwestern University during Spring 2023.

## Table of Contents
1. [Why is underwater imaging challenging?](#Why-is-underwater-imaging-challenging?)
2. [Example2](#example2)
3. [Third Example](#third-example)
4. [Fourth Example](#fourth-examplehttpwwwfourthexamplecom)

## Motivation
The ocean contains abundant resources and a rich ecosystem. Despite the fact that ocean covers 70% of earth's surface and plays a key role in supporting life on earth, it is still underexplored by humans. Exploring the secrets of ocean ecosystems has the potential to uncover fresh reservoirs of medicinal treatments, vaccines, food sources, energy solutions, and other valuable resources. Furthermore, it can serve as a wellspring of inspiration for developing innovations that imitate the remarkable adaptations of deep-sea creatures. Underwater imaging plays a crucial role in underwater operations by human or robot. However due to the suspended particles and light attenuation the underwater images often suffer from color distortion, low contrast and hazing effects. improving quality of underwater images will help with deep sea exploration and will help marine biologists to understand the life under sea better. Color distortion and hazing effect in the underwater images poses a difficult challenge for computer vision application. Further the artifacts observed in underwater images are quite different from what we observe in other images. Hence there's a need of an image enchancement technique that is tailored for underwaterimages. 
## Why is underwater imaging challenging?

To understand this let's go through a simplified underwater imaging model described in [[1]](#1). 

<!-- ![underwater_imaging_model](images/underwater_imaging_model.png)
*img_caption* -->

<figure>
  <img src="images/underwater_imaging_model.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 1: underwater imaging model [1].</figcaption>
  </center>
</figure>

From figure 1 above we can observe two key phenomenon that affect the quality of underwater images. 

1) **Scattering of light**: The light gets scattered due to presence of tiny suspended particles in water bodies. Scattering changes direction of light which makes the captured image hazy and noisy. 

<figure>
  <img src="images/hazing_effect.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 2: hazing effect in underwater images[1].</figcaption>
  </center>
</figure>

2) **Absorption of light**: 
The different wavelengths experience different level of absorption underwater, resulting in a pervasive color bias in underwater images. The uneven attenuation in the water leads to differences in how wavelengths of light are affected, ultimately impacting the overall color appearance of underwater photographs. This effect results in color distrotion in the captured images as shown in Figure 3.

<figure>
  <img src="images/color_distortion.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 3: color distortion in underwater images [2].</figcaption>
  </center>
</figure>

## Bio inspired vision system


In human visual system broadly there're two visual pathways of information namely Magnocellular and Parvocellular pathways [[3]](#3). The magnocellular pathway is responsible for transmitting signals related to large, rapidly moving objects, with a focus on low spatial frequency and high temporal frequency. This pathway, however, does not process color information. On the other hand, the parvocellular pathway carries information about small, slowly moving objects that are rich in color. It specializes in high spatial frequency and low temporal frequency perception. These pathways are illustrated in figure 4. 

<figure>
  <img src="images/m_and_p_pathway.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 4: Magnocellular and parvocellular pathways [3].</figcaption>
  </center>
</figure>

Zooming in to the retina of human eyes (Figure 5) each of these pathways are connected to different types of cells. The magnocellular pathway is connected to Parasol cells  and parvocellular pathway is connected to midget cell. 
<figure>
  <img src="images/retina_zoomed_in.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 5: Retina zoomed in [3].</figcaption>
  </center>
</figure>

The Parasol and Midget cells exhibit various properties which are very interesting. The Parasol cells are color blind and are more sensitive to low spatial frequencies. The Parasol cells are responsible for knowing **where** objects are. On the other hand Midget cells have a smaller receptive filed than parasol cells which makes them more sensitive to medium and high spatial frequencies. The midget cells are responsibele for knowing **what** objects are. The size comparison of these cells is shown in Figure 6.
<figure>
  <img src="images/Midget_vs_Parasol_cell.png" alt="my alt text"/>
    <center>
      <figcaption>Figure 5: Midget(left) vs parasol cells(right) [4].</figcaption>
  </center>
</figure>


Inspired by the two types of visual pathways Yan et al. [[2]](#2) developed a biological vision inspired framework for image enhancement in poor visibility conditions. 

## References
<a id="1">[1]</a> 
Zheng, Meicheng, and Weilin Luo. "Underwater image enhancement using improved CNN based defogging." Electronics 11, no. 1 (2022): 150.

<a id="2">[2]</a> 
Yan, Xiaohong, et al. "A novel biologically-inspired method for underwater image enhancement." Signal Processing: Image Communication 104 (2022): 116670.

<a id="3">[3]</a> 
Magnocellular and parvocellular pathways chapter from sensation and perception book https://pressbooks.umn.edu/sensationandperception/chapter/magnocellular-and-parvocellular-pathways/


<a id="4">[4]</a> 
parasol cell wikipidea page https://en.wikipedia.org/wiki/Parasol_cell