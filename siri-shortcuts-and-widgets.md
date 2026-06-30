# Golf Stats — Siri, Shortcuts, Widgets & Watch Faces

Golf Stats adds a set of **optional, hands-free** ways to score and glance at your
round without digging through the app — built entirely on Apple's own frameworks:

- **Siri** voice commands ("Score this hole in Golf Stats").
- **Shortcuts** you can build and chain in the Shortcuts app.
- The **Action Button** on iPhone 15 Pro and later.
- **Control Center** and **Lock Screen** controls.
- **Home Screen** and **Lock Screen** widgets.
- **Apple Watch** Siri commands, complications, and watch-face shortcuts.

There is **nothing to switch on inside Golf Stats** — these are configured in
iOS, watchOS, and the Shortcuts app. This guide walks through setting each one
up. (Because they're standard Apple screens, this page has no app screenshots —
the steps below describe exactly what you'll see in **Settings**, **Control
Center**, the **Shortcuts** app, and the **Watch** app.)

> **A round must be open or connected.** The scoring actions act on the round
> you currently have on screen in the app (iPhone) or the round **connected to
> your Apple Watch**. Open a tournament and a round so a hole is showing first.
> If nothing is open, the action politely replies *"Open a round in Golf Stats
> first."* rather than guessing.

---

## Contents

