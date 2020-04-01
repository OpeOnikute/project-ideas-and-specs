# Dance-Dance AfroNation
An app that plays random songs with a dance style for you to dance to. Each round will be 1-2 minutes.
You can record yourself dancing to the different songs and share.

## Feature Timeline
- Curate songs based on Dance styles.
- Play random songs on the browser based on the dance style. Songs should be split into 2 minutes.
- Record the user dancing and save video.
- Add the song name and dance style to the video.

## Dance styles
- [ ] Azonto
- [ ] Etigi
- [ ] Alanta
- [ ] Swo
- [ ] Skelewu
- [ ] Legwork
- [ ] Shakiti Bobo
- [ ] Yahooze
- [ ] Gweta

# Technical Sturvs
- dance styles will be an array of objects with the style as key and an array of songs as the value.
- each dance style will have an array of songs.
- to create the sound, we select 5 songs and pick out (2 minutes = 120 seconds. 120/5 = 24 seconds from each song) using an audio sprite.
- we would play each song from 1:00 so it is lit by that time.
- push each song into the final array and make sure they're preloaded.
- To play, pop a song from the array, play it and set timeout to pop the next song and play it.
- when there's no song in the array again, stop.

Loading songs
- Load each song in the array and set a hook for when it loads to count that all songs have loaded.
- If a user clicks play and not all songs have loaded, poll till they have all loaded.
- If 30 seconds reaches and still no show, replace the songs that haven't loaded. 