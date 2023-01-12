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
<h3>Concepting and Design</h3>
Initially started with gathering a lot of reference, planning to develop an environment that could also be submitted for the Grads in Games Rising Star competition. My idea started as a desecrated church, pulling reference from abandoned gothic churches, occult rituals as portrayed by hollywood more than real life, and style reference from environment artists for Runescape. Having gathered a large reference board to pull from, limiting the amount I had to resort to aditional research so speeding up my process, I began working on concept developing, using <a href="https://www.stjohndivine.org/">The Cathedral St. John The Divine (www.stjohndivine.org, n.d.)</a> and the <a href="https://wh40k.lexicanum.com/wiki/Genestealer_Cult">Genestealer Cult (Lexicanum, 2022)</a> from Warhammer 40K as primary reference. 

I started with an initial blockout in Maya, which was exported very early into UE5 to do a lighting pass. This allowed me to get a better idea right from the beginning of the kind of atmosphere I wanted create with this piece. This blockout process was very iterative, refining and exporting it back into engine regularly to get an idea of the rough shapes I wanted and see how they looked when properly lit. I also discovered I could export Maya scenes to FBX via command line, so wrote a tiny script to remove some of the manual steps from this process. You can see progress shots below from left to right, and can see me trialling some squarer designs for the top section before deciding it didn’t fit the theme I was aiming for, scraping it, and replacing it with more layers of angled-roof towers. As you can tell from the iterations below, while my idea started as an interior I have shifted to an external shot as it’s what I felt more drawn too. Internal scenes can also require a lot of unique props for set dressing, whereas with externals I could design the asset to be able to create a modular kit to allow faster completion time and allow for easy construction in engine.

After these initial iterations I moved into zBrush to start doing a more detailed blockout. I decided to switch to zBrush for this as I want to try the zModeller brush, mostly because it has live booleans and I really enjoy the workflow they enable. Utilising these booleans allowed me to create a 'stamp' which could be used across the model to create repeating features like windows, speeding up my workflow and allowing fast iteration over the whole model, enabling me to easily adjust the size or shape of one window and then see that change across the entire model.

<div class="box alt">
	<div class ="column">
		<div class="row">
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_1.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_2.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_4.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_6.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Lighting_2.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Lighting_1.png" alt="" /></span></div>
		</div>
	</div>
</div>


<h3>Substance Designer</h3>
I knew that this project would use a tileable stone brick texture for a majority of the texture, so I begun looking into Substance Designer as a solution to creating this. I used <a href="https://www.youtube.com/watch?v=VMfVQs5G-gE">this tutorial (3dEx, 2018)</a> as a starting point, although broke away within the first few minutes to develop it independently. The tutorial mostly gave me an initial intro, answering key questions like how to add nodes and create a tileable tile-like texture, and from there I found the software very intuitive. I think my programming background helped significantly here, is it is essentially just <a href="https://www.tabnine.com/blog/what-is-visual-scripting/">visual scripting (Tabnine Team, 2021)</a> which I'm familiar with. 

To produce this final version, I have several main sections, as you can see in the photo of the Substance Designer graph below. Firstly, it's generates three variations of brick shapes, using several layers of blended noise to rough up the edge, and another layer of noise to create a raised highlight runnign across the brick, which is then fed into an existing node to create a tileable texture. The graph then diverges into two seperate branches, one to generate the normal, ambient occlusion (AO), and roughness map, and the other to generate the base colour.
The normal, roughness, and AO maps are generated by creating a grayscale map with different values per brick, a technique I use repeatedly to help break up the tiling, which is then used as an opacity mask to blend various noise maps together. This gives per brick variation as well as variation across the texture as a whole, while the blending of multiple maps helps to minimise any continuous shapes that extend over multiple bricks, which otherwise is a risk of using larger scale noise maps. 
generating the base colour is then handled in two seperate parts, the grout and the bricks. The grout layer is the simplest, with just a base colour, which is editable in engine, and a dirt colour which is overlayed with a simple noise mask. The bricks are more complicated, again using random grayscale maps with different values per brick as masks to apply three seperate base colours to the bricks, all of which are customisable in engine. Multiple layers of colour are then layered subtly over this, giving each brick unique patterning and colouring. These layers are generated by creating a map where each brick has a random colour, and then masking out parts of this with noise. This is done repeatedly, with each new layer stacked on top of the other, so that by the end each brick has many specks of different colour. Due to the layering this process has been broken out into two sub graphs, Multi_Speckled_Islands and Island_Rand_Colour, to keep the main graph more readable.

