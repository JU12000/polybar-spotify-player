# About

For users of [spotify-player](https://github.com/aome510/spotify-player) and [polybar](https://github.com/polybar/polybar).

This script will retrieve the current Spotify Playback (what's currently at the top of the queue on your active device).
It shows both the play/pause state and the name of the song and artists. The name and artists will scroll above a certain length
which can be edited by changing the script directly.

The script uses `spotify-player` to get the current Playback directly from Spotify as long as `spotify-player` or the `spotify-player`
daemon are running. This means if you play a song on any device it will show when using this script. This allows you to remotely control
playback e.g. on your phone from `polybar` as long as `spotify-player` is open!

## Installation

Clone this repository and copy the shell script to `~/.config/polybar/scripts/`.

Make sure the script is executable `chmod +x polybar-spotify-current-playback`, and add it to your polybar config:

```ini
[module/polybar-spotify-current-playback]
type = custom/script
tail = true
exec = ~/.config/polybar/scripts/polybar-spotify-current-playback

; Optional: Left click to play/pause the current playback.
; click-left = spotify_player playback play-pause
```
Don't forget to add the module to your bar!
