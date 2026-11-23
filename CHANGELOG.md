# Changelog

## 1.0.35
- FF / REW now whirr like a drive searching; the pitch climbs while the button is held.
- New spin-up on PLAY, new disc loading sound (tray closing with a thud), and a case open / close sound for the library.

## 1.0.34
- Disc loading uses the new eject sound played backwards again (soft, no latch click at the end).

## 1.0.33
- Disc loading is back on the original insert sound; the new eject and the new clicks stay.

## 1.0.32
- New key clicks: left and right variants, alternating on each key press.
- New eject sound. Drive spin-up on PLAY and the hum are unchanged.

## 1.0.31
- Clean-up: the click helper is simplified now that pads, key release and the switches are silent; unused CSS removed (`.led.cuep`, `.led.loopp`, `#lib .lf`). No unused functions or variables found.

## 1.0.30
- CRUSH and FILTER switches no longer click.

## 1.0.29
- Landscape: the board packages are calmer (lighter bodies, softer marks, a slightly smaller main chip).

## 1.0.28
- Board packages sit under the frosted glass again, but stay solid (not see-through); the glass softens them.

## 1.0.27
- Board packages are solid now: drawn above the frosted glass in both layouts, with darker bodies, pins and markings.

## 1.0.26
- Board detail: drawn IC packages (bevelled body, pins on four sides, pin-1 dot, markings), test points TP1-TP3, a crystal can and resistor arrays. Landscape gets a QFP and test points on the left, a vertical MCU, crystal and resistors on the right; portrait gets the new packages and a row of test points. All faint, clear of the disc, display and buttons.

## 1.0.25
- Cue pads and key release no longer click (it was lost under the music). Keys, switches, disc and drive sounds stay.

## 1.0.24
- The old synthesised UI and disc sounds are removed; everything now plays from the recorded clips (pads and key release use the same click at other pitches). The clips are decoded as soon as audio starts.

## 1.0.23
- Lighter idle: while paused and nothing moves, the main loop runs about 20 steps a second instead of 60. A touch, a message, HELP, play or any motion wakes it at once.

## 1.0.22
- Accessibility: roles and labels on buttons, pads, transport, switches (CRUSH, FILTER), the VARISPEED slider and the display.
- Page zoom allowed again (`user-scalable=no` removed; the player itself still ignores touch gestures).
- Manifest: 192 px and maskable 512 px icons added.
- Read errors name the file and stay for 6 seconds.

## 1.0.21
- Screens refreshed; new screen with the white disc.

## 1.0.20
- The red line on the VARISPEED fader cap is removed.

## 1.0.19
- The red mark on the drive slider and the red stripe on the deck are removed.

## 1.0.18
- Recorded drive sounds: disc drop and spin-up, eject of the previous disc, spin-up on PLAY, a quiet drive hum while playing, and sampled key/switch clicks. All gated by the CLICKS toggle (long press LIB). The synthesised sounds stay as a fallback until the clips are decoded.
- Clips are short mono mp3 (about 45 KB in total) embedded in index.html.

## 1.0.17

- The drive under the clear disc is now a moulded deck instead of drawn parts: recessed wells for the spindle motor and the pivot, and a curved slot in which a small slider travels from the hub to the rim as the disc plays (it follows scratching and search). The swing arm of 1.0.16 is gone.

## 1.0.16

- The drive under the clear disc: a thin line-art plate (scale, screws, spindle motor) and a swing-arm pickup with an orange flex cable. The arm swings from the hub to the rim as the disc plays, and follows scratching and search. Hidden on the WHITE disc. Compositor-only motion.

## 1.0.15

- The rainbow sheen is only drawn on the clear (COLOR) disc. On the WHITE disc it hides itself; the IRIS switch keeps its setting and the sheen returns when you flip the disc back.

## 1.0.14

- Label editor: a bigger disc (340 px in portrait, 290 px in landscape) and the whole layout sits in the middle of the screen instead of hugging the top. In landscape the fields and styles are two columns next to the disc.

## 1.0.13

- The CRUSH and FILTER switches have a taller invisible touch area (46 pt tall on a 390 pt wide phone, was about 34 pt). The look is unchanged.

## 1.0.12

- Label editor in landscape: RESET and OK sit right under the style buttons instead of at the bottom of the column.

