# MA Browser Card

## V 3.5.8 (fork)
Fix (fork: DrHack1)
Loading toast moved to the top of the card (the bottom could be clipped when the
card overflows a popup dialog) and is now also triggered from _playMedia, so it
shows for every play path. High-contrast gold pill.

## V 3.5.7 (fork)
Fix (fork: DrHack1)
Tap-to-play feedback is now a clear "Loading…" toast at the bottom of the card
(plus the tile spinner), so feedback is guaranteed visible regardless of which
item type was tapped.

## V 3.5.6 (fork)
Fixes/improvements (fork: DrHack1)
- `height` now accepts a CSS length string (e.g. "82vh") so the card can fill a
  responsive container such as a popup, instead of only fixed pixels.
- Tap-to-play loading spinner is now clearly visible (fixed a transform conflict
  that hid it) and stays up for at least 700ms so it can't flash-and-vanish.

## V 3.5.5 (fork)
New options (fork: DrHack1)
`hide_sidebar` and `hide_player` (both default false). Hide the left sidebar
(logo + nav menus) and/or the bottom player bar, leaving a full-width search +
content view — handy for embedding the card in a compact popup. Hidden elements
stay in the DOM so player selection and playback still work.

## V 3.5.4 (fork)
Improvement (fork: DrHack1)
Instant tap-to-play feedback. Tapping an album/playlist/track now immediately
shows a loading spinner on that tile (covering the lag before audio starts),
cleared automatically once the player reports the new track playing, with a
15s safety timeout.

## V 3.5.3 (fork)
New Feature (fork: DrHack1)
Favourites can now appear on the home screen. New `home_sections` keys
(all default 0 = off, shown above the existing sections):
`favorite_playlists`, `favorite_albums`, `favorite_artists`, `favorite_tracks`.
Reuses the existing favourites library fetch (`get_library` with `favorite: true`)
and tap-to-play grids.

## V 3.5.2
Fixed a bug in the artwork fetch

## V 3.5.1
Increased the maximum limit for the UI slider controlling card height to 2500px

## V 3.5.0
New Feature
You can now resize artwork tiles.

Bug Fix
Updated the way artwork is fetched to compensate for the deprecation of the old method by MA

## V 3.4.0b
Added compatibility with HA 2026.6 new card suggestion feature

## V 3.3.0
Added the ability to configure the card using the Home Assistant UI.

Removed a duplicate waitWS command.
Fixed a bug where event listener wasn't removed correctly.

## V 3.2.0
A redesign of the Retro theme

## V 3.1.0
#### **New Features**
- New "retro" theme
- Can now adjust the number of items shown in each section on the home screen

### **Bug Fixes**
- Fixed an issue where sections would sometimes disappear when updating the dashboard theme or card
- Volume symbol now fits the themes better

## V 3.0.1
- HACs store compatibility update

## V 3.0.0
#### **New Features**
- Adjustable side bar size
- Ability to move player to top or bottom
- Ability to move the sidebar to the top, then move player to top or bottom
- Can now customise the header bar icon, main title and subtitle or hide it completely
- Set default action to enqueue now as well as play

### **Bug Fixes**
- Fixed an issue where recently added media would not be fetched correctly. MA token now required to display this correctly

## V 2.1.0

#### **New Features**
**Themes**
- Select light or dark card themes
- Select auto (default) to copy your dashboard Theme

#### **Visual Improvements**
- Changed Radio & Search icons to fit with the visuals of the rest of the card
- Stopped the playback controls rendering as emoji on certain devices

## V 2.0.0
Initial public release
