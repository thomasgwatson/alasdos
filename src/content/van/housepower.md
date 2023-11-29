---
layout: post
excerpt: "Writing out my house power/battery situation and my different options. Pile in with opinions as you like"
title: "Van House Power trouble-shooting"
author: Tom Watson
tags: ["vanlife"]
image: ../img/oregoncoast.jpg
date: "2020-09-10T15:11:55.000Z"
draft: false
---

Writing out my house power/battery situation and my different options. Pile in with opinions as you like

#### Brief context:
2001 Ford E350 Econoline. 
- Probably converted to SMB in 2002/2003 (1st owner)
- Original setup detailed in the owners manual: engine battery + engine alternator + engine inverter, house battery (thermoil 1427), house inverter with Trace Engineering RC6 panel, house generator slung under van. Fridge, water pump, microwave, Starcool house AC (not that we use it), house lights, 12v outlets, US plug outlets etc on house power/battery.
- 1st owner added solar panel, connected to Kyocera Commander IV unit, I assume after initial build (no details in owners manual)
- 2nd owner switched in LED lights across house to limit power draw.
- 2nd owner has also replaced battery at least once. Not sure what brand but assuming typical 200 amp hour RV battery (Deka or ... LifeLong?? Whats the other common one?). The house battery is slung under the barn doors. Its a unit; best removed with a jack.
- Me, 3rd owner, still figuring out what each of these system components does and represents
- Engine battery voltage has always been strong, from the dash readout. Maybe up to 14v or 15v? It reliably charges the house battery, acknowledging that this charging can be slower if things like the van AC are running.

So, when received in March 2020, the battery seemed solid and the solar panel was pushing about 2 solar amps into the system on a good day (best I ever saw was 2.5 solar amps; its a fairly old panel and its small).

![breitenbush campground](/img/breitenbush.jpg)
##### <sup>The Graceful Tripper</sup>

#### Issues
However, now I suspect at possibly three issues at play:
- fault between panel and Kyocera; Now the Kyocera shows 0 solar amps at all times
- battery misbehaving; doesn't seem to hold much charge
- House inverter misbehaving; I can get charge into the battery when the engine is running but not when the generator is running

On our first small trips, we weren't consciously managing power or thinking too hard about how much driving we were doing. Between the solar panel, driving, and messing around with the generator, we weren't really paying attention to battery levels. I have memories of the Kyocera and the RC6 reading the battery voltage as high as 13 or 13.5ish *but* I can't recall whether we were running the engine or generator at the time (which would then we telling us about the voltage output of the engine/gen-set, not the battery)
We have just returned from a longer trip (4 weeks roughly), and this is where these issues started to bubble up.

For one thing, we went backpacking for four days and three nights in the middle Sierras (at the very start of the trip). I wanted to test whether the battery would last that long, keeping the fridge on. The idea of a reheated curry at the trailhead was certainly enticing! Unfortunately, it didn't last and we lost the curry. :(
But after that, I started to notice some of these issues with the house battery. I was working under the assumption that the inverter would protect the house battery from load when it got too low (as described in the owner manual) but perhaps that was incorrect.

![backpacking](/img/backpacking.jpg)
##### <sup>Rae Lakes Loop</sup>

###### Discovering that something was up

After the backpacking, we drove 6 hours home and after a few days at home (getting our motorcycle carrier setup), we also drove another 4 hours.

In the second week of the trip, we parked the van near Mt Shasta for several days and I noticed:
- The generator would not charge the house battery, only the engine (I had assumed the generator did charge the battery). The generator would still power the house appliances though (microwave being the very obvious example)
- In fact, the RC6 unit lights for bulk or float charge never come on.
- The solar panel was no longer showing any solar amps coming out of it what so ever.
- After a day, the battery couldn't keep the fridge on overnight (despite running the engine and generator for over an hour to recharge it)

![Trace Engineering RC6 panel](/img/tracerc6.jpg)
##### <sup>Trace RC6 unit while the engine is running</sup>

###### The journey continued

We got smoked out of Shasta and headed for the Oregon coast (This was mainly a PNW trip). As we bumped up towards North Washington, we had several days with different hours of driving, and I started taking notes about what voltage was coming out of the battery