## 1.0.11

- Fix: a disc longer than about 11 minutes never started playing (decode-first waited for a buffer that was never kept, and decoded again and again, up to 800 MB). Discs over 10 minutes are now never decoded: they play straight from the audio element (no waveform or BPM for them, no memory spike). A decoded buffer that is not kept no longer blocks play either.

## 1.0.10

- Label editor in landscape: three columns (disc, text lines, styles with RESET / OK) that fit a phone screen without scrolling.

## 1.0.9

- Label editor is bigger: larger preview disc, taller input lines with 18 px type (iOS no longer zooms the page when a line is focused), larger style buttons in four columns, bigger RESET / OK.

## 1.0.8

- Clean-up: the dead CSS of the old help overlay, the unused lite-mode and scale rules, and three unused JS leftovers are gone (about 3 KB). Nothing visible changes.
- Label style H also keeps its title clear of the printed rim text.
- All pictures in `screens/` are re-shot from this version.

## 1.0.7

- The white gloss band and its motion-permission prompt are gone; the rainbow sheen (IRIS) is the only reflection now.
- Label style H: the handwritten title and artist are placed by the disc's width at their height, so they no longer cross the rim.

## 1.0.6

- Rainbow sheen: a spectrum layer above the label that stays put against the light while the disc turns under it, drifts slowly with the spin and follows your finger. It is its own switch (IRIS, next to JOG), separate from the white gloss, needs no permission and moves on the compositor only.

## 1.0.5

- Labels: long titles and artists are squeezed instead of cut with an ellipsis; style H keeps clear of the hub; the bar in style C follows the artist block.
- Cover art: the picture embedded in MP3 / FLAC / M4A files is shown on the lock screen and in the media controls.
- New label style ART (in the label editor): the cover fills the disc. It is never chosen automatically; AUTO keeps the printed styles.

## 1.0.4

- The spindle is now a low, tidy motor cap: a thin metal rim, three small flush clamps and a centre pin.

## 1.0.3

- Loading a disc now works like a tape deck: the file is decoded first (DECODING), then it plays from the buffer. The sound no longer starts on the media element and gets handed over to the scratch engine in the middle of playback, which is where the freezes and the silent moments came from.
- A silent looping element keeps playback alive with the screen locked.
- Files over 110 MB still play straight from the media element.

## 1.0.2

- The centre of the disc is drawn like a real CD: a dark clamping band, a light rim, a clear zone with a stacking ring, and the three-claw spindle on top.

## 1.0.1

- Long artist names now wrap onto a second line on the disc labels instead of being cut.
- Loading a disc shows DECODING while the pitch / scratch engine prepares and READY when it is done; the heavy steps yield to the screen between each other.

## 1.0

First complete release.

**Player**
- Buffer engine with smooth VARISPEED, LOCK (WSOLA pitch lock), scratch and tape-style search; the plain `<audio>` path stays for long files and the locked screen.
- 8 hot cues per file, A-B loop with points that snap to the beat grid, MAIN CUE, beat jump, auto loops and loop roll.
- BPM and beat grid detection (cached), SYNC, QUANTIZE, tap tempo with a `?` mark when the detector is unsure.
- AUTOMIX (4 / 8 / 16 s): the next disc is decoded ahead and crossfades on the beat grid. Heavy track pairs skip it to protect memory on iPhone.
- Play modes: normal, repeat one, repeat all, shuffle. Hold PLAY to stop.
- FX: digital CRUSH and a one-knob FILTER; fixed output level and limiter.

**Disc and look**
- Translucent disc over a PCB, a recessed well, a three-claw spindle that turns with the disc.
- Eight printed label styles (classic, banner, technical, dotted, ruled card, rings, stripe, handwritten) plus blank, editable per disc.
- Disc change: a frosted shutter slides over the disc while the label changes; the sound fades out and back in.
- Group captions on the panel, a grouped top row with the AUTOMIX lamps, PADS / FX pages.
- Landscape mode with a frosted control bar and group captions; portrait, tablet and desktop layouts.

**Stability**
- Disc analysis runs in short slices, so the screen stays responsive after loading a disc.
- Next-disc prefetch is skipped for heavy tracks (iOS memory), the master level can no longer stay muted after a change.
