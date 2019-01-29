# GSoC 2019 Ideas

### ToxBlinkenwall (eWindow) - Overwiew

Link: <a href="https://github.com/Zoxcore/ToxBlinkenwall">https://github.com/Zoxcore/ToxBlinkenwall</a>

ToxBlinkenwall (eWindow) is an effort to develop Software and Hardware to provide a cheap, stable,
easy to use and secure System to have Video Conferences anywhere in the world.<br>
The Main Component is Tox.<br>
ToxBlinkenwall (eWindow) utilizes Tox (c-toxcore: <a href="https://toktok.ltd/index.html">https://toktok.ltd/index.html</a>)
as the library to handle all encryption and sending and receiving of data.<br>
Tox is an open source, distributed, peer-to-peer and end-to-end encrypted network library.<br>

ToxBlinkenwall (eWindow) builds upon Tox to give Videocalls and Videoconferencing to users and small companies.<br>
We are developing better and smoother Video and Audio transmission and also getting Hardware acceleration support
for some devices. All this while still staying distributed, without centralized Servers, and also as
little 3rd party libraries as possible (no WebRTC).<br>
This makes the code small and easy to compile on many different platforms.<br>

Our current Hardware focuses on the Raspberry Pi (since it's easy to obtain in many places and also cheap)
and the Android platform (as it is very flexible and readily available).

___
### Code Cleanup and Stability

<b>Brief Explanation:</b>
The Source Code for ToxBlinkenwall has evolved over the years, by quickly implementing features and ideas and
testing them out.<br>
This Process was great for fast progress, yet not so great for a clear and structured code base.<br>
We want to clean the Code, and fix some of the most common mistakes made.<br>

<b>Expected Results:</b>
- C Code is purged of unused functions and variables
- Most Common Bugs (SEGV) fixed
- Most Common Causes for Crashes fixed
- Write Documentation for Test Cases
- Create Code Test and/or Unit tests

<b>Knowledge Prerequisite:</b> Experience with C, Knowledge about Debugging (and Debugger Tools)

<b>Difficulty:</b> Easy

<b>Mentor:</b> strfry

___
### VideoConference (Video Call with more than 2 participants)

<b>Brief Explanation:</b>
Toxblinkenwall can handle 1-on-1 Video calls in 720p and 1080p at 25fps.<br>
This pushes the Hardware and Software of the Raspberry PI to the limit.<br>
But we are envisioning even more, we want to be able to Videocall with more than 2 parties at the
same time.<br>
The idea is to implement a way to show 3 or maybe even more Video Feeds on 1 Display Device,
and handle multiple Audio PCM streams incoming.<br>

<b>Expected Results:</b>
- 3 or more clients can video (including audio) call each other
- all incoming video streams are displayed optimally on the available screen
- all incoming audio streams are mixed properly, resulting in a natural sound output
- handle different aspect ratios on the Display Device of each participant
- handle different orientation of the Display Device of each participant

<b>Knowledge Prerequisite:</b> Experience with C, Knowledge about PCM Audio, Experience with Video Codecs

<b>Difficulty:</b> Hard

<b>Mentor:</b> strfry, zoff

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
- Add Hardware Accelerated Video Encoding Support
- Clean up the Source Code
- Remove Duplication in the Source as much as possible
- Write Tests for the Android App
- Implement the most asked for missing features: Ringtone Support and Export/Import Data Function

<b>Knowledge Prerequisite:</b> Experience with Java, Knowledge about Android

<b>Difficulty:</b> Hard

<b>Mentor:</b> zoff

