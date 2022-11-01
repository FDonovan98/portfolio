---
layout: post
title: Reflective Journal
description:
image:
nav-menu: true
show_tile: true
tile_order: 3
---
<h2>September, October, and The Future</h2>
initial period based around 'finding the passion', as well as planning development path.
likely going to scale down time commitment to 2D, continuing to attend first year concept art lectures but reducing time committed to practice in order to devote more time to other areas. Due to 2D being a secondary rather than primary skill I'm developing, and finding other aspects, such as zBrush & maya, more compelling.
while game project revealed several useful insights into the importation of assets into Unity, it proved to be more of a distraction than a developmentally valuable process due to already having the game development knowledge, while missing the art creation knowledge. this will drive me to focus on art-specific projects moving forward with the course, rather than game projects, allowing focused development of art without the game & group work distracting from that. While it would prove invaluable to some, it isn't what I need most for my development at the moment, and implementation experience can come from personal projects, without the overhead that comes with working in a team.
Hope to continue mentoring, providing what help I can to peers but have also reached out to senior staff at GA offering to help out with the undergrad game dev projects in a mentor role. enjoy this and is rewarding, as well as being good evidence of suitability for senior positions, as I will want to pursue this and hope that this suitability, drawn from mentorship, strong interpersonal skills, and management and planning skills from production experience, will help me to stand out when applying for junior positions as there is a shortage of seniors, so my hope is that a junior who could be trained and mentored into a senior role will be an attractive prospect. teaching is also one of best ways to cement and test what you've learnt
continue recording reflective practice, although likely decrease formality as so far this has been for an assessment, but it is a practice i carry out regardless so makes sense to have a written, demonstratable record of process and practice

<h2>Week 5: 17/10/22 - 23/10/22</h2>
I decided to downscale my ongoing side project to prioritise practising UVs and learning zBrush over making a complicated model.
Manually UVing this scaled down model is the first time I've manually unwrapped an asset, having relied on auto-unwrap until now. Initial cylinder unwrap, unfolded, straightened and added manual cuts to improve automatic seam placement. additional planar maps to grab mug bottoms and edges, checking for stretching using the checkered map in maya. imported into substance to do quick check for noticeable seams or overlapping seams. separated supporting band caps due to them causing overlapping uvs while attached. straightened and arranged uv maps, then consulted with academic for possible improvement, who advised better cut placements and advised that cylinder projection could be rotated before unwrapping to provide cleaner unwraps. 
zBrush wood sculpting, began texturing. panelled asset allows multiple batches of practice and reflection on small segments, which facillitated experimentatoin and method comparison, and led to rapid improvements, with the final panel being significalntly higher quality than the first one. partly this was due to tools, switching brushes and preview material, partly software practice and familiarity, and seeking feedback and a software 'masterclass' from assistant lecture experienced with the software.

<h2>Week 4: 10/10/22 - 16/10/22</h2>
During a consultation with other artists on our team, a bad habit I have developed was highlighted, which was always trying to make an asset out of a single mesh. While I have found modelling an asset from a single mesh reduces the likelihood of producing overlapping faces, which could cause artifacting and take up additional space when UVing, a section of a model can often be easier and quicker to model individually. This single-mesh-manipulation can also produce undesirable topology compared to modelling parts separately, potentially increasing the polycount of a model significantly. As such, I aim to actively consider whether a part of my model would be better to model separately moving forward, as while there are certainly use cases for the single-mesh method, it should not be the method I <i>always</i> use.

I have also continued mentoring two artists on our team who are new to both 3D art and game development, supporting their use of Maya and Substance, as well as continued support with version control using Git. I demonstrated importing a completed asset into Unity, covering model and texture export and importation, prefab setup, material creation and application, and finally pushing these changes to the projects Git server. The reason I have taught them this workflow, rather than dropping raw models into scene, is to allow changes to be made to models in the future without having to make any changes in a scene. The more people making changes to one scene (or more specifically, the same binary file), the more likely we are to encounter merge conflicts (Atlassian, n.d.), which it's always best to avoid as they often result in loss of work when merging binary files.

I also did an initial lighting pass for our game, utilising a three-point lighting setup to soften shadows, with a single main light and two supporting secondary lights placed behind and to either side. These lights were purposefully different colours to help differentiate between different areas, providing another signpost to the player of where they are currently looking. The supporting lights are also dimmer than the main light, allowing me to write a quick script to add light flicker to the main light, giving the impression they had been plunged into darkness when the light flickers out, while still providing just enough light to navigate by. The flickers should give the impression of a run down environment, not make it impossible for the player to play the game.
<!-- assist in first year lectures - want to pursue leadership roles so useful experience, also enjoyable -->

<h4>References</h4>
Atlassian (n.d.). Git merge conflicts | Atlassian Git Tutorial. [online] Atlassian. Available at: https://www.atlassian.com/git/tutorials/using-branches/merge-conflicts.

‌

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



<h2>Week 2: 26/09/22 - 02/10/22</h2>
Following from my decisions in Week 1 regarding undergrad modules, I have arranged to meet with my academic tutor on a regular basis to check I am on track for my goals for the course. This has value due to them having more experience in the field, so they will likely have a better perspective on if my skill progression is on track, as well as having more experience of students progressing through the masters so would be able to highlight if there were areas that I was progressing slower than expected with. This then allows me to refocus my practice, or seek extra support, in these areas.

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






