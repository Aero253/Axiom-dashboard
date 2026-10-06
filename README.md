# Axiom

A personal dot-matrix dashboard for cabin crew, in black and white, with one red line on the globe for the day’s route. It's one HTML file, and it runs fully offline.

## Widgets
**On the board at first**
- **Clock & next duty:** Bangkok time, UTC (Z), week number, and a countdown to your next report.
- **Roster calendar:** import the eCrew *Personal Crew Schedule Report* PDF, or paste its text. Monthly totals are underneath.
  - ● flight
  - ○ standby
  - ◐ reserve
  - · day off
  - ◉ leave
- **Sun and Weather:** your base and roster cities appear by themselves. Tap the pencil to change or remove any of them, or add your own (up to 8). Weather for a new city loads the next time you're online.
- **Selected day:** your sectors, report and off-duty times, and your own plans for that day. Tap + next to Your plans, enter the time and plan, and tap ✓.
- **Next 7 days:** your roster for the coming week. Tap a day to open it.
- **Duty hours:** duty hours over the last 7, 14 and 28 days, and flight hours over 28 days, against the chapter 7 limits used in SL Swap Check. It also shows the rest you'll have before your next report. This is unofficial.
- **Weather:** live when online, for DMK and your next 7 days of destinations. Offline it keeps the last forecast.
- **Globe:** Thailand's dots are bigger and fully lit, and the rest of the world is dimmed, so home stands out. Zooming in adds more dots across the whole globe, so coastlines stay sharp, and islands like Taiwan, Japan, Hainan and Sri Lanka stay separate from the mainland. When a duty flies out and back on the same route (like DMK › CNX › DMK), it's drawn as one line, and the moving dots run out to CNX and back. Drag to turn it. Pinch or spread two fingers to zoom (up to 6×). On a computer, pinch the trackpad, use Ctrl + scroll, or the − and + buttons. Double-tap or tap the zoom level to reset.
- **To-do, Shopping and Notes.**

**Duty tools** (Max FDP and Wake-up are on the board at first)
- **Max FDP:** enter a report time and number of sectors. It shows the Table 2 limit, or the extension table limit, plus the latest on-blocks and off-duty time. **Use next duty** fills these in from your roster and shows how much spare you have.
  - Assumes acclimatised crew. Table 3 is not included.
- **Wake-up planner:** works from your next report. It shows when to go to bed, when to set the alarm and when to leave home, based on your travel time, get-ready time and sleep hours.
- **Layovers:** each night-stop in the next 14 days, with fields for hotel, room and pickup time (local), and a countdown to pickup.
- **Documents:** passport, licence, medical, recurrent training and visa expiry dates. Each shows as valid, due soon (90 days), renew now (30 days) or expired.

**On board**
- **PA helper:** writes the welcome announcement for a sector on your roster. It fills in the flight number, cities, flight time, local arrival time and temperature in °C and °F. You can change the wording, and there's a Copy button.
- **Phonetic speller:** spells names, booking references and seats in the ICAO alphabet (Tree, Fower, Fife, Niner).
- **Unit converter:** °C/°F, kg/lb, m/ft, cm/in, km/nm/mi, L/gal, ml/fl oz, km/h/kt/mph.

**Travel & time** (add from Edit layout → Add widgets)
- **World clock:** UTC, your roster layovers, and any airport you add. Tap + (top right), type an airport code or a city name (any airport in the world, picked from the suggestions), and tap ✓. Tap the pencil to edit: every row, including UTC and roster cities, gets a pencil to change its code and a bin to remove it. Hidden cities can be brought back from the same edit view. Tap ✓ when done.
- **Time converter:** pick a date, time and zone. It shows UTC, BKK, your layovers and your world clock cities.
- **Currency:** live rates, saved for offline use.
- **Expenses:** log layover spending in any currency. The month's total is converted to THB.
- **Sunrise & sunset:** for DMK and your next destinations.

**Everyday** (add from Edit layout → Add widgets)
- **Year countdown** (on the board at first): live countdown to New Year. Switch between two styles in the widget corner:
  - **Dots:** the whole year as 365 dots. Days gone are filled, today pulses, roster leave shows as rings, and countdown dates are marked.
  - **Countdown:** split-flap days, hours, minutes and seconds, with a month strip.
- **Countdown:** annual leave on your roster shows up automatically.
- **Crew bag check:** a reusable packing list.
- **Nap timer.**
- **Quick links.**
- **Water:** daily glasses against a goal. It resets each day. Tap the circle around the count to add one glass (250 ml), and the widget shows how much you've had against the goal. Tapped it by mistake? Tap the last filled dot to take one back. The count starts again at midnight (Bangkok time). Reaching the goal sets off dot fireworks. To change the goal, tap the flag (top right), step the number of glasses with − and +, and tap ✓.

## Change the layout
1. Tap the **four-squares** icon (top right).
2. Change what you like:
   - **Move a widget:** drag the six-dot handle at its top left. This works with a finger or a mouse, and the page scrolls when you reach the edge.
   - **Resize a widget:** drag the dots in its bottom-right corner. Left and right changes how many columns it covers, and up and down changes its height. The content fits the new size as you drag. Clocks and displays grow bigger, the calendar, globe and notes stretch to fill, and anything too big shrinks to fit. Double-tap the corner, or use **Auto height**, to let it size itself again.
   - **Pin** keeps a widget at the top. Dropping a widget above a pinned one pins it too.
   - **↑ ↓** move a widget one step at a time.
   - **Remove** takes a widget off the board. Put it back from **Add widgets**.
   - **Reset layout** returns to the start.
