---
layout: post
title: Reflective Journal
description:
image:
nav-menu: true
show_tile: true
tile_order: 3
---
<h2>Late February</h2>
Started on my next project, wanting to focus on composition and lighting primarily. As I said in my previous project composition I neglected until the very end and is one of the areas I'm least familiar, so this project can act as dedicated practice. As always, I started with a lot of research, I'd just finished reading The Religion by Tim Willocks, and wanted to do something inspired by this, and knew I wanted to do an environmental piece. The book is set in the 16th century during the siege of Malta, so after a lot of research into the period I settled on doing a historical Moroccan Riad, a style of traditional house with narrow rooms surrounding a central courtyard. I also wanted to keep the project small in both scope and physical size so I could focus on lighting and composition without being overwhelmed by other aspects, so this concept worked perfectly.

After settling on a concept and gathering more focused reference, I began blocking out a scene, iterations of which you can see below. While I started blocking out by feel and reference alone, I also used overlays for both the rule of thirds and golden ratio to help guide asset placement, while regularly switch my camera angle and making sure the layout still made sense as an actual place.
<div class="box alt">
	<div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Riad_Progress_1.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Riad_Progress_2.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Riad_Progress_3.png" alt="" /></span></div>
	</div>
</div>

<h2>January - Mid-February: Judgement Time</h2>
This was an intense time, I spent it wrapping up the cathedral, getting it finished and prepped for both my uni deadline and the Grads In Games Environment Art competition. While I didn't crunch, the time I normally spend keeping this up to date was instead spent on the doing the write up for the project. You can checkout <a href="{{ site.baseurl }}/2022/11/01/Cathedral.html">the write up here</a> or check it out <a href="https://www.artstation.com/artwork/QndJ6d">on my Artstation here.</a>

<h2>26/12/22 - 30/12/22</h2>
<span class="image left"><img src="{{ site.baseurl }}/assets/images/Cathedral/Chain_Box_Cross.png" alt="" /></span>

Logo retopology, experimenting with different methods for doing lowpoly for chains. Trialled using a surrounding box, and using two intersecting planes forming a cross aligned with the chain links. The surrounding box did not look good even when using an opacity mask, while the cross method worked incredibly well. You can see the comparison in the image to the left, with the cross at the front and box behind, and the difference is obvious. The cross method also has half the polycount, which is a nice bonus. I also separated the main logo and each chain section into different objects and made use of the <i>Match By Mesh Names</i> option when baking maps to minimise artifacting from the chains on the main logo body, which you can see is present in the screencap on the left.

The rest of the week was spent finishing the logo lowpoly and unwrap, as well as doing the same for another major asset.

<p style="margin-bottom:3cm;"></p>

<h2>12/12/22 - 16/12/22</h2>
More thorough investigation and experimentation with retopology in zBrush, experimenting extensively with dynamesh, zRemesher and zSphere. My conclusion is that these tools will be invaluable, under the right circumstances. For example, I can see these tools saving significant amounts of time with organic assets or assets with more uniform topologically density, however it struggled to appropriately vary topology density with the assets I was using, even when using the Topology Density tool to paint which areas should be more or less dense. I believe this was, at least in part, due to the nature of the assets I was using, assets where a large part of the surface could be effectively covered by single rectangular strip, while zRemesher aims to retop everything with squares, resulting in higher poly density that if done manually. While I did experiment with using zRemesher to get a rough starting point, then going back in and manually deleting unnecessary edge loops, I found this wasn't actually any faster than just doing the retopology manually from the beginning, and could be more temperamental as it required experimentation and adjustment of settings in order to get a suitable starting point.

After reaching this conclusion, and consulting with an academic, I started conducting research into other topology tools in both Maya and Blender, and after further experimentation, returned to Maya where I will likely complete the rest of the retop for this project. I chose this over Blender as, while from my brief experience with it I personally prefer Blender, Maya is currently the industry standard so I wish to focus my learning there, although I will likely dedicate some time to becoming more familiar with Blender before graduation. I like the flexibility that knowing multiple different programs gives me, just because a piece of software <i> can </i> do the specific task I need, it doesn't mean it is the <i>best</i> tool for the job, and I can't know what the best tool is if I don't know which ones are available.