<span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Stone_Graph.png" alt="" /></span>
<div class = "box alt">
    <div class="row">
		<div class="6u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Multi_Speckled_Islands_Graph.png" alt="" /></span></div>
		<div class="6u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Island_Rand_Colour_Graph.png" alt="" /></span></div>
	</div>
    <!-- <i> From left to right; the initial kit displayed in engine with a recoloured brick material, and the reimported kit with trim details moved to a separate material, in this instance a much lighter version of the brick material to highlight details.</i> -->
</div>

As with all of my work, I took a very iterative approach for the development of this asset, regularly importing the texture into UE5 to see how it looked in engine before making further changes to refine it, several stages of which can be seen below.

<div class="box alt">
	<div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Brick_Progress_1.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Brick_Progress_2.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Brick_Progress_3.png" alt="" /></span></div>
	</div>
</div>


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

<h3>Kit Assembly</h3>
Elements weren't built to a grid due to being developed fluidly in zBrush, so the assets needed tweaking in order to fit cleanly to a grid. This was done by scaling the assets to fit the grid in Maya, referencing back to the original concept blockout to ensure relative size was roughly maintained. Edging panels were also added around the arched top of the windows in order to square off the asset and pivots were standardised to being in the bottom left corner to give consistency across the pack.

<h3>Detailing</h3>
With the kit assembled and in engine, I was able to assess the entire pack with textures for the first time. My conclusion was that it was definitely missing something. The single material meant the asset all blended into one mass, without any clear highlights or separation. Comparing my kit to my references I also found that I was missing a lot of the detailing and transitional pieces, and that the pieces ranged from plain brick lining such as I've including on the tower main window, to highly detailed baroque style border pieces. 
As a first step in fixing this, I went through my kit assets in Maya and moved specific UV islands to a separate material. This allows those elements to have a different material in engine, which I then utilised by creating a lighter brick variant to pick out and highlight these details, which you can see below.

<div class = "box alt">
    <div class="row">
		<div class="6u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Kit_1.png" alt="" /></span></div>
		<div class="6u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Kit_2.png" alt="" /></span></div>
	</div>
    <i> From left to right; the initial kit displayed in engine with a recoloured brick material, and the reimported kit with trim details moved to a separate material, in this instance a much lighter version of the brick material to highlight details.</i>
</div>

<h3>Conclusion</h3>
While there is certainly more I could do with this project, I've gotten a lot out of it already, more than the project was initially intended to provide! While I could definitely push it further by sculpting more fine detail for the assets, I'm happy with the state of the project as it stands and have decided to leave it here for now. It's been an invaluable learning experience for zBrush and Substance designer, and I am incredibly proud of the tileable stone texture I created. It's also given me significantly more practice UVing and forced me to think about how the asset will work with a tiled texture when unwrapping, a perspective that I expect to be helpful not just with tileables but with trim sheets too.

<h4>References</h4>
FlippedNormals (2019). Retopology for Beginners in Blender 2.8 - Retopo the Correct Way. [online] www.youtube.com. Available at: https://www.youtube.com/watch?v=CuQzPDs99yM [Accessed 3 Jan. 2023].

‌3dEx (2018). Substance Designer - Stylized Bricks. [online] www.youtube.com. Available at: https://www.youtube.com/watch?v=VMfVQs5G-gE [Accessed 3 Jan. 2023].

Tabnine Team (2021). What Is Visual Scripting & How It Works. [online] Tabnine Blog. Available at: https://www.tabnine.com/blog/what-is-visual-scripting/ [Accessed 3 Jan. 2023].

Lexicanum (2022). Genestealer Cult - Warhammer 40k - Lexicanum. [online] wh40k.lexicanum.com. Available at: https://wh40k.lexicanum.com/wiki/Genestealer_Cult [Accessed 4 Jan. 2023].

www.stjohndivine.org. (n.d.). Cathedral of Saint John the Divine. [online] Available at: https://www.stjohndivine.org/.