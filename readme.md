# awesome-reaper-pedalboard
Notes on how to set up a pedal board using a midi controller using reaper.

## Samples files
My configured pedal board can be found in [this file](pedalboard.RPP)

Caveat - this is a work in progress. I have only used tihs with a midi keyboard at the moment, and I am yet to collect my midi pedal board from storage.

## Motivation

Pedal board are big, expensive, hard to transport, have complicated power requirements and at times not very flexible. Avoiding some of these features would be a good thing, digital audio audio workstations can turn this sort of sound effect into code and so remove some of these physical costs.

On the other hand, pedal boards don't involve programming - rather you have a limited number of settings that you can tweak, and which to some degree can be "performed" or experimented in in real time with feedback, like a musical instrument.

This project seeks a middleground by producing a "pedal board" for a guitar, or another instrument, using a digital workspace (in this case reaper), but controlling with midi controllers (knobs and sliders on an external device). This still gives 


## Why Reaper

Reaper is not open source, this means that it's use requires you to think about money and licensing, there is a risk that the company behind it go out of business or don't care about a particular feature that is important to you. On the other hand, it is well documented by a community, extensible and scriptable and affordable compared to other tools and free to use for an evaluation period. Life is full of compromises, and perhaps the use of reaper - until such time as ardour catches up is an acceptable one. 

I also, know that reaper supports "midi automation" where midi input can be used to control parameters of sound effects.
 

## Alternatives and prior work 

There are some open source projects that act as amp sims sometimes combined with pedal board. Some posts about rakarack mention the posibility of midi automation.
Ardour is a full open-source digital audo workspace. I am not familiar with it it's effects plguins


* [rakarrack](https://rakarrack.sourceforge.net/) and guitarix are two examples.


## How to produce an amp sim and an effects pedal
Pedal board can be quite personal so you will likely want to tweak your settings, and perhaps even the equipment you use. But perhaps you would like to start by using the settings layed out here.

At a high-level, this works by having a sequence of tracks representing different pedals. Midi controls are mapped to parameters in these pedals representing the dials on the front of a guitar a pedal. We can however put all these dials in one place and place these on a desk. A midi footswitch is used to switch between these effects.



## Equipment

### Midi knobs
I used the [subzero mini midi controller](https://www.amazon.co.uk/SubZero-MINICONTROL-MIDI-Controller/dp/B079RL4S9F/ref=cm_cr_arp_d_product_top?ie=UTF8) to vary parameters of the board - which I bought second hand on ebay (I suspect the board is no longer being manufactured).

This board is perhaps more reminiscent of a track mixer with its sliders and nobs, it is however cheap and cheap means replaceable and small. A more appropriate control might have pairs dials for as is common on pedals. However if might be natural for pedals to have an "intensity setting" and a "control setting".







