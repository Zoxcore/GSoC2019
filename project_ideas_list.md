# GSoC 2019 Ideas

### ToxBlinkenwall (eWindow) - Overview

Link: <a href="https://github.com/Zoxcore/ToxBlinkenwall">https://github.com/Zoxcore/ToxBlinkenwall</a>

ToxBlinkenwall (eWindow) is an effort to develop Software and Hardware to provide a cheap, stable,
easy to use and secure System to have Video Conferences anywhere in the world.<br>
The Main Component is Tox.<br>
ToxBlinkenwall (eWindow) utilizes Tox (c-toxcore: <a href="https://toktok.ltd/index.html">https://toktok.ltd/index.html</a>)
as the library to handle all encryption and the sending and receiving of data.<br>
Tox is an open source, distributed, peer-to-peer and end-to-end encrypted network library.<br>

ToxBlinkenwall (eWindow) builds upon Tox to give Videocalls and Videoconferencing to users and small companies.<br>
We are developing better and smoother Video and Audio transmission and also getting Hardware acceleration support
for some devices. All this while still staying distributed, without centralized Servers, and also using as
little in the way of 3rd party libraries as possible (no WebRTC).<br>
This makes the code small and easy to compile on many different platforms.<br>

Our current Hardware focuses on the Raspberry Pi (since it's easy to obtain in many places and also cheap)
and the Android platform (as it is very flexible and readily available).

___
### VideoConference (Video Call with more than 2 participants)

<b>Brief Explanation:</b>
Toxblinkenwall can handle 1-on-1 Video calls in 720p and 1080p at 25fps.<br>
This pushes the Hardware and Software of the Raspberry PI to the limit.<br>
But we are envisioning even more: we want to be able to Videocall with more than 2 parties at the
same time.<br>
The idea is to implement a way to show 3 or maybe even more Video Feeds on 1 Display Device,
and handle multiple incoming Audio PCM streams.<br>

<b>Expected Results:</b>
- 3 or more clients can video call (including audio) each other
- all incoming video streams are displayed optimally on the available screen
- all incoming audio streams are mixed properly, resulting in a natural sound output

<b>Knowledge Prerequisites:</b> Experience with C, Knowledge about PCM Audio, Experience with Video Codecs

<b>Difficulty:</b> Medium

<b>Mentor:</b> [strfry](https://github.com/strfry), [zoff](https://github.com/zoff99)

___
### Rotational Diversity: Introduce Portrait-Mode Video


<b>Brief Explanation:</b>
Toxblinkenwall currently assumes a default "wide" display configuration, like 4:3 or 16:9 aspect ratio.
From a design point of view, some users prefer an upright, "portrait-mode" aspect ratio.
This currently can only be done by rotating the camera, and living with distorted UI elements.<br>
To solve this, the communication protocol must be enhanced to negotiate the peers display and camera orientation, so that the endpoints can rotate the video and UI elements accordingly.

<b>Expected Results:</b>
- ToxBlinkenwall can be used in both landscape and portrait mode
- UI elements are drawn correctly
- Participants can have different display and camera orientations

<b>Knowledge Prerequisites:</b> Experience with C, Experience with graphics programming

<b>Difficulty:</b> Easy

<b>Mentor:</b> [strfry](https://github.com/strfry), [zoff](https://github.com/zoff99)

___
### Improve User Experience in the Android Client (TRIfA)
<b>Brief Explanation:</b>
Since TRIfA [https://github.com/zoff99/ToxAndroidRefImpl] is now the main Android Client for Tox,
we would really like to improve the User Experience with this Application.<br>
The Android Application was created in one Weekend (almost by accident, see our talk at ToxCon 2018
[Slides](https://github.com/zoff99/ToxCon2018/blob/master/slides/zoff_echobot_to_trifa.pdf))
and it is very stable and great.<br>
But we want even more.<br>
Users have been asking for some features that they are missing from the Application.<br>

<b>Expected Results:</b>
- Perform usability testing with documented results.
- Define UX improvements based on the test results.
- Add Hardware Accelerated Video Encoding Support
- Clean up the Source Code
- Remove Duplication in the Source as much as possible
- Write Tests for the Android App
- Implement the most asked for missing features: Ringtone Support and Export/Import Data Function

<b>Knowledge Prerequisites:</b> Experience with Java, Knowledge about Android

<b>Difficulty:</b> Hard

<b>Mentor:</b> [iphydf](https://github.com/iphydf), [zoff](https://github.com/zoff99)

___
### Build Lightweight Bootable Live Image of ToxBlinkenwall (eWindow)
<b>Brief Explanation:</b>
An interesting use case for ToxBlinkenwall (eWindow) is to take an old laptop and repurpose it into a dedicated Videochat station.
For this we need a live-booting USB image with the ToxBlinkenwall software on it.
Ideally it would be based on a light-weight linux distribution, like Alpine Linux.

<b>Expected Results:</b>
- Bootable Image for x86 with 
- CI flow to create updated images
- Auto-Configuration OR setup dialogs for various hardware configurations
- Implement persistent storage methods to retain keys and connections
- Implement update mechanism, or self-hosting build capability


<b>Knowledge Prerequisites:</b> Experience with Distro packaging, Linux boot process, Shell Scripting

<b>Difficulty:</b> Medium

<b>Mentor:</b> [strfry](https://github.com/strfry), [robinli](https://github.com/robinlinden)


___
### Code Cleanup and Stability

<b>Brief Explanation:</b>
The Source Code for ToxBlinkenwall (eWindow) has evolved over the years, by quickly implementing features and ideas and
testing them out.<br>
This Process was great for fast progress, yet not so great for a clear and structured code base.<br>
We want to clean the Code, and fix some of the most common mistakes made.<br>

<b>Expected Results:</b>
- Code follows common modularity guidelines and design principles.
- C Code is purged of unused functions and variables
- Most Common Bugs (SEGV) fixed
- Most Common Causes for Crashes fixed
- Write Documentation for Test Cases
- Create Code Test and/or Unit tests

<b>Knowledge Prerequisites:</b> Experience with C, Knowledge about Debugging (and Debugger Tools)

<b>Difficulty:</b> Easy

<b>Mentor:</b> [iphydf](https://github.com/iphydf), [strfry](https://github.com/strfry), [robinli](https://github.com/robinlinden), [zugz](https://github.com/zugz)


___
###
