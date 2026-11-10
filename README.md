# Bedtime Bridge shortcuts

Ready-made shortcuts for the Bedtime Bridge iPhone app. The app sends itself a notification with a
command word (for example `RUN_BEDTIME`), and a Shortcuts automation that watches for that word
runs the matching shortcut. Each shortcut tells the app when it started and when it finished.

## Which folder

- **Bedtime Bridge**: for the App Store app.
- **Bedtime Bridge Beta**: for the TestFlight beta.

A shortcut only works with the app it was made for, so take them from the folder that matches
yours.

## Adding one

1. Tap the `.shortcut` file, then **Add Shortcut**. Wind Down On and Off ask which Focus is your
   wind-down Focus.
2. Read the note at the top of the shortcut and set up its automation once: Shortcuts →
   **Automation** → **+** → **Notification** → App: Bedtime Bridge (or Bedtime Bridge Beta) →
   Message contains: the word below → **Run Immediately**, **Notify When Run** off → Next →
   **Run Shortcut** → the shortcut.
3. Add your own steps where the shortcut says so (lights, music, a thermostat).

| Shortcut | Message contains | What it does |
|---|---|---|
| Bedtime | `RUN_BEDTIME` | Sets tonight's alarms (offers to pick a time if nothing is found), turns on Sleep Focus, says tomorrow's plan |
| Good Morning | `RUN_GOOD_MORNING` | Turns off Sleep Focus and says the morning's plan |
| Back To Bed | `RUN_BACK_TO_BED` | Your steps for going back to bed |
| Nap Start | `RUN_NAP_START` | Turns on Sleep Focus |
| Nap End | `RUN_NAP_END` | Turns off Sleep Focus |
| Wind Down On | `RUN_WIND_DOWN` | Turns on your wind-down Focus and says how long until bed |
| Wind Down Off | `RUN_CANCEL_WIND_DOWN` | Turns off your wind-down Focus |
| Preview Tomorrow | `RUN_PLAN_PREVIEW` | Shows tomorrow's plan without setting alarms |
| Morning Update | `RUN_MORNING_UPDATE` | Checks the drive and updates the leave-by reminder |
| Disarm | `RUN_DISARM` | Your steps for turning off a home alarm |
| Arm Stay | `RUN_ARM_STAY` | Your steps for setting a home alarm for the night |
| Backstop Early, Deadline, Late | `RUN_BACKSTOP_EARLY`, `RUN_BACKSTOP_DEADLINE`, `RUN_BACKSTOP_LATE` | Says the backstop out loud, then your steps for when you're not up yet (lights on, a speaker) |
| Set Tomorrow's Alarms | *(none: a Time of Day automation, e.g. 22:00 daily)* | Sets tomorrow's alarms at that time unless you already set them or chose no alarms (Apple Home or phone-only setups; needs app 0.5.1) |
| Leave Check | `RUN_LEAVE_CHECK` | Checks the drive and reminds you when to leave |

Set Tomorrow's Alarms is set up differently: Automation → **Time of Day** → your time → Daily →
**Run Immediately** → Run Shortcut → Set Tomorrow's Alarms.

Bedtime also works on its own, or from a charger, Sleep Focus or bed-sensor automation.

Signed so anyone can import them.
