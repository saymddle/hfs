HOW TO ADD WORSHIP SONGS
=========================

1. Drop your MP3 files into this "audio" folder.

2. Open worship.html in a text editor.

3. Find the <audio> tag for the song you want to update, for example:

   <audio controls preload="none" class="track-audio">
     <source src="audio/fire-falls-down.mp3" type="audio/mpeg">
     Your browser does not support the audio element.
   </audio>

4. Change the file name inside src="audio/____.mp3" to match
   the exact name of your MP3 file (keep it inside the audio/ folder).

5. Update the song title, time, and track number text above the
   <audio> tag to match your song.

To add a brand new song (not just replace one of the 4 placeholders),
copy one whole "track-card" block in worship.html, paste it as a new
block in the list, and update its details + filename the same way.
