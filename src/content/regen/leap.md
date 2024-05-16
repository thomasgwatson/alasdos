---
layout: post
excerpt: "A new future"
title: "Hylo Leap"
author: Tom Watson
tags:
 - regenerative
image: ../img/peacoco.jpg
date: "2022-03-04T23:46:37.121Z"
---

Posted 2024-03-04

### Group-chat is where the party at

Group-chat is where A LOT of the world is starting their organizing efforts. Its informal, rapid-fire, there are multiple providers of group chat that have VAST infrastructures that help it work in low-bandwidth spaces. And, in own own experiences and others, organizing and coordination hits fiction and stumbling-blocks as groups outgrow group-chats. If only we could wrap those group-chats in the warm embrace of more structured coordination tools... 😉

So we get Hylo Leap. Or Boost. Or Hylo River. I'm just going to use Leap as the working title for now

Before I launch into my proposal, let me list a bunch of my other assumptions

Assumptions
- Most folks in the world will interact with online stuff via mobile
- Thus, if your mobile experience is pokey, you will struggle to connect to those people
- Our 'power-users', stewards, typically need to engage and connect with these regular users
- So even if our desktop/web experiences satisfy them, we will struggle to help them reach their goals
- We will not replicate the performance of messaging services with 50 mil+ annual budgets with our resources

### Leap Proposal
- Research Beeper/Matrix bridges (check both Beeper hosted bridges, self-hosted and Matrix service providers)
- If technically tenable, proceed with proposal 
- get the existing mobile app stable (i18n, some low effort performance tweaks, proposals/roles stuff)
- !! Stop developing existing mobile app
- Greenfield new mobile app development; likely still react native, maybe expo addition to it being RN
- ** CHALLENGE: how do we create test/development environments (fake signal group for example) that can allow for development?

At this stage, we still have the web-app and the legacy mobile app in operation. Our existing partners still have access to everything they paid for. The beta of the new app is released to the app stores and exists in parallel to the existing Mobile app.

###### New app, working name LEAP
- Groupchats from connected messaging services are visible in Leap. 
- Infrastructure for messaging is handled by the respective service.
- No individal chats from other messaging services are ported over (avoid clutter). 
- If the original service encrypts messages, this is respected. No copies of group-chat messages are stored in our backend 
- Leap users don't even need to be Hylo desktop/web users to get benefit from Leap; they benefit from the coordination provided by power-users, who are full Hylo users
- Non-leap users from the original group-chats will see get some benefit; links to public hylo content will still be avaiable to them and they will be prompted to join Leap for private content.