<p style="margin-bottom:3cm;"></p>

<h2>05/12/22 - 09/12/22</h2>

Started playing with Substance Designer, creating a tileable stylised brick material. This was a lot of fun, and honestly way easier to get into than I had feared, I think my programming background really shines through here, letting me get to grips with  the node based process quickly. After importing this into engine, the standard tiling method, honestly, annoyed in how limited it was, I didn't want to have to use a slightly differently scaled material for each object of a different size! That seemed like a lot of busy work, so I spent a little time putting together a script so that the textures now scale in world space rather than object space, meaning any object I apply the material too will have bricks of the same size, with no extra work on my part. This is limited for now, working only in the world planes, as the effort to make it work in a general case isn't worth it when I don't currently have a use case for that functionality.
As always with my work, this was a very iterative process, with multiple rounds of importing the asset into engine to better gauge how it looked in the situation it would be used.

<div class="box alt">
	<div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_1.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_2.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_3.png" alt="" /></span></div>
	</div>
	<div class="row">
		<div class="6u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_4.png" alt="" /></span></div>
		<div class="6u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Tileable_Bricks_5.png" alt="" /></span></div>
	</div>
</div>

<p style="margin-bottom:3cm;"></p>

<h2>21/11/22 - 02/12/22</h2>

This week I began the first detail pass of my Cathedral scene with zBrush, utilising Arraymesh and Live Booleans which, especially when combined, are wonderful. They've allowed fast iteration over the whole model, enabling me to easily adjust the size or shape of one window and then see that change across the entire model. I've also done a second lighting pass with this updated model, which you can see below.

<div class="box alt">
	<div class="row">
		<div class="6u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Lighting_1.png" alt="" /></span></div>
		<div class="6u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Lighting_2.png" alt="" /></span></div>
	</div>
</div>

I have also been experimenting with retopology in zBrush on a single window piece, as I was unsure how long retopology would take. This small scale allows me to answer that question, letting me better estimate the project timeline and ensure I hit my deadline. My initial thought was to bake te detail down to plane, however this bake did not come out well. Then aiming for single chamfer between levels, and after a fair bit of experimentation I got a good low poly model that bakes well by using zSphere. I decided to use zBrush for retopology here as I wanted to experiment with the tools, as the more tools I know the more flexible I am and the better I can choose the correct tool for the job. Also, the less switching I have to do between software the faster and smoother my workflow is likely to be; the export/ import process is slow and tends to be an area that errors can occur.

Throughout my process, i've intended the asset to be modular, allowing faster completion time (it's much quicker to unwrap an element once than 16 times) and allow for easy construction in engine. I aim to construct this kit in such a way that creating new buildings in engine is quick and efficient, allowing me or a designer to quickly develop new assets in engine.

I also realised I neglected planning my shot composition and final presentation, so have done some quick sketches to improve and add more visual interest to the scene, seeking to frame the building as focal point. For reference, I've been looking at the third piece <a href="https://www.artstation.com/artwork/8w4Agn">here</a> by artist Zahir Aghakhani for inspiration, trying to block off one side of the screen and angle it in to lead eye to the focal point. I really enjoy with this piece how the diagonals run consistently from top left to bottom right, even the rain is slanting slightly in that direction, pulling the viewer in that direction, and use of broken & picked up lines from the tarpaulin to the car in the left of frame to lead the eye to the focal point.

<div class="box alt">
	<div class="row">
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Lighting_2.png" alt="" /></span></div>
		<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Composition_1.png" alt="" /></span></div>
		<div class="4u$"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Composition_2.png" alt="" /></span></div>
	</div>
</div>

