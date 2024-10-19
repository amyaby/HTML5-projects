in this small projects we tired to translate and put the subtiles of a video 
usinf #WEBVTT
1-in an st_specify language.vtt u write the time rang with the words that've been said there :
```lua
hh:mm:ss.milliseconds --> hh:mm:ss.milliseconds
```
and don't forget to split each paragraph said with a number so things will be organised 
and under each time range write the translation or the subtitles .
once u finish writing ur .vtt files 
u move to the core which is your html file in the body you use this command:

```html
<body>
    <video controls>
        <source src="vidéo.mp4" type='video/mp4'>
        <track src="st_en.vtt" kind="subtitles" srclang="en" label="english" >
        <track src="st_fr.vtt" kind="subtitles" srclang="fr" label="frensh" >
    </video>
</body>
```

after **src** we always write the URL of the file 

**kind:**

`Description`: This attribute indicates the type of text track. Possible values include:
`subtitles:` Used for subtitles that translate the spoken dialogue.
`captions:` Used for captions that include not only dialogue but also non-speech elements (like sound effects).
`descriptions:` Provides descriptions of the video content for visually impaired users.
`chapters:` Used for chapters in the video.
after srclang we write the 

# SUMMARY

**src:** Necessary for specifying the subtitle file location.
**kind:** Recommended for clarity on the track type; not strictly necessary.
**srclang:** Not required but useful for language identification.
**label:** Optional but improves user experience by providing a descriptive name for the track.
