---
layout: post
title: "Keyboard from Scratch"
excerpt: "Building a custom programmable ortholinear keyboard from scratch with the qmk_firmware"
categories:
  - Microcontrollers
tags:
  - microcontroller
  - ortholinear
  - teensy
  - keyboard
  - electronics
  - colemak
last_modified_at: 2018-03-23 11:56
---

# Intro

I have been using mechanical keyboards for a while now and frankly, I never want to go back. After reading about custom keyboard layouts, alternative arrangement of keys and open-source keyboard firmwares, I decided to give it a try. I was looking for something minimalistic, portable and usefull. Also it had to be something with an open-source firmware I could modify to my needs.

I discovered the the keyboards at https://olkb.com/ and others which matched what I was looking for, but they where sold out at that moment. Other options where too expensive or just "not right" (I might have been picky). Long story short: I decided to build my own.

Where is the fun in just buying one? Also, how hard can it be?

# Design Decisions

## Ortholinear

> Ortho... What?!

The term "ortholinear" refers to a layout of the switches
on a keyboard, where the keys are aligned vertically and
horizontally, compared to standard staggered keyboards.
The staggering of keys on most of todays keyboards is
based on the way they had to be placed on typewriters to
be able to arrang the "arms" that hold the keys. These
mechanical reasons are obviously redundant on a computer
keyboard.

Though there are no known studies to prove it, the idea is that your fingers move forward and backward when bend, not sideways. Also the arrangment makes it more space-efficient allowing for the fingers to move less when typing.

More ergonomic or not, I liked the idea and the reasoning behind it. Also it looks awesome and is easier to build. I decided to go with a key arrangement like the one on the [Planck Keyboard](https://olkb.com/planck), that is 4x12 equally sized keys with the exception of the space bar, which takes up two units.

## Switches

When it comes to the switches in a keyboard you basically have to choose
between to categories: Mechanical or rubber dome.



![placeholder](/assets/img/switch-const.png)

Image from [OLKB Maker Fair Posters](https://www.dropbox.com/s/jjo98z2f1cd9ifw/olkb-maker-faire.pdf?dl=0)


If you have ever typed on a mechanical keyboard you will be spoiled and never want to go back. Rubber dome (or membrane) keyboards are cheap to manufacture but high-quality keybaords will use mechanical switches in most cases as they feel better and last way longer.

Probably the most important choice when choosing or building a mechanical keyboard will be the switch type. There are queite a few there and a lot of explanations on the differences.


![placeholder](/assets/img/switch-types.png)

Image from [OLKB Maker Fair Posters](https://www.dropbox.com/s/jjo98z2f1cd9ifw/olkb-maker-faire.pdf?dl=0)

I decided to go with Cherry MX Brown switches after trying the different types on a tester.

## Keycaps

Keycaps are the plastic caps you push your finger against when typing. They can be replaced and are not a part of the actual switch, meaning you have to get them separately.

Keycaps for mechanical keyboard can have different shapes, that is the profile of the keycap as well as the touch area can have different forms. There are three standard keycap families

#### DSC Family
![placeholder](/assets/img/DCS-family.jpg)
medium profile, cylindrical top, sculptured.

#### DSA Family
![placeholder](/assets/img/DSA-family.jpg)
medium profile, spherical top, non-sculptured.

#### SA Family
![placeholder](/assets/img/SA-family.jpg)
high profile, spherical top, sculptured.

#### G20 Family
![placeholder](/assets/img/pmk-g20-family.jpg)
medium profile, flat top, non-sculptured

If you are interested on more in-depth information about keycaps and shapes you can visit this [Wiki on Reddit](https://www.reddit.com/r/MechanicalKeyboards/wiki/keycap_guides)

I decided to go with DSA keycaps as they feel the the most comfortable to me and allow to switch they keys between each other because they all have the same form.

## Microcontroller

For the microcontroller I decided to go with a [Teensy 2.0](https://www.pjrc.com/store/teensy.html). It has 25 I/O pins wwhich is enough for what I want to build. These microcotrollers get used a lot for custom keyboard builds, so there is a lot of information out there and the firmware I plan to use supports it. It can act as a keybord controller, so no additional software or drivers will have tho be installed on the computers I connect the keyboard to later on.

Also it is small enough to fit in a pretty flat case, which is desirable to make the keyboard more ergonomic.

## Wiring

Since I don't have the stuff at home to etch PCBs at home, I will be making all connection with simple wires.

There is a good tutorial on how to wire a keyboard with only wires and diodes [here](http://blog.roastpotatoes.co/guide/2015/11/04/how-to-handwire-a-planck/). Basically you put a diode on each swich and then wire each row and each column to a pin on the microcontroller.

The result looks something like this:

![placeholder](/assets/img/planck-wiring.png)

## Firmware

For the firmware I want to use the [QMK Firmware](http://qmk.fm/). It is open source and widely used. Adding my custom layout shouldn't be a problem and it already has all nessesary functions I desire like support for backlight and custom programming of keys and key-combinations.

## Keymap and Layers

## Backlight

# Building the Keyboard
## Materials
## Case and Baseplate

# Setting up the Firmware
## Adapting the Firmware
### Switch wiring
### Keyboard Layers
### RGB Lighting
## Flashing it on the Keyboard



-----
A footer Link <a href="https://github.com/binaryplease">Link Text</a>