I have a lot more ideas for what I could do here, including adding a landing platform to the end of the bridge, designed so it looks like a smaller, original platform that has then been expanded in a make-shift manner. This would give me an opportunity to do more environmental storytelling, something I would be really keen to include, as well as do a small walkthrough of the scene, going from the landing pad, up stairs onto the bridge, allowing a slow reveal of the main cathedral as the player mounts the stairs. While I am keen to do this, I am very aware of feature creep and don't want the project to get away from me, so it is an expansion that will go into the backlog for now as the rest of the piece is higher priority.

Finally, totally just to brag but I had a very proud mentor moment, walking past one of my old mentees confidently explaining a process they hadn't heard of two months ago to a peer. One of several reasons I want to do more mentoring going forward, that is such a rewarding feeling!

<p style="margin-bottom:3cm;"></p>

<h2>11/11/22 - 18/11/22</h2>
I began collecting reference for my next module, planning to develop an environment that could also be submitted for the Grads in Games Rising Star competition. My idea started as a desecrated church, pulling reference from abandoned gothic churches, occult rituals as portrayed by hollywood more than real life, and style reference from environment artists for Runescape. I love their style and am planning to apply there upon graduation, so it seems sensible to reference their work while designing my own. I've gathered a large reference board to pull from, probably larger than strictly needed, but it means I have to resort to web searches less than I otherwise would, speeding up my process.

Working on my environment concept, I started with an initial blockout in Maya, which I exported super early into UE5 to do a lighting pass. This allowed me to get a better idea right from the beginning of the kind of atmosphere I wanted create with this piece. This blockout process was very iterative, refining and exporting it back into engine regularly to get an idea of the rough shapes I wanted and see how they looked when properly lit. I also discovered I could export Maya scenes to FBX via command line, so wrote a tiny script to remove some of the manual steps from this process. 
You can see progress shots below from left to right, and can see me trialling some squarer designs for the top section before deciding it didn't fit the theme I was aiming for, scraping it, and replacing it with more layers of angled-roof towers.

As you can tell by now, while my idea started as an interior I have shifted to an external shot as it's what I felt more drawn too, and I believe it will be more reasonable and flexible in terms of project scope. While an interior could need a good amount of props to decorate, with the exterior I'm hoping to be able to repeat a lot of detail and shapes that I create, saving me a lot of time.

<div class="box alt">
	<div class ="column">
		<div class="row">
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_1.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_3.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_2.png" alt="" /></span></div>
		</div>
		<div class ="row">
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_5.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_4.png" alt="" /></span></div>
			<div class="4u"><span class="image fit"><img src="{{ site.baseurl }}\assets\images\Cathedral\Cathedral_Blockout_Progress_6.png" alt="" /></span></div>
		</div>
<div>

After these iterations I was happy with how my rough blockout was looking, and have now moved into zBrush to start doing a more detailed blockout, the start of which can be seen below. I decided to switch to zBrush for this as I want to try the zModeller brush, mostly because it has live booleans and I really enjoy the workflow they enable. Having spent a day starting to get my head around it, it's exciting and promising, I'll need longer to see but I may actually prefer it over Maya for hard surface, it feels closer to Blender which is positive. Now that I've got a boolean constructed to generated the stepped arches around the door frame, I'm planning to duplicate it and use it for the window cut outs. This should give a consistent feel to the building by having repeated shapes and motif's, while also saving me time.

<p style="margin-bottom:3cm;"></p>

<h2>September, October, and The Future</h2>
This initial period of my masters has been focused around 'finding the passion', experimenting and finding the area of game art that I am most drawn to, and then planning my development pathway with this in mind.
Moving forward I will be scaling down the time committed to developing my 2D skills, as I was spending a quarter of my time on it. While still a useful aspect, it is not an area I am as passionate about, so while I continue to attend first year concept art lectures the time I spend practising these concepts will be reduced. This will allow me to dedicate more time to the most compelling and important aspects for my future career, primarily the development of assets and environments in Maya, zBrush, and in engine.

