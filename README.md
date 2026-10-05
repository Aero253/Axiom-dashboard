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
- **Selected day:** your sectors, report and off-duty times, and your own plans for that day.
- **Next 7 days:** your roster for the coming week. Tap a day to open it.
- **Duty hours:** duty hours over the last 7, 14 and 28 days, and flight hours over 28 days, against the chapter 7 limits used in SL Swap Check. It also shows the rest you'll have before your next report. This is unofficial.
- **Weather:** live when online, for DMK and your next 7 days of destinations. Offline it keeps the last forecast.
- **Globe:** drag to turn it. Pinch or spread two fingers to zoom (up to 6×). On a computer, pinch the trackpad, use Ctrl + scroll, or the − and + buttons. Double-tap or tap the zoom level to reset.
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
- **World clock:** UTC, your roster layovers, and any airport you add.
- **Time converter:** pick a date, time and zone. It shows UTC, BKK, your layovers and your world clock cities.
- **Currency:** live rates, saved for offline use.
- **Expenses:** log layover spending in any currency. The month's total is converted to THB.
- **Sunrise & sunset:** for DMK and your next destinations.

**Everyday** (add from Edit layout → Add widgets)
- **Countdown:** annual leave on your roster shows up automatically.
- **Crew bag check:** a reusable packing list.
- **Nap timer.**
- **Quick links.**
- **Water:** daily glasses against a goal. It resets each day.

## Change the layout
1. Tap **Edit layout**.
2. Change what you like:
   - **Move a widget:** drag the six-dot handle at its top left. This works with a finger or a mouse, and the page scrolls when you reach the edge.
   - **Resize a widget:** drag the dots in its bottom-right corner. Left and right changes how many columns it covers, and up and down changes its height. The content fits the new size as you drag. Clocks and displays grow bigger, the calendar, globe and notes stretch to fill, and anything too big shrinks to fit. Double-tap the corner, or use **Auto height**, to let it size itself again.
   - **Pin** keeps a widget at the top. Dropping a widget above a pinned one pins it too.
   - **↑ ↓** move a widget one step at a time.
   - **Remove** takes a widget off the board. Put it back from **Add widgets**.
   - **Reset layout** returns to the start.
3. Tap **Done**.

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

## Use it
- **Straight from the file:** open `index.html` in Safari, Chrome or Edge.
- **As an app on iPhone:**
  1. Upload this folder to GitHub Pages, the same way as SL Swap Check.
  2. Open the link in Safari, then tap **Share → Add to Home Screen**.
  3. After the first visit it opens with no signal.
- **After you upload a new `index.html`:** bump `CACHE_VERSION` in `sw.js` (for example `axiom-v1` → `axiom-v2`).

## Data
Axiom was called Crew Dotboard before. Data saved under the old name carries over, and old backups still restore.

Everything stays on the device. To move it between your phone and computer, use **⋯ → Back up data**, then **⋯ → Restore from backup** on the other device.

On iPhone, the Home Screen app keeps its own data, separate from Safari. Use Back up and Restore if you switch between them.

Countdowns read the eCrew times as Bangkok time. Weather comes from Open-Meteo, which is free and needs no key.

pdf.js © Mozilla (Apache 2.0). The Doto, Geist and Geist Mono fonts are under the SIL Open Font License.
