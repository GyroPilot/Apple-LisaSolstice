# LisaSolstice

The seasons on the Apple Lisa: days to the next solstice or equinox, the Earth's orbit and tilt, where the Sun is
overhead now, sunrise and sunset in your town, day and night on a world map, solstice traditions counted to this
year, fun facts, and pictures from history. It opens on the author's solargraph: six months of the Sun's path over
Cincinnati, exposed on film in a pop-can pinhole camera on his roof from the June to the December solstice. The
solstice history comes from Tim and Connie O'Connor's Winter Solstice talk.

Tool number **419326** in the GyroPilot series. Lisa Pascal, Workshop 3.0, Lisa Office System 3.1. LisaTwinClock's
clock is built in, so it also sets the Lisa's clock (in the twin year) by hand or from the network.

## Keys (also in the Seasons, Clock and Network menus)

| Key | Page |
|---|---|
| D | days to the next solstice or equinox, and the next five coming up |
| O / E | the Earth's orbit seen from above / its tilt, for today |
| W | where the Sun is straight overhead now |
| M | day and night now on a map of the world |
| Y | sunrise, sunset and daylight in your town (Seasons > Set Your Town / Set Your Time Zone) |
| L | solstice traditions: how many winter solstices old each one is |
| F | a fun fact (25) |
| G | the solargraph |
| P | pictures from history (six, P again for the next) |
| S / N / C / T | set the clock by hand / from the network / show it / about twin years |

## The network (optional)

N sets the clock from an **ESPFuji ESProFile** (its own clock), an **RS-232 FujiNet** on Serial B (its clock, or
timeapi.io for your town or a time zone), or a **LisaNet**. If the web gives no time, LisaSolstice falls back to the
FujiNet's / ESProFile's own clock and says so. Everything else works without a network.

## Pictures

- The solargraph: Tim O'Connor's own photograph.
- Newgrange plan and section: W. F. Wakeman, 1903, public domain.
- Midwinter sunlight in the Newgrange chamber: photo by Dentp, CC BY-SA 4.0
  (https://commons.wikimedia.org/wiki/File:2013_Solstice_Newgrange.jpg).
- Stonehenge at sunset: photo by Jeffrey Pfau, CC BY-SA 3.0
  (https://commons.wikimedia.org/wiki/File:Stonehenge_cloudy_sunset.jpg).
- Great Serpent Mound, an early postcard; the Yule log, a 19th-century wood engraving; the heavens, an engraving of
  the 1600s: public domain.

The two photos are 1-bit conversions for the Lisa screen, encoded as rows in `sources/SOL-PHOK.TEXT` and
`sources/SOL-PHOP.TEXT`; those conversions are shared under the same CC BY-SA licences as the photos. The rest of the
source code is MIT (LICENSE).

## Building

Copy `sources/SOL-*.TEXT` to the Lisa as SOL/<name>.TEXT (SOL-MAIN.TEXT -> SOL/MAIN.TEXT, SOL-PHOA.TEXT ->
SOL/PHOA.TEXT and so on) and `icon/SOLICONA.BIN` as SOL/ICON.BIN, then `R <SOL/MAKE` and `R <SOL/INSTALL`.
The picture units are generated: `tools/make_solpic.py` (the solargraph) and `tools/make_solpho.py` (the six pictures,
split into include files so each fits a crowded Workshop disk).

MIT licence (code). Tim O'Connor (bmwcyclist / GyroPilot), 2026.