While the game project I participated in did reveal several useful insights into the importation of assets into Unity, it proved to be more of a distraction than a developmentally valuable process. This was due to already having the broader game development and pipeline knowledge, and while practice makes perfect, I want to focus on developing my art as it is currently the weaker skill set. This has driven me to ensure I am able to focus on personal art-specific projects, rather than cooperative game projects, as I move forward with my course and future modules. While the experience of developing a game in a team would prove invaluable to some, it isn't what I need most for my development at the moment, and engine implementation experience can come from personal projects, without the overhead that comes with working in a team.

I hope to continue mentoring into the next module as I thoroughly enjoy it, find it very rewarding, and enjoy helping others with their development. I plan to continue providing what help I can to peers, and have also reached out to senior staff at Falmouth University Games Academy, where I am doing my masters, offering to help out with the undergrad game development projects in a mentor role. It also acts as good evidence of suitability for senior positions, as I will want to pursue this path moving forward. I hope that this suitability, drawn from mentorship, strong interpersonal skills, and management and planning skills from production experience, will help me to stand out when applying for junior positions given there is a shortage of seniors, so my hope is that a junior who could be trained and mentored into a senior role will be an attractive prospect. I have also found teaching is one of best ways to cement and test what you have learnt, adding another way in which it is beneficial for my personal development, as well as the development of those I mentor.

Most likely, I will continue writing these reflective posts, although will likely write them much quicker and more loosely as so far these have been for an assessment. As I carry out reflective practice anyway it makes sense to have a written, demonstrable record of my process and practice, regardless of whether I am assessed on it.

<p style="margin-bottom:3cm;"></p>

<h2>Week 5: 17/10/22 - 23/10/22</h2>
<i>The model this section refers to can be found on my Artstation, at <a href="https://www.artstation.com/artwork/xYnQKY">https://www.artstation.com/artwork/xYnQKY</a></i>

I decided to downscale my ongoing side project to prioritise practising UVs and learning zBrush over making a complicated model. This smaller scope allows me to work iteratively on the project, giving me the time to complete a stage and then redo it to practice lessons learned during the first pass, and act on feedback received from both peers and academics. For example, I unwrapped the blockout in order to practice manually UV unwrapping, which allowed me to then create better UVs faster when it came to actually unwrapping the low-poly, while also allowing me to create the low-poly with considerations for how it would unwrap, rather than just creating it and the UVs being an afterthought.

The blockout was then exported to zBrush to sculpt wear onto the metal and grain onto the wood. Designing the asset with panelling allowed me to overlap UVs to save on creation time, however I instead used the panelling to do batches of practice and reflection. This facilitated experimentation and direct comparison, and led to rapid improvements with the final panel being of a significantly higher quality than the first one. This was partly due to selection of a better brush and preview material, and partly from being more familiar with the software, both through practice and through arranging a software 'masterclass' from an assistant lecturer who specialised in zBrush.

<p style="margin-bottom:3cm;"></p>

<h2>Week 4: 10/10/22 - 16/10/22</h2>
During a consultation with other artists on our team, a bad habit I have developed was highlighted, which was always trying to make an asset out of a single mesh. While I have found modelling an asset from a single mesh reduces the likelihood of producing overlapping faces, which could cause artifacting and take up additional space when UVing, a section of a model can often be easier and quicker to model individually. This single-mesh-manipulation can also produce undesirable topology compared to modelling parts separately, potentially increasing the polycount of a model significantly. As such, I aim to actively consider whether a part of my model would be better to model separately moving forward, as while there are certainly use cases for the single-mesh method, it should not be the method I <i>always</i> use.

I have also continued mentoring two artists on our team who are new to both 3D art and game development, supporting their use of Maya and Substance, as well as continued support with version control using Git. I demonstrated importing a completed asset into Unity, covering model and texture export and importation, prefab setup, material creation and application, and finally pushing these changes to the projects Git server. The reason I have taught them this workflow, rather than dropping raw models into scene, is to allow changes to be made to models in the future without having to make any changes in a scene. The more people making changes to one scene (or more specifically, the same binary file), the more likely we are to encounter merge conflicts (Atlassian, n.d.), which it's always best to avoid as they often result in loss of work when merging binary files.

