# BITS Helper

**Bomber Information Technology Services · Mountain Home High School**

BITS Helper is a one-page daily dashboard for Mr. Bergenstock's school day. Open it in the morning and you see what kind of day it is, where you need to be, what's coming up and who to call. It's a single HTML file with no install, no server and no build step, and it works on a phone or a computer.

---

## What it does

### Today at a glance
- **Day type badge:** A Day, B Day, Fast Friday, 1:00 Dismissal, Finals or No School. It knows the 2026-27 bell rules: Mon/Wed are A days, Tue/Thu are B days, Friday is Fast Friday unless it's a full-block Friday.
- **Live "Now" box:** shows the period you're in, how many minutes are left and what's next. It runs on Mountain Home (Central) time on any device.
- **Heads-up alerts** for unusual days that are coming (early dismissals, pep rallies, finals).
- **Prev / Today / Next** buttons to look at any day of the year.

### Bell schedule built around my classes
- Each period shows its course and Canvas course banner:
  - 2nd, 3rd, 8th: Intro to Computer Science (Processing)
  - 4th: Game Dev & Design
  - 5th, 7th: AP Computer Science A
  - 1st, 6th: Planning
- **Duties are added automatically** from the duty list (for example, Wednesday PM bus loading and Friday lunch duty in the pavilion).
- **Period notes:** click any period to open a notes box right under it. Jot down where the class stopped, and the note is there the next time you click that period.

### School calendar
- Today's events and the next 14 days, from the MHHSCA 2026-27 calendar.

### Look It Up
Buttons under the calendar that each open a search box and a scrolling list:

| Button | What's in it |
|---|---|
| 📞 Phone Extensions | 2026-27 extension sheet, plus each person's job and department |
| 🗓️ Master Schedule | Every teacher's A/B day schedule. Prep periods are highlighted, and a "Who has PREP during…" filter helps find coverage |
| 🦺 Duty List | AM, PM, D-hall and lunch duties by day |
| 🍽️ Staff Lunches | 1st and 2nd lunch lists |
| 📅 School Calendar | The full 2026-27 year, with past dates faded |
| 🚌 Bus Loading | Loading grid by bus number (search any bus) plus the PM bus duty roster |
| 🗺️ School Map & Evacuation | Interactive campus map (see below) |
| 🏢 Who to Call (District) | Central office contacts by department |

### Interactive school map
- The full campus map, labeled with teachers by room, fit to the screen, with zoom in/out and a **Whole map** button.
- **Search any teacher, office or room number** to drop a pin on the map.
- **Each building is a clickable zone** that opens its evacuation map, with fire routes and tornado locations: Big Top, 100's, 200's/Dunbar, ACME/Agri and CBI.

---

## How it's built

- One self-contained `index.html` with plain HTML, CSS and JavaScript. No frameworks.
- All schedules, lists and map images are embedded in the file, so it works offline once loaded.
- Fonts come from Google Fonts (Russo One and Inter).
- Theme: BITS royal blue and Bomber gold, with a circuit-board header.
- Notes save in the browser on the device you're using (`localStorage`). In the private Claude-hosted version, notes sync across devices.

## Updating it

The data lives in clearly named blocks inside the script:

| Block | Holds |
|---|---|
| `COURSE` | Period → course name and banner |
| `SPECIAL` | Special-schedule days (early dismissals, finals, full-block Fridays, no-school days) |
| `EV` | Calendar events |
| `DIR` | Phone extensions |
| `LOOK` | Master schedule, duty list, lunches |
| `MAPD` | Map images, building zones and room pins |

Edit the block, save, and reload the page.

## Use on a phone

Open the page in Safari or Chrome and choose **Add to Home Screen**. It opens like an app.

---

*Built for the 2026-27 school year at Mountain Home High School, Mountain Home, Arkansas. Go Bombers!*