- [The five scoring actions](#the-five-scoring-actions)
- [Siri](#siri)
- [The Shortcuts app](#the-shortcuts-app)
- [The Action Button (iPhone 15 Pro and later)](#the-action-button-iphone-15-pro-and-later)
- [Control Center & Lock Screen controls](#control-center--lock-screen-controls)
- [Home Screen & Lock Screen widgets](#home-screen--lock-screen-widgets)
- [Apple Watch — Siri & the Action Button](#apple-watch--siri--the-action-button)
- [Apple Watch — complications on a watch face](#apple-watch--complications-on-a-watch-face)
- [Apple Watch — running an action from your watch face (Run Shortcut)](#apple-watch--running-an-action-from-your-watch-face-run-shortcut)
- [Permissions & requirements](#permissions--requirements)

---

## The five scoring actions

The same five actions are available to Siri, the Shortcuts app, the Action
Button, Control Center, and the Apple Watch:

| Action | What it does |
| --- | --- |
| **Score This Hole** | Works out the hole's score from the shots you've tracked (the same calculation as the shot map's **Auto Score**), saves it, and moves to the next hole. |
| **Go to Hole** | Jumps the round on screen to a hole number you choose. |
| **Tag a Shot** | Drops a GPS shot pin at your current location. Optionally records the **club**, **lie**, and **stance slope** — or leave them blank. |
| **Set the Flag** | Places (or moves) the hole's green/flag pin at your current location. |
| **Set Score** | Records a hole's **score** and/or **putts** by number — no GPS, handy for entering a score by voice or in a shortcut. |

**Tag a Shot** and **Set the Flag** need your location (When-In-Use) — they
capture a single GPS fix the moment you run them, exactly like the **Tag Shot**
and **Set Flag** buttons on the in-app shot map. If location is off or no fix
arrives, the action tells you instead of dropping a bad pin.

---

## Siri

Nothing to set up — just talk to Siri. Try any of these (Siri also accepts the
variations listed):

- *"Score this hole in Golf Stats"* — also: "Score my hole…", "Log this hole…",
  "Record this hole…"
- *"Go to a hole in Golf Stats"* — Siri then asks **which hole**.
- *"Tag a shot in Golf Stats"* — also: "Mark a shot…", "Drop a shot…", "Pin a
  shot…", "Log a shot…"
- *"Set the flag in Golf Stats"* — also: "Set the pin…", "Mark the flag…", "Move
  the pin…"
- *"Set my score in Golf Stats"* — also: "Record my score…", "Log my score…"

Golf Stats uses Apple's **App Intents** framework only — there's no Siri sign-in,
no special permission, and the actions send nothing to any server. The voice
phrases are translated, so they work in your device's language too.

> Siri voice control needs a real iPhone or Apple Watch (it can't be exercised in
> the Simulator).

---

## The Shortcuts app

Every action is also a building block in the **Shortcuts** app, so you can wire
them into your own automations (for example, a single shortcut that tags a shot
*and* speaks the distance).

1. Open the **Shortcuts** app.
2. Tap **+** to create a new shortcut (or edit an existing one).
3. Tap **Add Action** and search for **Golf Stats** — the five actions appear:
   **Score This Hole**, **Go to Hole**, **Tag a Shot**, **Set the Flag**, and
   **Set Score**.
4. Pick one and fill in any optional fields (e.g. Tag a Shot's **Club**, **Lie**,
   and **Slope**; Set Score's **Hole**, **Score**, and **Putts**). Leave a field
   blank to skip it.
5. Name the shortcut and tap **Done**.

You can run that shortcut from the Shortcuts app, add it to your Home Screen, put
it in Control Center, trigger it with Siri, or — importantly for the Action
Button and Apple Watch below — pick it from those system menus.

---

## The Action Button (iPhone 15 Pro and later)

The Action Button can run any Golf Stats action. The most useful one on the
course is **Tag a Shot** — one press drops a GPS pin where you're standing.

1. Open **Settings → Action Button**.
2. Swipe to the **Shortcut** screen.
3. Tap **Choose a Shortcut**.
4. Pick the Golf Stats action you want — for tagging a shot, choose **Tag Shot**.
   (The same list also offers **Score Hole**, **Go to Hole**, **Set Flag**, and
   **Set Score**.)

Now a single press of the Action Button tags a shot on the hole you have open.

> ### ⚠️ Use the *Tag a Shot* **Shortcut**, not the *Tag a Shot* **Control**
>
> When you assign the Action Button, you may notice Golf Stats appears in **two**
> places:
>
> - under **Shortcut** (the App Intent — what step 4 above selects), **and**
> - under **Controls**, as a *Tag a Shot* **Control Center control**.
>
> **Choose the Shortcut, not the Control.** A Control Center control **requires
> your iPhone to be unlocked to run** — so if you press the Action Button with
> the phone locked in your pocket on the course, the *Control* version won't tag
> the shot until you unlock. The **Tag a Shot Shortcut** runs the action
> directly and is the reliable choice for the Action Button.

---

## Control Center & Lock Screen controls

Golf Stats adds three controls you can drop into **Control Center** or onto the
**Lock Screen**:

- **Tag a Shot** — *"Drops a shot pin at your current location on the hole you're viewing."*
- **Set the Flag** — *"Sets the hole's flag pin at your current location on the hole you're viewing."*
- **Score This Hole** — *"Scores the hole you're viewing from its tracked shots, then moves to the next hole."*

Each control briefly opens Golf Stats to run the action on the round you have
open, then shows a short confirmation banner. The wide control tile also shows
the hole you're on (e.g. *Tag a Shot · Hole 7*).

**To add one to Control Center:**

1. Swipe down from the top-right corner to open **Control Center**.
2. Tap the **+** in the top-left corner (or press and hold an empty area) to edit.
3. Tap **Add a Control**.
4. Search for **Golf Stats** and pick **Tag a Shot**, **Set the Flag**, or
   **Score This Hole**.
5. Tap anywhere to finish.

**To add one to the Lock Screen:**

1. Press and hold the Lock Screen, then tap **Customize → Lock Screen**.
2. Tap one of the control slots below the clock.
3. Search for **Golf Stats** and pick a control.

> **Note:** Because controls run through a separate system extension, they need
> the phone **unlocked** to act. For a press-and-go experience on the course,
> prefer the **Action Button + Tag a Shot Shortcut** combination above.

---

## Home Screen & Lock Screen widgets

Two widgets keep your round (and the players you follow) in view:

### Current Hole

*"Shows the hole you're on in your active round."* It displays the hole number,
your to-par, shot count and total. Available sizes:

- **Home Screen:** small and medium (wide) tiles. The wide tile adds the
  tournament, course, weather, and your running total.
- **Lock Screen:** circle, rectangle, and inline (next to the clock) shapes.

### Following

*"Live standings of the players you follow."* It lists each player you're
following live — name, holes played (**Thru**), total, and to-par — best score
first. Available **Home Screen** sizes: small (3 players), medium (4), and large
(up to 8). It refreshes itself periodically and whenever the standings change.

**To add a widget to the Home Screen:**

1. Press and hold an empty area of the Home Screen until the icons jiggle.
2. Tap the **+** in the top-left corner.
3. Search for **Golf Stats**.
4. Choose **Current Hole** or **Following**, swipe to the size you want, and tap
   **Add Widget**.

**To add a widget to the Lock Screen:**

1. Press and hold the Lock Screen, then tap **Customize → Lock Screen**.
2. Tap the area above or below the clock to add widgets.
3. Search for **Golf Stats** and pick **Current Hole** (the **Following** widget
   is Home-Screen only).

> The **Current Hole** widget fills in once you have a round open in the app; the
> **Following** widget fills in once you're following at least one live round
> (tap the live icon on the tournament list and enter a share code).

---

## Apple Watch — Siri & the Action Button

The Apple Watch app has the **same five actions** as the iPhone. On the watch
they act on the round **connected to the watch**, so first connect a round:

1. On the iPhone, open the round you're playing.
2. Tap the round's **•••** menu → **Connect to Apple Watch**.

Then, on the watch, you can:

- **Use Siri** — raise your wrist and say *"Score this hole in Golf Stats"*,
  *"Tag a shot in Golf Stats"*, *"Go to a hole in Golf Stats"*, *"Set the flag in
  Golf Stats"*, or *"Set my score in Golf Stats"*.
- **Use the Action Button (Apple Watch Ultra)** — open **Settings → Action
  Button → Shortcut** on the watch and choose a Golf Stats action (e.g. **Tag
  Shot**).

If no round is connected, the action replies *"No round is connected to your
watch. Open Golf Stats on iPhone and connect a round first."* Tagging a shot or
setting the flag also needs the watch's location and a GPS fix outdoors.

---

## Apple Watch — complications on a watch face

Two complications put Golf Stats on your watch face:

- **Current Hole** — *"The hole you're playing, with score and to-par."*
- **Following** — *"Live standings of the players you follow."*

Both come in the four watch complication shapes — **rectangular**, **circular**,
**corner**, and **inline** — so they fit most faces.

**To add a complication:**

1. On the watch, **press and hold** the watch face, then tap **Edit**.
2. Swipe to the **Complications** screen.
3. Tap the complication slot you want to use.
4. Scroll to **Golf Stats** and pick **Current Hole** or **Following**.
5. Press the Digital Crown to save.

You can also do this from the iPhone: **Watch** app → **Face Gallery** (or your
current face) → tap a complication slot → choose Golf Stats.

> The **Current Hole** complication updates while a round is connected to the
> watch; the **Following** complication shows the live standings of players you
> follow (it refreshes periodically).

---

## Apple Watch — running an action from your watch face (Run Shortcut)

The Golf Stats **complications above are glanceable displays** — tapping one
opens the app, it doesn't *run* a scoring action. To **trigger an action**
(like Tag a Shot) **straight from the watch face**, use watchOS's built-in **Run
Shortcut** complication. This needs one extra step, because a watch-face
complication can only launch a **saved shortcut**, not a raw app action:

**Step 1 — Create a shortcut for the action.**

1. On the iPhone, open the **Shortcuts** app.
2. Create a new shortcut with a single action: search for **Golf Stats** and add
   **Tag a Shot** (or whichever action you want).
3. Give it a clear name like *"Tag Shot"* and tap **Done**.
4. The shortcut syncs to the Apple Watch automatically. (You can also open the
   **Shortcuts** app *on the watch* and confirm it's listed there.)

**Step 2 — Add the Run Shortcut complication to your watch face.**

1. On the watch, **press and hold** the watch face → **Edit** → swipe to
   **Complications**.
2. Tap a complication slot.
3. Choose **Shortcuts** from the list, then select **Run Shortcut**.
4. Pick the **Tag Shot** shortcut you created in Step 1.
5. Press the Digital Crown to save.

Now tapping that complication on your watch face runs the Golf Stats action
directly. Remember a round must be **connected to the watch** (and, for Tag a
Shot / Set the Flag, location must be allowed) for it to take effect.

---

## Permissions & requirements

- **Location** — only **Tag a Shot** and **Set the Flag** use it, and only at the
  moment you run them (When-In-Use). Grant Golf Stats location access when
  prompted, or in **Settings → Privacy & Security → Location Services → Golf
  Stats**.
- **No account, no Siri sign-in, no extra entitlements.** These features collect
  no data and send nothing to a server. (The **Following** widget/complication
  reads the live standings of the share codes you already follow.)
- **Real devices.** Siri voice, the Action Button, and the Apple Watch path all
  require physical devices.
- **Localized.** Every action title, description, spoken reply, and even the Siri
  trigger phrases are translated into all supported languages.
