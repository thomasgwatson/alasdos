---
layout: post
excerpt: "Mapping Bioregions"
title: "The challenges of mapping bioregions (Part 3)"
author: Tom Watson
tags: ["bioregionalism", "mapping", "Terran", "Hylo"]
image: ../img/high-desert.jpg
date: "2022-11-12T23:46:37.121Z"
draft: false
---

_This is the third post in a three part series on bioregions. If you aren't familiar with bioregions, best to start at [part one](https://twicefire.com/bioregional/bioregion-1/)_

We want to start mapping out bioregions. We have realised there are lots of fiddly questions and nuance that come from that. We are going to try sort through all that anyway. This is a bit more of a nitty-gritty, and possibly wonky read, so please set your expectations accordingly (and if you are trying to share with someone about bioregionalism, I wouldn't start with this post!).

![break](../img/icon.jpg)
### What process can we use to determine bioregions in the mapping context?

What are the key things we need to consider in a process for mapping something? In all cases, we tend to consider questions including:

- How ought it be represented via geometry?
- What data can we map to the base geometry and can we get it?

And following on from those questions:

- How ought it be shared?
- Do we have the skill-sets, resources, access and time to achieve the scheme that is the outcome of answering these questions?
- What sort of process do we use to take all of the above geometries, data and inputs to actually generate bioregions?
- How might these choices help or hinder other processes layered on top of this system (voting systems)

For bioregions, as understood by bioregionalists, we also consider the human cultural aspect

- How do we create bioregions that resonate with folks that live in that region?

![break](../img/icon.jpg)

These questions or considerations also form an interlocking bundle; its very hard to consider them one at a time, figure out that piece out in isolation, and then move on to the next question. If we attempt to solve for only one question at a time, it can defacto lock us into only a narrow range of options for other considerations.

And finally, a mapping scheme is just an exercise in imagination unless it is adopted by folks. Figuring out who are the various adoptees, users and champions of a mapping scheme, and when to involve them, is very much the meta-art of building a mapping scheme. This post is very much a result of trying to address that process, and if you've read this far, odds are you are one of those potential stakeholders!

This post is going to be a living journal of all of my research and thinking about all these different considerations. As of 30 May 2022 (and prior), I have had an idea for an uncommon scheme to achieve the goal of mapping bioregions, but I want to lay out the alternative concepts and justify the trade-offs inherent in any of the design choices one must make in these matters. Wish me (and us) luck!

### How ought it be represented via geometry?

["The map is not the territory"](https://en.wikipedia.org/wiki/Map%E2%80%93territory_relation) is a relatively well-known philosophical phrase that denotes that the representations and models we make about reality are not reality themselves, despite their benefit in allowing us to share understandings of reality. The geometry is the literal representation of territory; the sort of geometry we use to represent something will shape how we think about that something. And, may I remind us always, the representation is always a reduction of what it represents; and thus, it is 'always wrong' in some sense. [All representations (models) are wrong, some are useful.](https://en.wikipedia.org/wiki/All_models_are_wrong)

With that prelude, how do different options shape up?

###### Unique polygons
Unique in the sense that each bioregion has its own custom geometry, not dependent on a known set of geometries (like parcels or county boundaries). This, for one bioregion, is very straight-forward and familiar. When we are creating a series of bioregions though, the flexibility of unique polygons adds complexity fast. We have to enforce topologically sensible boundaries; random little gaps or overlaps between bioregions can lead to confusion in some instances. A second consideration is that creating custom polygons for a large number of bioregions can be a lot of work, and we cannot easily crowd-source that because of the topological concerns. Mapping data from other sources into these custom polygons is also a little more onerous than other options. 

###### 'Known' polygons
Existing polygon systems include: counties, shires, parcels, watershed systems, zipcodes, WWFs ecozones and many more. These aren't generally appropriate for a direct mapping of one bioregion to one of these geometries but if the geometries are small enough, they could be used as constituent pieces of a bioregion (for example, these five counties together make up a bioregion). One advantage is that data and information that we want to use to make sense of a bioregion may already be encoded into these polygon systems. However, almost all of these know polygon systems will be constrained by country and state/province boundaries, which gets in the way of the ecological aspect of mapping a bioregion. And some of these systems (zipcodes, parcel data, etc) will be clear and comprehensive for one part of the world but not whole continents. 

###### Grid systems
Grid systems in mapping tend to grapple with the challenge of applying a globally coherent set of pre-defined shapes to the earth, as a way to streamline the organization of data. They make all sorts of data comparisons and sorting easier, once the data has been mapped to the grid system. The two global grid systems I am familiar are S2 and H3. [S2](https://s2geometry.io/) was made by google and divides the world up into a hierarchical scheme of four-sided polygons that interlock over the whole world. Its great as a spatial index, meaning a way to quickly 'address' datasets that have geometries. It is not very appealing as a representation geometry; the four sided shapes distort in appearance, dependent on their location on the globe.

H3 came out of Uber, helping them track supply and demand for rides. In addition to the advantages of S2, it also provides a better representation geometry with its hexagon grid, along with more consistent relational dynamics between the grid elements. That consistency in relational dynamics makes it simpler to derive impact across the hexagons in a local area. Say if we wanted to apportion voting power by distance from an intervention, that would be very simple to calculate with this grid.

###### Point data
This option is more of a thought-experiment than a practical choice. If we represented a bioregion as a point at its notional center, we would do away with the issue of defining boundaries... because there would be no boundaries to define! Figuring out where that center is, membership and identity for these would be a constant nightmare, as would trying to represent data in this scheme. I would prefer to pass on this option.

![break](img/bird.jpg)

### What data can we map to the base geometry and can we get it?
It would be incredible to inform our decisions about defining bioregions by having access to keystone species, habitat boundaries, watersheds, human patterns of movement and land-use, local inhabitants perspectives, ecological and climatic factors, etc etc... And each of these possible data sources would need to be 1) Found or created (!) 2) Ported to whatever geometry we settle on 3) analysed and integrated into whatever process is used to delineate bioregions 4) Updated as things inevitably change over time. On top of all that, the different datasets would ideally be global, or at least harmonised across global datasets.