3. Tap the **tick** to finish.

The layout is saved on each device.

## Screens
The board picks how many columns to use from the screen width:

| Screen | Columns |
| --- | --- |
| iPhone, or the foldable iPhone when folded | 1 |
| Foldable iPhone when unfolded, or a tablet | 2 |
| Laptop | 3 |
| Big desktop | 4 |

Each widget scales its text to its own width.

## Duty alert on the LED ticker
The ticker turns into a caution light before your next report:

- **Yellow caution:** from **2 h 30 min** before report. The ticker blinks solid yellow on and off every 2 seconds, with hazard-tape stripes, and the badge counts down: "REPORT IN 2H 10M".
- **Red:** from **35 min** before report. It blinks red about once a second, and the badge shows "GO · 34 MIN".

At report time the alert stops.

The alert flashes on every motion level, Calm included. Only turning on Reduce Motion in your phone's accessibility settings stops the blinking. Then the colours stay on without flashing.

To change the times, search `index.html` for `ALERT_YELLOW = 150, ALERT_RED = 35`. The numbers are minutes before report.

## Icons
Every button is a round icon. Hover with a mouse to see its name. The top bar, left to right:

| Icon | What it does |
| --- | --- |
| Sun or moon | Switches between light and dark theme |
| Bolt, wave or flat line | Motion level: Max, Full or Calm |
| Arrow into tray | Back up data |
| Arrow out of tray | Restore from backup |
| Four squares | Edit layout (shows a tick while editing) |

Icons, checkboxes and text boxes keep the same tap size when you resize a widget. Only the content scales.

Buttons that wipe something (clear roster, reset layout) turn solid with a ⚠ on the first tap. Tap again within 4 seconds to confirm.

## Motion
There are three levels, under the motion icon in the top bar: **Full** (the default), **Max** and **Calm**. If your phone has Reduce Motion turned on, Axiom starts on Calm until you pick a level yourself.

**Boot-up (Full and Max)**
- **Splash:** dots fly in from all sides, spell **AXIOM** and "CREW DASHBOARD", then burst away. Tap it to skip.
- **Board settles:** widgets rise in one after another, every heading and number shuffles like a split-flap departures board, and duty-hour bars light up dot by dot.

**While you use it (Full)**
- **LED ticker** across the top. Hover or tap it to pause.
- **Clock:** changed digits pop in, and the colon blinks.
- **Weather icons:** rain drips, rays shimmer, and lightning flickers.
- **Globe:** a red route line with running dots and a radar ping.
- **Edit layout:** widgets jiggle.
- **Small touches:** calendar cells wave in when you change month, and a ticked box pops.

**Max adds**
- A rippling dot background that reacts to taps.
- 3D tilt with a light that follows the mouse.
- A plane and stars on the globe.
- Rain and lightning behind the weather.
- Page flips.
- Shuffling on every value that changes.

**Calm** turns everything off, including the boot-up.

## Dot lettering
The big numbers and headings are drawn as real round dots by the app itself, not with a font. So they look the same on every iPhone, Android phone or computer, even where web fonts are blocked (Lockdown Mode, file previews, some in-app browsers).

## Use it
- **Straight from the file:** open `index.html` in Safari, Chrome or Edge.
- **As an app on iPhone:**
  1. Upload this folder to GitHub Pages, the same way as SL Swap Check.
  2. Open the link in Safari, then tap **Share → Add to Home Screen**.
  3. After the first visit it opens with no signal.
- **After you upload a new `index.html`:** bump `CACHE_VERSION` in `sw.js` (for example `axiom-v1` → `axiom-v2`).

## Theme
the sun/moon icon in the top bar switches between Light and Dark. The first time, it follows your phone's setting. After that it stays on what you picked.

## Data
Axiom was called Crew Dotboard before. Data saved under the old name carries over, and old backups still restore.

Everything stays on the device. To move it between your phone and computer, use the **download** icon in the top bar, then the **upload** icon on the other device.

On iPhone, the Home Screen app keeps its own data, separate from Safari. Use Back up and Restore if you switch between them.

Countdowns read the eCrew times as Bangkok time. Weather comes from Open-Meteo, which is free and needs no key.

pdf.js © Mozilla (Apache 2.0). The land map and Thailand's shape come from Natural Earth (public domain). The Geist and Geist Mono fonts are under the SIL Open Font License.


Airport list: airportsdata (MIT licence) and OurAirports (public domain).


## Full screen
- **iPhone:** add Axiom to your Home Screen (Share, then Add to Home Screen) and open it from there. It runs full screen with no browser bars. iPhone doesn't allow full screen for pages in Safari.
- **Desktop, Android and iPad:** tap the full-screen button in the top bar. Press Esc or tap it again to leave.
- There's no scroll bar on any device; scroll with your finger, trackpad, mouse wheel or arrow keys.
