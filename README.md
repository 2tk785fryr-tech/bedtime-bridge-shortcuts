# Bedtime Bridge shortcuts

> 🌐 **[See the website](https://2tk785fryr-tech.github.io/bedtime-bridge-shortcuts/)**

**Up on time, every time.**

Ready-made shortcuts for the Bedtime Bridge iPhone app. They let your alarms get set at bedtime
without opening the app, and let your bedtime and morning do more at the same time: lights,
scenes, music, a Focus.

### Which app do you have?

| | |
|---|---|
| **Bedtime Bridge** (App Store) | Use the links in the **App Store** column below |
| **Bedtime Bridge Beta** (TestFlight) | Use the links in the **Beta** column below |

A shortcut only works with the app it was made for.

---

## Start here: which ones do you need?

It depends on how you chose to have your alarms set (the app asks during setup, and it's in
**Settings → How alarms get set**):

| You chose | Shortcuts you need |
|---|---|
| **A Focus filter** (Sleep Focus) | **None.** Everything below is optional extras. |
| **A shortcut** | **One** of: [Set Tomorrow's Alarms](#set-tomorrows-alarms) (at a set time), or [Bedtime](#bedtime) from a Sleep Focus or charger automation |
| **Myself, from the app** | None. Open the app before bed; it also sets the next 2 mornings. |
| **Home Assistant sets them** | None for alarms. Home Assistant runs the rest through its own automations. |

Not sure? Start with **Set Tomorrow's Alarms**. It's the simplest: one automation at a time you
pick, every day.

---

## How these shortcuts work (30 seconds)

There are two kinds:

1. **Run at a time you choose.** [Set Tomorrow's Alarms](#set-tomorrows-alarms) runs from a
   Time of Day automation, for example 10 PM every day.
2. **Run when the app asks.** The app sends itself a quiet notification with a command word (for
   example `RUN_BEDTIME`). A Shortcuts automation watching for that word runs the matching
   shortcut. You set the automation up once; after that it runs on its own.

Every shortcut tells the app when it started and finished, so the app can show a tick and you can
see it in **Settings → The app → History**.

---

## Setting one up, step by step

Do this once per shortcut. It takes about two minutes.

### 1. Add the shortcut

Tap the shortcut's link below (on your iPhone). Shortcuts opens; tap **Add Shortcut**.

> 📷 *Screenshot: the Add Shortcut screen*

Wind Down On and Off ask which Focus is your wind-down Focus while you add them.

### 2. Read the note at the top

Each shortcut starts with a short note: what it does, which word it watches for, and where you
can add your own steps.

> 📷 *Screenshot: the note at the top of a shortcut*

### 3. Make its automation

1. Open **Shortcuts → Automation** (bottom of the screen) → **+** (top right).
2. Choose **Notification**.
3. **App:** Bedtime Bridge (or Bedtime Bridge Beta).
4. **Message contains:** the command word from the table below, exactly as written, for example
   `RUN_BEDTIME`.
5. Choose **Run Immediately**, and turn **Notify When Run** off.
6. Tap **Next** → **Run Shortcut** → pick the shortcut → **Done**.

> 📷 *Screenshot: Notification trigger with App and Message contains filled in*
>
> 📷 *Screenshot: Run Immediately selected, Notify When Run off*
>
> 📷 *Screenshot: Run Shortcut with the shortcut picked*

### 4. Test it

In the app, open the shortcut's card (**Settings → How alarms get set**, or the setup page) and
tap **Test it**. The card shows a tick when the app sees the shortcut ran.

> 📷 *Screenshot: a card with its tick*

### 5. Add your own steps (optional)

Each shortcut has a spot marked **Your steps go here**. Add any Shortcuts action: lights, a Home
scene, music, a thermostat, a podcast. The suggestions under each shortcut below are a start.

---

## The shortcuts

### Set Tomorrow's Alarms

Sets tomorrow's alarms at a time you choose, unless you already set them or chose no alarms.
**This is the one to use if you picked "A shortcut" during setup.** (Apple Home and phone-only
setups.)

| App Store | Beta |
|---|---|
| [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Set%20Tomorrow's%20Alarms.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Set%20Tomorrow's%20Alarms.shortcut) |

**Set up differently:** Automation → **+** → **Time of Day** → your time (a bit before your
earliest bedtime, e.g. 10 PM) → **Daily** → **Run Immediately** → Next → Run Shortcut → Set
Tomorrow's Alarms.

> 📷 *Screenshot: Time of Day automation set to Daily*

**Tip:** pick a time you're always home and awake for. If you go to bed at different times, a
Sleep Focus automation with [Bedtime](#bedtime) follows you instead.

### Bedtime

Watches for `RUN_BEDTIME`. Sets tonight's alarms (offers to pick a time if nothing is found),
turns on Sleep Focus and says tomorrow's plan.

| App Store | Beta |
|---|---|
| [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Bedtime.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Bedtime.shortcut) |

Also works from its own automation: **When Sleep Focus turns on**, **When I connect to power**
(the charger, at night), or a bed sensor.

**Suggestions for your steps:** bedroom lights to 10%, then off; lock the door; a white-noise
playlist; thermostat to its night setting.

### Good Morning

Watches for `RUN_GOOD_MORNING`. Turns off Sleep Focus and says the morning's plan.

| App Store | Beta |
|---|---|
| [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Good%20Morning.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Good%20Morning.shortcut) |

**Suggestions:** open the curtains; lights on; start the coffee maker plug; the news or a podcast
on a speaker; the weather.

### Back To Bed

Watches for `RUN_BACK_TO_BED`. Your steps for going back to bed (on a day off, or after an early
alarm you don't need).

| App Store | Beta |
|---|---|
| [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Back%20To%20Bed.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Back%20To%20Bed.shortcut) |

**Suggestions:** lights off again; close the curtains; Sleep Focus back on.

### Nap Start and Nap End

Watch for `RUN_NAP_START` and `RUN_NAP_END`. Turn Sleep Focus on and off for a nap.

| | App Store | Beta |
|---|---|---|
| Nap Start | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Nap%20Start.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Nap%20Start.shortcut) |
| Nap End | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Nap%20End.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Nap%20End.shortcut) |

**Suggestions:** dim the room; close the blinds; a nap playlist with a timer.

### Wind Down On and Wind Down Off

Watch for `RUN_WIND_DOWN` and `RUN_CANCEL_WIND_DOWN`. Turn your wind-down Focus on (and say how
long until bed) and off. They ask which Focus is your wind-down Focus when you add them.

| | App Store | Beta |
|---|---|---|
| Wind Down On | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Wind%20Down%20On.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Wind%20Down%20On.shortcut) |
| Wind Down Off | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Wind%20Down%20Off.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Wind%20Down%20Off.shortcut) |

**Suggestions:** warm, dim lights; screens to grayscale; a reading lamp; quiet music.

### Preview Tomorrow

Watches for `RUN_PLAN_PREVIEW`. Shows tomorrow's plan without setting any alarms (the evening
preview).

