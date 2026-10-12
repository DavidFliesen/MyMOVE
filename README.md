# MyMOVE! — v1.2.0

**A pocket companion for Veterans in the VA MOVE! Weight Management Program.**

MyMOVE! turns the *MOVE! Veteran Workbook (2023)* into simple weekly steps you can track on your phone: learn the module, set two SMART goals, log every day, check in, repeat. It's built to help you stick with the program, not replace it.

> **Disclaimer:** MyMOVE! is an independent companion app. It is not made, endorsed, or reviewed by the U.S. Department of Veterans Affairs and does not give medical advice. Your MOVE! care team and your doctor come first. Talk with them before changing how you eat or how active you are.

---

## Features

### Already enrolled? Pick up where you are
MyMOVE! works whether you're starting MOVE! today or are already weeks in.

- **At setup**, choose **Already enrolled**. Enter your current week (for example, week 7) or your program start date; whichever you enter, the other fills in automatically.
- **Enter your starting weight** from when you began MOVE!, and optionally your weight today. Setup shows your progress so far: pounds and percent lost, and your weekly average.
- **Earlier modules** can be marked complete automatically. You can still open and review every one of them.
- **Past weigh-ins** from your MOVE! visits can be added in **Progress → Weigh-in history**, so the weight chart shows your whole journey.
- **Past weekly check-ins** can be filled in by picking the week in the check-in form.
- **Past days' food and activity** can be logged using the back arrow on the Log tab.
- **Already set up as new?** Go to **More → Edit my plan, week & start date** and switch to *Already enrolled*. A prompt on the Today screen does the same.

### Plan setup
- Enter your current weight and pick a goal of 5%, 7%, 8% or 10%.
- Pick a pace from ½ to 2 lb per week.
- The app shows your goal weight and an estimated target date.
- Your daily calorie target uses the MOVE! ranges (1,200–1,500 for women, 1,500–1,800 for men) and never goes below 1,200. If your care team gave you a number, enter that instead.
- It also includes the readiness and confidence scales and "My reasons to MOVE!", based on the workbook's decisional balance exercise.

### Today
The Today screen shows:
- This week's module.
- Calories in, calories out and calories left.
- Weekly active minutes against the target: 150, rising to 300 from Week 9.
- Strength days, which count toward the 2-day target.
- Water against 9+ cups.

It also lets you:
- Track your two SMART goals by tapping each day you hit them.
- See weigh-in reminders and weekly check-in prompts.
- Read a tip of the day.
- Open quick craving and stress tools.

### Log
- **Food log:** time, amount, calories, meal and mood, matching the workbook's Food and Activity Log. Recent items can be re-added in one tap.
- **Activity log:** minutes, type and effort on the RPE scale. Only effort of 4 or higher counts toward weekly minutes, and vigorous minutes count double.
- **Water and weight**, for any past day.

### Program
- **MOVE! Veteran Workbook link:** the official workbook PDF is linked as the app's companion in the Program tab, the More tab, and every module. Each module shows the workbook pages where its lesson appears.
- Each module is labeled by week. **You're here** marks your current week and **Review** marks earlier ones.
- **Go to my week** jumps straight to your current module. Inside a module, use **‹ Week / My week / Week ›** to move between weeks.
- A **Mark weeks complete** button catches up earlier modules in one tap.
- All 16 modules plus 3 mini-modules: Weight and Sleep, Quit Tobacco, and Be Involved in Your Health Care.
- Each module has plain-language key points and a "Bring it home this week" checklist.
- Each module links to the tools it uses.
- One module is suggested per program week. You can open any module at any time to match your MOVE! group.

### Toolbox (26 tools)

| Area | Tools |
|---|---|
| Goals | Weight Loss by the Numbers, SMART Goal Builder, My Reasons, My Rewards, Weekly Check-In (any week), My Weigh-In History |
| Eating | Rethink Your Drink, Healthy Food Swaps, Rate My Plate, Size It Up! Portion Guide, Food Label Check, Meal Plan & Shopping List, Safe Cooking Temps, Dining Out Checklist |
| Activity | Calories Burned in 10 Minutes, Target Heart Rate, Effort Scale (RPE), Step Goal Builder |
| Mind & behavior | Rethink a Thought (4 steps), My Eating Triggers, Craving Timer (15 min), Calm Breathing, Stress Tracker, 5-Step Problem Solver, My Slip Plan |
| Maintenance | My Toolkit Review, Questions for My Care Team |

### Progress
- Weight trend chart with a goal-weight line.
- 5%, 8% and 10% milestones.
- Weekly active-minute bars with reference lines at 150 and 300.
- Logging streak, check-in history and your chosen rewards.

### More
- VA MOVE! Get Started steps and links.
- Veterans Crisis Line: dial **988 then press 1**, or text **838255**.
- Back up and restore your data.
- Share a progress summary with your MOVE! team.

---

## Privacy

All data is stored **only on your device**, in the browser's local storage. Nothing is sent to any server, and there are no accounts, trackers or APIs.

Clearing your browser data erases the app's data. Use **More → Back up** regularly, especially before changing phones.

---

## Install

**On a phone:** open the app's URL in Safari (iPhone) or Chrome (Android). Then choose one of these:
- iPhone: **Share → Add to Home Screen**.
- Android: **Install app**.

After the first visit, the app works fully offline.

**Hosting (GitHub Pages):**
1. Upload the files below to the root of the repository.
2. In the repository, go to **Settings → Pages**, select the main branch and **/ (root)**, and save.

```
index.html          App (HTML, CSS and JavaScript in one file)
manifest.json       PWA manifest
sw.js               Service worker (offline cache)
README.md           This file
icons/
  icon-192.png
  icon-512.png
  icon-maskable-512.png
  apple-touch-icon.png
```

---

## Technical notes

- **Code style:** a single-file app written in ES5-only JavaScript. It uses no template literals, arrow functions, `let` or `const`, and no CSS custom properties; all colors are hardcoded hex values.
- **Dependencies:** none. There are no frameworks, no build step and no external requests.
- **Saved data:** stored under the local storage key `mymove.v1`.
- **Service worker:** the app page is network-first, so updates arrive when online, and falls back to the cache offline. Icons and the manifest are cache-first.
- **Releasing an update:** bump `VERSION` in `index.html`, `CACHE` in `sw.js`, and the version at the top of this README.

---

## Sources

Program content is adapted and summarized from:
- [MOVE! Veteran Workbook (2023)](https://www.move.va.gov/docs/veteranworkbook/MoveVetWorkBook-2023.pdf)
- [move.va.gov](https://www.move.va.gov) and its [Get Started](https://www.move.va.gov/MOVE/GetStarted.asp) page

---

## Version history

| Version | Date | Notes |
|---|---|---|
| 1.2.0 | 2026-10-12 | MOVE! Veteran Workbook (PDF) linked as companion in Program, More and every module, with each module's workbook page range. |
| 1.1.0 | 2026-10-12 | Support for Veterans already enrolled: start at any week, set program start date and starting weight, auto-complete earlier modules, Weigh-In History for past weigh-ins, check-ins for past weeks, week labels and review navigation in Program, start date and weekly average on Progress. |
| 1.0.0 | 2026-10-12 | First release: plan setup, Today dashboard, food, activity, water and weight logs, 16 modules + 3 mini-modules, 25 tools, weekly check-in, progress charts, offline PWA, backup and restore. |

---

Built by ARTEZIQ.
