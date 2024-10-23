---
layout: post
title: Live Glitch Visuals w/ Music (#1)
date: 2024-10-23
categories: av
custom_excerpt: A quick exploratory project relating to live, glitchy visuals synced to music.
---

### TL:DR

I found a cool way to generate live visuals on the fly with audio input to control some effects. I'm still exploring ways to reduce latency and improve the experience both for the user (video DJ?) and the viewer.

### Demo?

Ok admittedly I've only just started using this set up and have barely any practice using it. On top of that I am still adjusting and finding better ways to make cool stuff happen. So I don't have anything worth showing off yet, but I will hopefully have something cool soon. I'll link to it here when it's ready.

### Tools

[**PhotoMosh Pro**](https://photomosh.com) - Program for creating cool glitchy visuals. Can take a webcam of file input for video, as well as microphone or audio file input to modulate effects.

[**OBS**](https://obsproject.com/) - Recording/streaming software for capturing base visuals. 

[**VoiceMeeter**](https://vb-audio.com/Voicemeeter/) - Software for routing audio between programs virtually.

[**VSTHost**](https://www.hermannseib.com/english/vsthost.htm) - Program for loading audio effects.

### How's it work?

{:refdef: style="text-align: center;"}
![Live Glitch Workflow](/assets/misc/glitch-flow.png)
{: refdef}

PhotoMosh is a super versatile tool for creating photos and recorded videos, but it has some limitations that make it difficult to use live. The main limitations is the input modes- it only accepts photo/video files or a webcam as input on the visual side, and only audio files or microphone as input on the audio side. For my application, I wanted to be able to feed it videos from the internet and have more control over those videos ahead of time. I also wanted to be able to take an audio input from my PC live instead of having it pre-recorded.

The video input aspect of this is fairly straightforward. I can use **OBS**'s Virtual Camera feature to grab videos from anywhere I want- capture card input, webcams, YouTube videos, or any other program. I can have multiple captures going at once and combine them in different ways, even apply some effects right through OBS. This is then output by OBS and recognized by my PC as a webcam. PhotoMosh can then take that input, and now we have a much more flexible way to adjust the incoming video signal for this program.

The audio is a more involved process due to some practical reasons. First, I wanted to be able to grab audio from anywhere. For practicing using this setup, it is useful to be able to play music off Spotify or SoundCloud. In a concert setting though, I would be grabbing an aux output from an artist's track to use. The solution I found is using a tool called **VoiceMeeter**. This program creates a bunch of virtual audio inputs and outputs to allow you to route audio signals between programs and speakers. 

So I take an audio source, in this case Spotify. I use VoiceMeeter to route that signal right back out my desktop speakers (Note: in a concert setting this would be unnecessary, as my PC would not be the audio source). Then I also route this audio signal through **VSTHost**. This program allows me to apply audio effects to the signal. I can use this to isolate out certain sounds, like if I only want the bass or the hihat to effect the visuals. From VSTHost, I route the signal back through VoiceMeeter, where this time I send the modified signal to my headphones. This way I can monitor the signal as I change it with effects to make sure I'm isolating the right parts. This signal also finally gets sent into PhotoMosh as a simulated microphone. 

### How do you use it?

{:refdef: style="text-align: center;"}
![Sample Glitch Output](/assets/misc/glitch-out.png)
{: refdef}

Ok so that's the setup, but how do you actually use it? First step, pull up an interesting video either already on the PC, or right from YouTube. Capture this video using OBS. Then play some music. Find the frequencies you want to use to control an effect and use an EQ, gate, or other audio effect to manipulate it to your liking. Then through PhotoMosh, start glitching by adjusting parameters. Use that audio signal to control any effects and that's it! You can adjust video input, change effects, and adjust the audio effects live without much difficulty.

### Problems and Next Steps

The main issue in this project is latency. VoiceMeeter is fairly quick but I can still audibly hear an offset listening to the two different output signals. Removing the audio effects from the stream speeds things up a bit, but then I don't have as fine control over the effects as I would like. PhotoMosh also has fairly significant latency. 

So how can I improve this? If it's possible to know the tracks that might be played at a concert ahead of time (i.e. a set list), then tracks could be prepared ahead of time with audio effects already applied to isolate target signals. This isn't as dynamic, but would speed things up significantly. Another option would be to use hardware effects on the audio input, e.g. EQ and gate pedals.

I'm also interested in exploring some other glitch and live visual tools. I've played around with some live coding for audio, but haven't tried out any visual languages. I'm guessing this would be less user friendly but probably more versatile once I got the hang of things. I've also seen some other cool glitch software such as [**FFglitch**](https://ffglitch.org/what/), but I haven't even begun to explore that yet. Basically I just wanted to get this out there so I can look back and reference it as my workflow here changes.