| App Store | Beta |
|---|---|
| [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Preview%20Tomorrow.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Preview%20Tomorrow.shortcut) |

### Morning Update and Leave Check

Watch for `RUN_MORNING_UPDATE` and `RUN_LEAVE_CHECK`. Check the drive and update the leave-by
reminder; Leave Check also reminds you when to leave.

| | App Store | Beta |
|---|---|---|
| Morning Update | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Morning%20Update.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Morning%20Update.shortcut) |
| Leave Check | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Leave%20Check.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Leave%20Check.shortcut) |

**Suggestions:** start the car (if your car's app has a shortcut); turn on the porch light.

### Disarm and Arm Stay

Watch for `RUN_DISARM` and `RUN_ARM_STAY`. Empty on purpose: your steps for turning a home alarm
off in the morning and setting it for the night.

| | App Store | Beta |
|---|---|---|
| Disarm | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Disarm.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Disarm.shortcut) |
| Arm Stay | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Arm%20Stay.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Arm%20Stay.shortcut) |

### Backstop Early, Deadline and Late

Watch for `RUN_BACKSTOP_EARLY`, `RUN_BACKSTOP_DEADLINE` and `RUN_BACKSTOP_LATE`. If you're not up
yet, they say the backstop out loud, then run your steps. Each one is louder than the last.

| | App Store | Beta |
|---|---|---|
| Early | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Backstop%20Early.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Backstop%20Early.shortcut) |
| Deadline | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Backstop%20Deadline.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Backstop%20Deadline.shortcut) |
| Late | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge/Backstop%20Late.shortcut) | [Get it](https://github.com/2tk785fryr-tech/bedtime-bridge-shortcuts/raw/main/Bedtime%20Bridge%20Beta/Backstop%20Late.shortcut) |

**Suggestions:** Early: bedside lamp on slowly. Deadline: all bedroom lights on full, a speaker
announcement. Late: everything, plus a call or message to someone you trust.

---

## Good to know

- **More than one is fine.** Every run re-checks your plan; it never sets a second set of alarms.
- **Each works only with its own app** (App Store or Beta). If you switch, add the other column's
  version.
- **If one doesn't run:**
  - Check **Notify When Run** is off and **Run Immediately** is on (otherwise iOS asks first).
  - Check **Message contains** matches the word exactly, capitals included.
  - Low Power Mode and Focus modes don't stop automations, but turning off the app's
    notifications does: **Settings → Notifications → Bedtime Bridge → Allow Notifications** on.
  - In the app, **Settings → The app → History** shows whether the command was sent and whether
    the shortcut reported back.
- **The app never opens Shortcuts by itself.** It only does when you tap a button like Get it or
  Test it.
- The shortcuts are signed so anyone can add them.

---

Questions or ideas: open an issue in this repo.