I also did an initial lighting pass for our game, utilising a three-point lighting setup to soften shadows, with a single main light and two supporting secondary lights placed behind and to either side. These lights were purposefully different colours to help differentiate between different areas, providing another signpost to the player of where they are currently looking. The supporting lights are also dimmer than the main light, allowing me to write a quick script to add light flicker to the main light, giving the impression they had been plunged into darkness when the light flickers out, while still providing just enough light to navigate by. The flickers should give the impression of a run down environment, not make it impossible for the player to play the game.
<!-- assist in first year lectures - want to pursue leadership roles so useful experience, also enjoyable -->

<h4>References</h4>
Atlassian (n.d.). Git merge conflicts | Atlassian Git Tutorial. [online] Atlassian. Available at: https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts.

<p style="margin-bottom:3cm;"></p>‌

<h2>Week 3: 03/10/22 - 09/10/22</h2>
<!-- Sprint review, escalation and conclusion of team difficulties by individual leaving the group -->

This week I ran sprint retrospective, guiding the team as we did an internal demonstration of the latest build, went through what had worked well, what had caused problems, and things that could be done to improve, throughout the last sprint. This was then used to help guide the tasks for the next sprint, alongside the project backlog. This allows and encourages developers to share problems they have encountered and allows the team to collaboratively generate solutions, encouraging trust and understanding across disciplines as everyone is made aware of problems facing others, including problems they may be responsible for. This practice was primarily shaped by the theory within the book 'Agile Game Development With Scrum' by Clinton Keith (2010), as well as supporting research from various websites, including Scrum.org (Scrum.org, n.d.).

Alongside this game jam I have been working on improving my art fundamentals, and have been attending undergrad lectures as part of this. This has included study of the Andrew Loomis proportion charts for both the body (2021a) and the head (2021b). While I had seen these before I hadn't done any proper focused studies on them, and while I still need to do that I have begun applying the basics in sketching silhouettes as well as during Life Drawing. Having internalised the basic "8 heads" proportions I'm finding they are becoming more instinctual, as well as giving me incredibly useful reference to pull from. As such, these drawings have become the start of, to borrow a phrase from my programming work, my debugging checklist for when I am drawing humanoids and the drawing is feeling off. As mentioned, I have been doing silhouette studies as a method of practice, both for my understanding of proportion given that I can do a lot of figures very quickly, and because producing silhouettes is an important part of concept art so will be a useful skill to demonstrate I can do for industry. The importance of producing silhouettes comes from both its speed, something essential during the early stages of development (Howtonotsuckatgamedesign, 2014), and that it forces an artist to focus on shape language and initial read (Administrator, 2014), rather than getting lost in the detail of a design too early.

This week I also set up a dedicated art version control server for our project. This serves several purposes, providing a repository of all the raw files for art assets, making it possible for developers to look at each others files to provide feedback if requested, having a back up of all files in the case they are unable to working or access files on their local machine, as well as encouraging all artists to become familiar and more comfortable with Git. This will help to alleviate any trepidation they may otherwise feel when having to push files to the main project repository, a trait I have observed when working with artists on previous projects.

<h4>References</h4>
Loomis, A., 2021a. Figure drawing for all it's worth. Clube de Autores.

Loomis, A., 2021b. Drawing the Head & Hands. Clube de Autores.

Scrum.org. (n.d.). What is a Sprint Review? [online] Available at: https://www.scrum.org/resources/what-is-a-sprint-review.

‌Keith, C., 2010. Agile game development with Scrum. Pearson Education.

Howtonotsuckatgamedesign. (2014). Let’s Get Real About Concept Art. [online] Available at: http://howtonotsuckatgamedesign.com/2014/02/lets-get-real-concept-art/.

Administrator (2014). Shape Language & Silhouette in Art & Design. [online] ConceptStart.net. Available at: https://www.conceptstart.net/art-tutorial/improve-shape-language-silhouette-in-concept-art-design-illustration.