Alas, going for both breadth and depth on all of these feels like a mind-boggling amount of work. With an infinite budget, it would probably still take a lot of human talent and time to get everything our hearts could desire. Consequently, some level of prioritisation of data-sets and a periodic, iterative process of determining bioregions will serve us best, as we add more data and community input over time. For now, I will detail initial views and guesses on what data sets we could use and how easy (or hard) it will be to integrate it into a process.

###### Human population density & Human landscape management density
Population density is fairly easy to get as a data source, and while I would not factor it in bioregion boundaries, it is useful as a quick indicator of our impact in an ecology. It ought to be paired with datasets related to human landscape management; the distribution of our built environment ('towns and pastures' versus 'suburbs and motorways' could have the same human density but very different ecological impacts), distribution of agriculture, infrastructure and 'managed' landscapes. Getting all the different datasets that could inform human landscape management will vary in ease (especially across the globe) but are really handy for giving folks a read on what bioregional interventions might be transferable between different regions. These datasets will also be handy for tracking bioregional health over time, as we create different distributions of human impact on ecologies.

###### Watersheds
Watersheds should be fairly easy to source data-sets for, perhaps a little annoying to make consistent across the globe, and are key for determining impact in some categories of bioregional intervention (removal of a dam, waste water treatment, etc). Watersheds will have an impact on bioregional boundaries but it is a bit fuzzy to determine the cut-off vs continuation point for them. For example, the whole Mississippi basin crosses vast terrains and contains a diverse range of ecologies and peoples; It would be an unwieldly bioregion to coordinate for all matters. Better to have smaller bioregions that are more nimble, but that have an inter-bioregional coordination mechanism for watershed scale interventions.

###### Ease of movement
'Ease of movement', stemming from a military term I'm familiar with, 'lines of communication', is important for bioregions because the easier it is for humans, materials and flora and fauna to move through different areas, the more likely those areas make sense as being connected into a bioregion. Generating this dataset might be a little cumbersome, built up from how easy terrain is to traverse (open plains vs thick jungle), infrastructure like roads and railways (etc), and even human defined borders (this is where I'd prefer borders to influence bioregions for now). This could be extended to be split into human and fauna categories; a system of highways might make it easier for humans to get around but cut off access to different regions for animals. Not the highest priority dataset to compile but one that I think does significantly impact how ecosystems function.

###### Climatic factors (marine influence, latitude, elevation, weather patterns)
Climatic factors deeply shape ecologies. The flora and fauna of a bioregion are ultimately all consequences of the climatic conditions of a place. Datasets that represent climatic conditions are typically very available, the tricky aspect will stem from how they are combined to understand bioregional boundaries. The Köppen climate classification system could represent an easy initial drop-in analysis to cover that 'tricky' integration question, as it provides a concise characterisation of the climatic conditions apparent in different places.

###### Flora and fauna habitation patterns
The flora and fauna of a region can be the most obvious identifying features of an area. From a long term local perspective of an area, there are usually one or two dozen trees, animals, plants, etc that define a region. From the outside perspective, it might be tricky to determine what are the key flora and flora, and also how that influences the boundaries of a bioregion. *Coppice Agroforesty* notes that the Society of American Foresters identified 145 different 'natural communities' of forest stands, using names of one to three dominant species like "Hemlock-Sitka Spruce" or "Oak-Hickory". That might be a good dataset for this purpose but would need to be complimented by similar datasets for other regions of the world.

###### Minimum viable data set?
What is the least amount of work and data we can get away with while still providing a decent basis for the creation of bioregions? This is my current working set, as of November 2022.
- Human population density
- Koppen climate classification
- Built environment (proxy for human landscape management)
- Agricultural lands (proxy for human landscape management)
- Watersheds (depending on how easily their representation can be harmonised across continents)

To continue hammering home the point, these would of course need to be integrated into some process to actually generate bioregions.

