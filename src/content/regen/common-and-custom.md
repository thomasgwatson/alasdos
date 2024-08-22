---
layout: post
excerpt: ""
title: "Common and Custom"
author: Tom Watson
tags:
 - regenerative
 - hylo
image: ../img/brontebeach.jpg
date: "2024-08-24T23:46:37.121Z"
---

We started using common and custom with the roles feature. 

> *Common*: well-known patterns, good defaults, 'intuitive' or recommended ways of orienting to the platform. Folks need guidance, and coherence across the platform.

and

> *Custom*: many needs are not met by the common patterns. How can we make the user experience more composable? More targeted? Get precisely the notifications/content that I want?

### Can we extend this dual-idea of common-custom to more of the app?

We are leaning that way with creating content already; We are looking at making the most common 'post', be as simple as posting a chat to a chat stream. And then, *custom*, making deeper levels of content creation pop out to a bigger, more involved creation UI.

###### Groups

We are ideating around doing the same for groups; quick/easy ways to pop-off connected sub-groups from another group. Default *common* evolutions for new groups. And custom composition of the group navigation and all the extra ways to view the group. Maybe it even makes sense to organize the group settings into common and custom, splitting the more core settings from the more advanced ones?

###### Navigation

We have talked at length about re-organizing the group navigation and overall navigation. And how to organize notifications, prioritizing some groups over another, do we include sub-groups in both overall nav *and* group-nav? how to 'follow' someone? Where do we put or even include 'My Home', the public map, public groups explorer, all my groups, my activity, 'catch-up', direct-messages and more

###### Views

Well, each of these things is a view. And we can make views composable. When I see a group in the overall nav, its just a 'view'; a view of the platform based on that group and its activity (this view also tends to require my membership of that group: membership still matters!). What if instead of just letting me customize the order of those groups, the interface lets me pick those group 'views' from a template *common* view, but it also allows me to compose those views in other ways. 

###### User stories

Say, I just want one button for all my internal Hylo circles; I get to create a view, include the four groups that I want to, assign it a nickname ("work stuff"), give it an avatar or just use an avatar from one of the groups, and then position it in the overall nav. I can click on that view, and just get content that matches what I have specified. I can even adjust notifications settings specific to this view. Because its my work stuff, I want to receive push notifications for all new content in this view.

Or, say I wanted to follow a set of bioregionalist folks on the platform. I could add them to my "following" view. Now I can see any of their public posts, or posts from groups we share, without the noise of everything else going on in those groups. For this view, I set it to just give me a daily digest on their new content, so I can keep an eye on them.

Most folks will get value out of the common views. Some folk will get value out of their own custom views. What I think is a powerful possibility that comes from this is that super users can create good views and share them with their friends or their groups. So everyone can more deeply curate their different interests. This is like an extension of twitter lists/bluesky follow-bundles.

###### Other benefits

Another great possibility that could come out of this is an opportunity to streamline. We could have one workflow (view creation) that allows a user to customize their own overall navigation AND allows group stewards to customize the views of their group content. It could allow us to also remove the saved search and the existing group custom-view UI and roll it into this. Having a common way to compose views means we can have more consistency across these different ways of letting users see what they want to see more of.

What about platform suggestions, curation by us or fancy new content algorhithms? Those can all be presented as new 'common' views for users to adopt or ignore.

What if I want to add sub-headings to my personal nav menu, like putting several groups or views in a "chat channel" grouping? Yes, I think it would be useful to do this. In that same vein, groups ought to be able to set their 'default' view, that is the first thing that their members seen when going to their base url.     

Leaning into the common-custom dual-pattern allows us some subtle design affordances. More of the app will have something like a little plus sign icon, that denotes that a piece of the UI is configurable. We could also add a cute little color theme and/or animations to the 'custom' parts of those apps (for example, to a border or around the plus button), to signify where users can go deeper into the fancy *custom* aspects of a different piece of the platform.

###### How does this impact mobile
I think the views nav and the group navs should port over just fine. Having a full view creation UI on mobile might be a stretch. And if we went this path, we might even want to consider allowing a separate nav positioning/ordering for browser and mobile, to allow for a tighter selection on mobile.

###### Possible data model

Views have:
title
notifications (might be an array of enums denoting what notifications are desired)
icon/symbol/avatar? (maybe the data model has all of these as separate and whichever one of the three is populated dictates what is displayed)
order/positioning
container (how does the views' data get represented, on the map? in a stream?)
query {
  groups
  users
  query params
}
pointer? (for direct link/basic navigation views)


What can it point to?
container (map, list, stream, etc)

Relations:
Clearly, groups will have views, users will have views and there will database defined commonViews

> Avoiding hard queries and denial-of-service

Queries will generally be pagable; you get 20 results and have to scroll to get more. That is digestable.

Paging in the same way is a little weird for map based queries; often its nice to limit those geospatially... So, this might be a fiddly bit to figure out (unless we built a full 'tile' index for each query on the fly but that is probably a "we have 50 staff and a huge budget" level of optimization)

#### Summary
I now see many requests that have come in and things that feel like they are missing in the app, as people wanting different views of the platform. Curious to hear how this bubbles and brews in everyone's head and whether the spirit of Hylo resonates with this idea.
