---
layout: post
title: Cathedral
# description: Feugiat amet 
# image: assets/images/castan.png
# video: https://www.youtube.com/embed/lYTyDO7lnCA
released: December 2022
# storefront: Steam
# storeurl: https://store.steampowered.com/app/1836170/Castan/
# roles: Producer
display: false
---
Project intro, outline

Initially wanted to focus on atmosphere. 
Inpsired by gothic architecture and mood, also pulling from 40k for symbolism and atmosphere
focused primarily on building itself, neglected shot composition until later in the project

Have designed asset to be able to create a modular kit to allow faster completion time (it's much quicker to unwrap an element once than 16 times) and allow for easy construction in engine. Hope to construct kit in such a way that building new buildings in engine would be quick and efficient.

<h3>Substance Designer</h3>
I knew that this project would use a tileable stone brick texture for a majority of the texture, so I begun looking into Substance Designer as a solution to creating this. I used <a href="https://www.youtube.com/watch?v=VMfVQs5G-gE">this tutorial (3dEx, 2018)</a> as a starting point, although broke away within the first few minutes to develop it independently. The tutorial mostly gave me an initial intro, answering key questions like how to add nodes and create a tileable tile-like texture, and from there I found the software very intuitive. I think my programming background helped significantly here, is it is essentially just <a href="https://www.tabnine.com/blog/what-is-visual-scripting/">visual scripting (Tabnine Team, 2021)</a> which I'm familiar with. As with all of my work, I took a very iterative approach for the development of this asset, regularly importing the texture into UE5 to see how it looked in engine before making further changes to refine it, several stages of which can be seen below.

<div class="box alt">
	<div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_1.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_3.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_5.png" alt="" /></span></div>
	</div>
</div>

To produce this final version, I have several main sections, as you can see in the photo of the Substance Designer graph below.
<span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Stone_Graph.png" alt="" /></span>

Early importation into engine allowed me to set up the engine material early and refine it, for example I set it up so it tiled, then discovered I dislike how the default tiling works. My initial, and the simplest, implementation scaled the texture in the objects local space, meaning that each object required a material with a different scaling value in order to have a consistent brick size across models. This seemed like it would require a lot of tinkering and wouldn't scale well, so I put together a quick script to scale the texture in world space rather than local space for each object, meaning that I can have one primary material that controls the brick scale. When an asset has a normal or AO map a new instance of the primary material can be created, and it has optional slots to insert a custom AO and/ or normal map.
<span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Primary_Mat.png" alt="" /></span>

<h3>Retopology</h3>
I used this project as an opportunity to investigate different workflows and processes, practicing concepting & in both Maya and zBrush, learning and eperimenting with the zModeller brush. Also investigated retopology across the two platforms, spending a significant amount of time experimenting with retopology in zBrush using zRemesher, DynaMesh, and zSphere, as well as retopology in Maya using QuadDraw, and some light research into retopology in Blender as well. 

In zBrush, I found that using dynamesh followed by zremesher provides very clean, regular topology. While excellent for curved surfaces, such as a lot of organics, this regularity has limitations. The topology can be guided to create good flow around features, such as eyes, and while the density can be guided to an extent with weight painting it often requires adjustment after, especially for hard surface work. I found it was adding much more geometry than needed in order to keep uniformity, bloating the polycount and requiring me to manually remove edge loops to fix this. I found that this process of tinkering with zRemesher settings to get a good remesh and then going in to delete edge loops manually was actually no faster than doing the retopology manually in Maya, provided less control, and could actually take longer if it took multiple iterations to find good settings for zRemesher, especially if the mesh required dynameshing first. <br>
I also looked into using zSphere, however after some time of using it it appears to be equivalent to Maya's quaddraw, however lacks features and is harder to use, making it a less preferably option to Maya.
Lastly, I investigated retopology in Maya using quaddraw. I'm aware this is the industry standard, so I wanted the context that knowing about the other retopology options would provide me, as it allowed me to make an assessment whether Maya was the industry standard for retopology for a good reason, or if other options were actually better. <br>
From my experimentation, while in principle it is very similar to zBrush's zSphere, I found it had a couple main advantages. First, being able to extrude edges, combined with live surface, in quad draw is significantly faster than placing individual vertices in zSphere, and makes it significantly easier to create level edge loops across a model. I want to emphasise how much faster quad draw is, especially utilising the dynamic vertex merging when using edge extrusions, and in my opinion this is the primary advantage it has over zSphere. It is also much easier to read, with quad draw visibly generating faces, as opposed to zSphere visually generating only edges and vertices.<br>
Although I did not experiment with blender, I did do some research into it and found that the workflow was again very similar to quad draw, but required more setup, adding multiple modifiers to an object and customising the objects texture in order to get equivalent functionality. <a href="https://www.youtube.com/watch?v=CuQzPDs99yM">This YouTube video from the channel FlippedNormals (FlippedNormals, 2019)</a> gives a good intro to retopology in blender. While I will likely look into this in the future if I want to monetise my personal artwork, it doesn't seem to offer any significant benefits over quad draw in Maya.

With this reserach in mind, I adopted quad draw for the rest of the retopology in this project as there are no assets that I would consider ideal for zRemeshing, and Maya is more of an industry standard than Blender.

<div class = "box alt">
    <div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Main_Window_Retop_1.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Main_Window_Retop_2.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Main_Window_Retop_3.png" alt="" /></span></div>
	</div>
    <i> From left to right, a quick retop done with zRemesher, retop done with zSphere, and retop done in Maya with Quad Draw. Notice the density and number of redundant edge loops in the zRemesher version, and the unaligned edge loops in the zSphere version, a problem that occurs due to the nature of the tool.</i>
</div>

<h4>References</h4>
FlippedNormals (2019). Retopology for Beginners in Blender 2.8 - Retopo the Correct Way. [online] www.youtube.com. Available at: https://www.youtube.com/watch?v=CuQzPDs99yM [Accessed 3 Jan. 2023].
‌
‌3dEx (2018). Substance Designer - Stylized Bricks. [online] www.youtube.com. Available at: https://www.youtube.com/watch?v=VMfVQs5G-gE [Accessed 3 Jan. 2023].
‌
Tabnine Team (2021). What Is Visual Scripting & How It Works. [online] Tabnine Blog. Available at: https://www.tabnine.com/blog/what-is-visual-scripting/ [Accessed 3 Jan. 2023].
‌