# awesome-reaper-pedalboard
Notes on how to set up a pedal board using a midi controller using reaper.

## Samples files
My configured pedal board can be found in [this file](pedalboard.RPP)

Caveat - this is a work in progress. I have only used tihs with a midi keyboard at the moment, and I am yet to collect my midi pedal board from storage.

## Motivation
Pedal board are big, expensive, hard to transport, have complicated power requirements and at times not very flexible. Avoiding some of these features would be a good thing, digital audio audio workstations can turn this sort of sound effect into code and so remove some of these physical costs.

On the other hand, pedal boards don't involve programming - rather you have a limited number of settings that you can tweak, and which to some degree can be "performed" or experimented in in real time with feedback, like a musical instrument.

This project seeks a middleground by producing a "pedal board" for a guitar, or another instrument, using a digital workspace (in this case reaper), but controlling with midi controllers (knobs and sliders on an external device). This still gives 


### Not to do 
The aim here is construct a tool that can be played without interacting generally with a computer.

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

Faderfox offered some nice midi controllers that mostly consist of knobs, but these are relatively expensive. I also saw some options on etsy which were more affordable, though I have had problems with receiving broken electronics on etsy before and the products may not be easily replaceable.

### An old mac laptop
I originally used a linux laptop run but wanted my set up to support a digital piano sound and found it difficult to find VST plugins for linux. There were tools which promised to convert windows VST plugins to linux ones or provide bridges but they were not trivial to use, so I elected to use an old mac machine.

You'll note that a dedicatd machine is probably more expensive than a reasonable amplifier. Headphone amplifiers are very cheap and you could likely buy 5 or six pedals for a similar price. People have however [run Reaper on single board computers such as raspberry pi](https://www.youtube.com/watch?v=ASszi2F495E) and a linux machine is more compact.

### A digital audio converter (for guitar) DAC
I am using [The Behringer UCG102](https://www.behringer.com/behringer/product?modelCode=P0198) which has the advantage of being cheap and small.

### An electric piano (if you want to play piano)

I bought a yamaha p-45, which I understand from youtube videos is one of the cheapest "electric pianos" that you can buy. Electric piano's have key weightings designed to simulate a piano.


### Ways of having less hardware

My motivation is to create a dedicated set up using midi controllers to "get away from hardware" and avoid too much iteraction with a computer. However, others may wish to spend less money, or own fewer things. There are some approaches here.

The midi controller could be replaced with [Touch OSC](https://www.youtube.com/watch?v=hmuhoDx70QM) which allows an Android or iOS phone or tablet to control reaper via midi events. The desktop component of touch osc runs on windows, mac or linux.

I am using a dedicated laptop to run reaper, a raspberry pi can reaper and would reduce costs and the size of the set up. Alternatively a "part time" laptop could be used.

# Features

The most important feature for making playing "fun" is a looper plugin.

# Plugins I used
https://www.meldaproduction.com/downloads Third party free plugins. I used the metronome
https://audiolatry.gumroad.com/l/grandpianoxxl -- A free properitary  sampled piano midi instruments

# Reading
* https://plugins4free.com A large collection of free VST plugins that are compatible with reaper (depending on your underlying architecture).
* https://github.com/webprofusion/OpenAudio A large list of open source VST plugins and other tools.
* https://tonehunt.org/ A large collection of amp sims for use with the neural amp

# Trouble shooting Reaper

## My midi control has stopped working

Try unplugging your midi controller, going to preferences, right clicking on the midi device and forgetting it, then plugging it back in again and enabling it. I had to do this once.