###### Initial Technical/data design
- Leap users sign up by: phone number? connecting a message service?
- Each group chat added to Hylo backend as a group when a Leap user adds that chat.
- These hylo groups are restricted and private but can be attached to parent groups (Not intending Hylo to be a direct/automated ingress point back into these group-chats)
- ** CHALLENGE: the best outcome is that Leap is able to read group meta data and membership. We will need to protect personal information from those membership lists in a separate way that obscures it to our servers, until such time as they join Leap or sign up to Hylo
- Group metadata persists on device: initially from messaging services and complimented by persisted Hylo group data
- This means practically no server-request-blocking async calls to load app; near instant loading of app
- All members of a chat are mapped to hylo users: 
- either as real existing users (problems with how to map, since Hylo doesn't know about phone numbers right now) or
- as proto-users (no real profile) that can be claimed later on by that phone number/unique ID/entity (personal information obscured on our servers, so likely some form of hashing used there).

#### Paid functionality:
I would want a decent free experience; there is still value to being on Leap, even as an organizer, without having to pay for it. And, there are paid features that really simplify coordination (and/or offer deeper coordination)

Ideas for paid features:
- connect your Leap group-chats to the topic-based chat from a parent group (this chat would still be available in the desktop/web hylo interface regardless)
- Push/forward/publish your Hylo content to the message-service group-chat (connect to your non-Leap members)
- A single interface to push an announcement/event to multiple group-chats, across services (I see folks cutting and pasting or forwarding messages across communities they run on whatsapp on the regular)
- A single interface to create a child-group that invites people by email or phone number to a group-chat-hylo-group combo (might be weird if they don't already have whatever service already hosts the group-chat)

Those last two are particularly helpful to organizers of all sorts.

Again, free to be in hylo groups. Free to be in group chats on Leap. Free to start organizing small stuff on Leap (with that basic confluence of hylo and messaging data streams) But only group-chats that are sponsored by a hylo parent group get the fun interconnection tooling (better to handle payments outside of the mobile environment, lest Apple come after us for a 30% cut).

#### Multiple layers in the one timeline
So, a groupchat is a timeline. And its a timeline with one layer of data, from the message service. This message stream is something we explicitly do not control, nor do we directly 'see it' as a service provider. The Leap app can be the confluence between that data stream and various Hylo (and ultimately Holo, maybe other) data streams. Here different hylo data streams could be layers defined by
- slicing up post types as a set (eg: show me events but not other types)
- announcements
- mentions
- parent group content (layers of the above)
- digests

Initially this would be minimal, and the group and users could evolve into using them over time. How do we manage getting users their preferred signal to noise ratio?

###### Squelch, not silence
Squelching is when a device receives a signal that isn't strong enough, and it is suppressed. Squelching is the vibe I am going for with talking about helping our users with signal-to-noise ratio. How can we keep sending info to our users and know what to squelch? For example, Whatsapp and Signal send little notices about people joining, leaving the group, admins changing description, etc. But these don't cause push-notifications, nor other 'unread' UI to be updated. And they are presented in a background way from a UI perspective.

I want to apply that concept to Leap for Hylo layers; Hylo content isn't sent whole, unbidden, to user devices. But 'activity notices' (naming is tricky here) are still pushed. These contain hylo content metadata; enough data to act as a pointer and reference of the content, and little more. All Leap users get these updates but they are largely background data. One big difference with the pointer notices is that they GO somewhere (unlike 'someone joined the group' which is the whole message).

The baseline is that these tiny activity notices are pushed to all Leap users for that group. If a Leap user has preset to receive events from a specific group-chat, these activity notices can be displayed as a stub in the stream, as a cue for where to trigger a further download of content (could even be used to pre-load). The stream can also have a subdued indication of hylo activity in it, giving the user a sense that wider activity is taking place, and a UI component to anchor their curiosity if they choose to dig deeper. 

Of course, when a power-user pushes hylo-content to the group-chat (an announcement, an event invite...), that will be presented to Leap and non-Leap users of that chat, and offer another onboarding opportunity for these users. Leap users will be able to see that content in Leap, non-Leap users of the group-chat will need to log-in if the content isn't public.. or request a one-time magic-link login for that specific content

#### Evolution
Of course, more features can be revealed as the group-size/experience of stewards grows

- As a group becomes larger and/or requiring of a deeper layer of coordination, power-users can have access to fuller-UIs for creation/editing in the webapp/desktop, that still have a compact representation in Leap.
- We double-down on events; scheduling them, invites, reminders, live-votes, working-groups, maybe even schedule-outline views
- Integration with ticketing providers
- That will probably need to extend to online as well: straight-forward linking to zoom calls, etc
- For bigger groups, AI assistants for stewardship activities. This is probably extendable to the paid features as well, with additional assistant functionality like scheduling messages available
- At a certain level of group-evolution, the ability to post to public is enabled
- Maybe instead of it being paid, topic-based chat is enabled in a later evolution for a group
- Regular users still get lots of value just out of being on Leap; Power-users/stewards get richer tooling by using the desktop/web app

Another step-up in the group evolution unlocks budgeting and more complex governance options

### Whats missing and what happens to the rest of the Hylo ecosystem
The one direct content stream Leap might have is local/bioregional activity, for public local stuff. Maybe at some point Leap includes the bioregional discovery story/journey.

The legacy hylo mobile app can just be, without significant updates. Maybe after a little while, when LEAP is more mature, we decommission the legacy mobile app. At some point the desktop app is released. The webapp redesign reflects whatever we decide are sensible evolutions. The desktop/webapp become the home for power-users/stewards. The backend won't need to be replaced but a separate Matrix messaging backend will need to be setup to support cross-platform messaging and our own dm/group-chat structure (which can just be a plain matrix messaging service).

### The outcome
- We offer a way to meet users where they are at (whatsapp etc), minimizing onboarding fiction
- There are clearer value-add features that power-users and stewards will want to pay for
- We are still offering so much capability and functionality to free-users
- The really hairy connectivity, low-bandwidth situations are largely handled by other services that we bonus off
- We have a mobile app with a better foundation of data-handling, built for off-line and no-connectivity moments from the ground-up
- We do away with the concept of 'feature parity' between desktop/web and mobile