<p style="margin-bottom:3cm;"></p>

<h2>Week 2: 26/09/22 - 02/10/22</h2>
Following from my decisions in Week 1 regarding undergrad modules, I have arranged to meet with my academic tutor on a regular basis to check I am on track for my goals for the course. This has value due to them having more experience in the field, so they will likely have a better perspective on if my skill progression is on track, as well as having more experience of students progressing through the masters so would be able to highlight if there were areas that I was progressing slower than expected with. This then allows me to refocus my practice, or seek extra support, in these areas.

<p style="margin-bottom:3cm;"></p>

<h2>Week 1: 19/09/22 - 25/09/22</h2>
This was the first week of the Game Art Masters at Falmouth University, which was incredibly busy as I attended lectures for seven different undergrad modules, as well as the lectures for my masters module. While intense, this aided in 'evaluating' the undergrad modules, as I wanted to attend them to aid in the development of my artistic skills and knowledge, but given I have limited time per week I can't attend every undergrad lecture. I decided to attend first year Concept Art and Environment Art lectures as these aligned with my desired future role of Junior Environment Artist, preferably at Jagex, building on both my 2D and 3D skills. More generally, I am wanting to develop my skills towards being able to design, concept, and produce environments for players to explore, taking into account artistic considerations such as atmosphere, lighting, colour palette etc., and combining this with design considerations like how the area is revealed to the player and guiding them along specific paths and highlighting important areas or items. Looking at the Jagex job posting for the role (jobs.lever.co, n.d.) one thing they want as a bonus is traditional 2D art skills, which further increases the value of the first year Concept Art module for me, as well providing a reason for me to continue attending Life Drawing sessions.

This week began a three week game jam, in which I lead concepting discussions due to me being one of the more experience developers within our team, and having a good overview of the entire game development process, not just a single discipline. This is due to me having actively developed this broader view point during my previous projects when working as a Producer. This perspective aided in the team being able to design a concept with a mind for what was possible given the available scope and team composition. At the beginning of the project, there were three major concerns: the game jam was only 3 weeks, it was a development team that hadn't worked together before, and a majority of developers were new to game development. 
Given that a majority of games, even smaller indie titles, are produced over several years not weeks (Dana 2022) it was clear that we would need to design a concept that was very focused, both mechanically and environmentally. This was especially true as the team had not worked together before, so would be progressing through 4 stages of team work (Tuckman, B.W., 1965, p.384) and wouldn't be as productive as a team who we were already familiar with working together. Finally, Working with developers new to game development meant they were unaware of industry standard 3D pipelines (Intel 2018), so it was important to introduce them to these both before and during the project. This allowed all developers to be using the same optimised workflows, increasing efficiency and enabling easier communication and cooperation between developers.

These three factors fed into my primary concern during ideation, which was scope, as overscoping can cause crunch, increase developer stress, and result in features being cut close to a deadline. We explored several ideas for managing scope, such as designing a lot of modularity and reusability into our environments and mechanics, effectively increasing the <i>value</i> of each piece of work produced. We began ideation with a session of brainstorming, which served the dual purpose of acting as a team building exercise (Chandler, H.M., 2009, p. 221), allowing us to explore all ideas without committing to something that was out of scope.

<h4>References</h4>
jobs.lever.co. (n.d.). Jagex jobs. [online] Available at: https://jobs.lever.co/jagex [Accessed 6 Oct. 2022].

Dana (n.d.). How Long Does It Take To Develop a Video Game? [online] Available at: https://geekygamingstuff.com/how-long-does-it-take-to-develop-video-games/.

Tuckman, B.W., 1965, p.384. Developmental sequence in small groups. Psychological bulletin, 63(6).

Intel. (2018). Step Up Your 3D Asset Pipeline. [online] Available at: https://www.intel.com/content/www/us/en/developer/articles/technical/step-up-your-3d-asset-pipeline.html [Accessed 5 Oct. 2022].

Chandler, H.M., 2009, p. 221. The game production handbook. Jones & Bartlett Publishers.