After a longer day of driving (the 23rd), the battery voltage seemed to top out at 12 volts. The next morning (24th), the fridge had dropped it to 9.3. We drove less than 2 hours on the 24th, and the next morning (25th), we only had 7.9 volts and the fridge wasn't running. On the 26th we drove over four hours, getting the battery to 12 volts at the end of the day and it fell to 7.3 by the next morning (on this morning the RC6 was also flashing strangely... I assume an error code that isn't listed in the owners manual)

After this, we arrived at a relative's house in Washington, cleared out the fridge and turned it off for a week, with a bunch of driving.

In the last week back, we drove more per day, so avoided the fridge conking out. At this point, we were dodging the wildfires in Oregon that were coming up everywhere, and making tracks home to Northern California. The voltage at the end of all that driving (including over 9 hours on the last day) got up to 12.2 volts.

![Side view of van at our fav boondock of the trip](/img/sidecoast.jpg)
##### <sup>Side view of van at our fav boondock of the trip</sup>

#### Questions
1. What is a healthy voltage range coming out of house battery? I was expecting over 13 volts for a full charge. The RC6 manual states: "A completely dead battery will read about 11.6 volts or less in an at-rest position". So I suspect something is funky there for sure...
1. Should I expect the generator to charge the house battery?
1. Should one expect a correctly functioning inverter from discharging a house battery to a level that damages it? Again, the RC6 manual states that it ought to do this. But if the inverter is partially busted, perhaps some of its features aren't working.
1. Could there be a blown fuse between solar panel and Kyocera commander? Or just a bad wire?

#### Possible actions to take
So, there is a mix of a few different issues here and I need to figure out how to resolve them.
Some options:
1. Maintain the battery (check fluid level etc)
1. Replace the battery
1. Switch battery to DIY lithium battery
1. Replace inverter?
1. Upgrade solar panel (I want a bigger panel)

###### Maintain or Replace battery
No change to the power setup here; just fixing or replacing stuff. Either way, I would need to figure out how to access the battery. Considering its bulk and position, I would need a hand (or a flat jack) and also I haven't figured out how to remove the battery from its carry cage under the van. Any links to youtube videos of someone doing that?

###### Switch to lithium
A friend in Washington has set up their own bespoke lithium setup for their overlanding rig. Getting 2nd hand cells, testing them all, throwing them into a purpose built case and away you go. Well, of course there are important differences between the AGM and lithium batteries (AC/DC stuff I'm not fully aware of) and I suspect I will have to  make changes to the inverter (but if the current one is already busted...)
Feels like a high effort, high risk, high reward possibility...

###### Replace the inverter
Given the weird behavior, and the corrosion on the POWER SWITCH (is that the inverter?), I suspect something needs to be sorted on the inverter. Since the generator can still run the appliances but seemingly not charge the battery, I would guess there is a break in the circuit between inverter and house battery. But then how is the fridge pulling volts from the house battery? 

![breitenbush campground](/img/powerswitch.jpg)
##### <sup>Corrosion on the power switch</sup>

###### Upgrade the solar panel
So, I've been wanting to do this since before there were these power issues. I'm not sure whether I'll have to update the Kyocera Commander unit as well; the ideal would just be taking off the old panel, mounting the new ones on the roof tracks and plugging in new panel(s). However I have a vague recollection that the control unit can also have a big impact on what power you can get out of panels, so an update might be needed anyway?

That's basically where I am at today. Air quality is insanely bad outside right now, so I doubt I'm going to get to any of this on the weekend but I would love to hear from folks about what gaps I have in my understanding or plans.

[Posted this on the Sportsmobile forum](https://www.sportsmobileforum.com/forums/f20/van-house-power-trouble-shooting-26974.html#post281313)

And on the [Sportsmobile facebook group](https://www.facebook.com/groups/63027624960/permalink/10158282697314961)

![fuses on panel](/img/fuses-on-panel.jpg)
![low voltage](/img/low-voltage-panel.jpg)
![rc6 yellow cable](/img/RC6-yellow.jpg)
![Apline](/img/Apline.jpg)
![low voltage](/img/HI-AMP-BUSS-135A.jpg)
![inverter/charger](/img/traceM2512.jpg)