![break](img/rolling-in.jpg)
### How ought it be shared?
Whatever mapping scheme we come up with, it has to be shared in order to serve any purpose. Ideally it would be open and free for non-commercial uses, and user and developer-friendly, to aid in adoption. As of November 2022, I am just going to note what else needs to be considered around getting a mapping scheme into use.

- Versioning/Publishing
- Editing/Updating (particularly as new data or new community inputs become available)
- Distribution; Making it available

I have a lot of uncollected thoughts about these topics but I think any deeper delving into them can wait for another time.

![break](../img/icon.jpg)
### What process do we use?
What sort of process do we use to take all of the above geometries, data and inputs to actually generate bioregions?

- How much of the process can be automated?
- How can we factor in community input?
- Is there a role for 'expert' stewardship/input?
- How do we handle different communities/stakeholders having different ideas about bioregion boundaries?
 
Similarly to the "How ought it be shared" question, there are many many tangents and factors that could be delved into for this question set as well.

 ![break](../img/icon.jpg)
### What other systems and/or uses might be layered on top of a bioregional mapping scheme?
How might these choices help or hinder other processes layered on top of this system? In a future where bioregionalism grows, do we want the mapping of those bioregions to remain just a geographic 'vibe' for a region, or do we want the mapping scheme to help underpin our coordination at a deeper level? If we take the 'vibe' route, a bioregional boundary will be useful as a banner to rally folks together and little more. If we invest more effort and thought into answering the prickly questions about how to define a bioregional mapping system, then we can build a foundation of a deeper coordination system. A deeper mapping scheme can underpin how we identify who is impacted by a possible decision or intervention and a possible estimation for how much someone is impacted. In essence, a deeper mapping scheme is needed if we want bioregional governance to scale. 

Think of the complexity and contention around the geography of the USA political system; allocation of senators via state-boundaries. Gerrymandering of districts to consolidate one party's political power. The rural/urban schism papered over by 'blue' or 'red' states. The geographies of all of the states, counties and districts in the USA electoral system are the water in which USA politics swims in. If there are any aspirations to one day surpass this fractious system, we will need a 'better' mapping scheme for our coordination to swim in.

### Do we have the skill-sets, resources, access and time to achieve the scheme that is the outcome of answering these questions?
Phew, this is a tough one. Do we even have enough bandwidth to define the problem space, let alone any solutions!? (I've been pecking away at the problem space, here and there for most of 2022 now). We would need to go through a prolonged 'gathering-support -> building -> validation -> gathering support' cycle to drive this, and over time we would need to keep coming back to this question.

![break](img/pools.jpg)
### How do we create bioregions that resonate with folks that live in that region?
To start, we peel this question in two; those that get what a bioregion is and those that don't. And a particularly salient parallel question in reflection is: Does building a mapping scheme mean 1) generating a set of bioregions to proffer to people, or 2) generating a framework or structure on to which folks can bring their concepts of bioregions into a shared system?

###### If you already know what a bioregion is
In this case, you probably already have solid ideas of what your bioregion is, and maybe ideas about some neighbouring bioregions. The challenge faced here is how do we harmonise your ideas of your bioregion with someone that lives down the street? Yes, of course, talk about it with them, but what do we do when we have different ideas of the scale, extent and defining characteristics of a bioregion? Here, a proffered set of bioregions will tend to feel constrictive to existing bioregionalists. Having a framework, with some process, by which existing bioregionalists can iron out the above differences in scale, extent, etc, for their bioregion.

###### If you don't have a clue about bioreigonalism
Well, in this case, proffering a set of bioregions, with some explanation about their formulative logic, would likely spur adoption and interest in bioregionalism. It would allow someone new to the concept of bioregionalism to grasp a tangible local example and wrestle with it straight from the start. Essentially, it would avoid the dead-end to the understandable question of "Well, bioregionalism sounds interesting, what's my bioregion then?" (The dead-end here is asking someone to figure it out for themselves).

There is a tension worth emphasising here, between the supposed needs of the in-group and the out-group. Build only for the in-group; create something that helps with coordination but not necessarily growth of the movement. Build only for the out-group, and struggle to rally the existing bioregionalists to adopt the mapping scheme. Clearly any scheme which hopes for success will build for both, and will need to have the right mix of features/trade-offs to bring both groups into the fold.

###### Resonance, bioregions and 'Home'
The other important aspect of making bioregions that resonate with folks is whether a pitched bioregion can feel like 'Home' to those who live there. Or maybe more broadly, does it create a sense of belonging? Nation-states are 'imagined communities'; they are a shared narrative about a collection of places and peoples. When they don't resonate, when they are too contrived, when they fail to live up to their myths and promises, these stories tear at the fabric of society, instead of generating cohesion. Bioregionalism is in part a call to reevaluate and reemphasise our relationship to the lands, creatures, living environment, traditions, peoples, and sacred places that we live amongst and in. That reevaluation and reemphasising will be constrained if folks cannot generate a sense of belonging to place.

### What next?
No doubt, there is more nuance, more detail, in all of the above. And after this sort of survey of the challenge space, there ought to come synthesis and distillation. I need to make a pitch. I need to flesh this out with a story of what might be, and how we might get there.
 

