---
layout: post
excerpt: "Also a business/product strategy"
title: "A love letter to invitations"
author: Tom Watson
tags:
 - regenerative
 - hylo
image: ../img/high.JPG
date: "2024-06-24T23:46:37.121Z"
---

This love letter is also a business strategy ;)

> I propose that we make invitations the beating heart of Hylo. 

To invite is the core verb of consent-based connection. A good invitation is clear in who is asking, to whom they are asking, why they are asking, what they are asking, and allows for meaningful gradients of response. A good invitation takes care of the invitee's attention; does this little morsel of information give me enough to decide to learn more or to decline? This invitational energy is now brimming through our landing page; lets extend it to the whole experience!

Making invitations a primary concept like posts and groups will lead to:
- A more reliable way for stewards and super-users to connect with their movements, peers and communities
- A more gentle membrane for folks (invitees) to start engaging with the platform
- More events organized via Hylo
- A platform that covers much more of the foundational tooling for bioregional organizing
- Additional invitation mediums that include Holo, whatsapp groups, signal, etc, that would be worth paying for on top of a free platform.
- A movement/contact management system that would be worth paying a premium for
- A bite-sized white-label experience as part of that MMS
- The centering of the 'invitational vibe'; the energy of being asked to engage with something fun/worthwhile, while having control over how deep one wants to go.

---

## An invitational frame of mind

Of course, we have invites right now. We have group invites. And we have invites to create an account. And in some ways, you could say that an announcement is a invitation for a whole group to engage. Or a mention in a comment is an invitation to engage. Many platform actions have an invitational aspect to them. And, as inviters, we don't know enough about how those scattered invites are landing. And as invitee's its not always clear we are being invited, or how to signal interest/disinterest or "remind me later"

We end up with questions like:
- Did the invitee even open the invitation?
- Did they baulk at signing up to a platform?
- Did they see the content but didn't engage in anyway?
- Did they mean to engage but were busy when the invitation arrived (Can they say, remind me later)?
- Do they want to be kept updated on the content as others engage with it?
- Do they actually never want to receive an invitation from that individual again?
- Does accepting the invitation take too many steps before they get to the content?

![break](../img/icon.jpg)

By centering invitations, we can make it
- Easier to answer those questions (at a much deeper level than Mixpanel tweaks)
- Smoother for invitee's to engage with content and otherwise control their experience

How do we make it easier:
- Uniting all the different ways you can 'invite' someone to engage into a coherent data model (do we have an invites table that centralizes it all? do we track it all in the activities table, since that kinda does track some of it already?)
- Allowing invites to all* the different forms of content
- Allowing those invites to go out to non-users; via inviter provided emails or phone numbers (and other mediums in the future)
- Allowing invitees to use that medium (an email or a phone number) to login into an isolated view of that content
- By isolating them to just that content, we can offer a different membrane for interaction. It's fast; loads a dedicated server-side rendered view that has a tiny bundle and laser focused functionality. Its walled off from other content/groups (with an escape hatch to the platform and full signup); bad behavior can only happen on that piece of content. Because its an isolated view, its much easier to offer a white-labelling experience.

\* Ok, maybe not every single type of content... but maybe?

---

### What specific features would anchor this?
- Isolated views
- Invitation station; a centralized UI for managing your invitations (+ inviter work-flows)
  - A finer-grained tracking of invitation acceptance and 'engagement'
  - When creating content, having a UI to pop out the extra 'invitation' layer for more specific distribution
- "Magic-link" based logins
- Text-code logins (enter these six numbers...)
- Post-invite 'Subscribe' to content via text/mobile (eg: you say maybe to an event invite)
- Invitee workflows 
  - Quick and simple ways to show interest or disengage ("text 'm' to this message to mute this event"; "RSVP: yes/no/maybe"; "Show me this later" etc)
- 'save for later'/TODO UX
- Allow a user to be associated to content without being part of one of the groups the content is posted to

###### Features needed in addition for paid add-ons
- A bridge to holo
- A bridge to matrix compatible services (whatsapp, signal etc)
- A white-labeling interface
- A invitation flyer UI; customize your online flyers and make it coherent across several mediums
- Contact management system that extends the invitation station to allow for tracking engagement of a movement of people outside of the group-scope

---

### Behaviors or patterns this would beget
- More events organized on Hylo
- Significant increase in casual users
- Deep value created for super-users
- Easeful engagement of folks outside of the Hylo platform

### Impact on our values
- Stewardship
  - This would mainly make existing stewards more effective. In time, I would want to add other features to help increase the growth of regular users into stewardship
- Adaptation
  - I think this better positions us in an attention-contested world.
  - It also boardens our reach; "meeting people where they are at", with app/account-fatigue
- Co-Creation
  - This is generally inherent in the way we build things. Of course, I would love to bring this concept to the wider community and it would ultimately depend on their use and engagement
- Wellbeing
  - Less direct impact on wellbeing, beyond more events => more connection => greater wellbeing
- Liberation
  - Set our users free! Reducing the burden on casual users for downloading an app or signing up to another service is actually really healthy
- Agency
  - This helps both super-users better understand how their invites are landing and also allows invitees to better signal their interest or otherwise in the actual content, instead of being befuddled by platform friction.

### Business outcomes
- Good foundation for several possible revenue streams from super-users (not necessarily targetting regular/casual users for revenue). These would need marketing.
  - White-labelled outreach for muncipalities, NGOs, county/state governments to connect with their constituents around governance (the isolated views would be white-labeled and mainly what is seen but users can ultimately see content in hylo clients)
  - Holo-users can push content into the Holo ecosystem
  - Event organizers can have a single platform for connecting with invitees, volunteers, staff, and the different mediums they are spread across (pushing their invites via signal/whatsapp/telegram)
- Makes CSAAS even more compelling
- A greater degree of differentation in functionality from peer platforms (Mighty Networks, Facebook, etc etc)

#### Roll-out concept
This could be wrapped up into a specific pitch deck to get targetted funding. For the paid-features, I would roll them out to existing paid partners as a testing ground while we work on them, with the understanding that their prior funding is basically credit against any paid-features they wish to continue using. Once a good baseline of functionality is established we can then bring on marketing and outreach, with the goal of starting to generate revenue in late Spring/Summer 2025.

![break](../img/icon.jpg)

## What comes next?
There are imnumerable details to go into from here, many that I have already had the chance to consider and many I have not. I like centering on invitations because it brings more coherence to all the different use-cases for groups, both ones on the platform and ones that we are courting. Getting invitations right gives us appeal to wider regen-adjacent partners. Their revenue can float the platform, and we can gently invite them into a deeper appreciation for stewardship, bioregional thinking and models of shared governance. I also really like that it better serves those outside the membrane of Hylo membership, those who loathe to download another app and those who are at the fringes of connectivity.