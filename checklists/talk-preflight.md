# Talk-day preflight checklist

Copy this file, fill in the three variables, and tick the boxes. It is written for a talk given from a laptop with a slide deck (HTML or PDF) on a projector or wall display, where the deck may sit on its last slide for a long stretch (commentary, replies, Q&A) with no keypresses. Goal: no sleep, dim, screensaver, lock screen, notification or wrong clock on the display.

Variables:

- `{date}` : day and start time of the session
- `{room}` : where you present (check it again the day before; programs change)
- `{timezone}` : the time zone of the room, for example `America/Denver`

Talk: `{date}`, room `{room}`, clock set to `{timezone}`.

## 1. The day before (at home or at the hotel)

- [ ] Run your final build and export every file you will carry: the deck, a PDF copy, printed speaker notes, a handout if you use one.
- [ ] Open the deck once from a local file in your browser with Wi-Fi **off** and walk it end to end. Nothing may be fetched from the network.
- [ ] Open the PDF copy from the USB stick on your laptop once.
- [ ] Print the speaker notes and keep them where you can reach them without the laptop.
- [ ] Copy every file to an offline backup: a USB stick, plus a second copy on a different device or cloud folder you can open without logging in on a stranger's machine.
- [ ] Pack: charger, display adapters for HDMI and VGA (the room's ports are unknown), a spare cable, the clicker and its spare battery.
- [ ] Charge the laptop to 100%.
- [ ] Re-check `{room}` and the session time against the latest program.

## 2. Laptop settings (once, before the day)

Set these so the machine does not power down during the quiet stretch.

| Setting | macOS | Windows | Linux (GNOME) |
|---|---|---|---|
| No sleep on power | System Settings > Battery > Options: prevent automatic sleeping on the power adapter | Settings > System > Power: Screen and sleep = Never when plugged in | Settings > Power: Automatic suspend = Off when plugged in |
| No screen saver or lock | System Settings > Lock Screen: display off = Never, screen saver = Never, password delay long or Never | Settings > Personalization > Lock screen: screen saver None; sign-in required = Never | Settings > Privacy > Screen: blank screen = Never, automatic lock = Off |
| No power saver dimming | Low Power Mode = Never; dim on battery off; auto-brightness off; fixed brightness | Battery saver off; adaptive brightness off; fixed brightness | Power saver off; automatic brightness off; fixed brightness |
| Quiet notifications | Focus / Do Not Disturb on, nobody allowed; notifications off while mirroring or sharing | Focus assist / Do Not Disturb on (priority only, empty list) | Do Not Disturb on |
| Clock | Set the time zone to `{timezone}` so the laptop matches the room | same | same |

- [ ] Browser: one window, no other tabs, sound muted.

## 3. Thirty minutes before the session

- [ ] Plug into the wall. Do not present on battery. Confirm the power indicator shows charging.
- [ ] Connect the adapter. Set the displays to **extended**, not mirrored, so the presenter view stays on the laptop. If the room forces mirroring, run from the printed notes. Use 1920 x 1080 or the projector's native resolution at 60 Hz.
- [ ] Choose the right input on the projector or wall panel. Find the projector's auto-off or eco timer and disable it if you can. Know where the Blank and Freeze buttons are and do not press them by accident.
- [ ] Turn Do Not Disturb on. Quit chat, mail, calendar, sync clients and update prompts. Turn Wi-Fi off if the deck is offline (this also stops update pings).
- [ ] Keep the machine awake from a terminal and leave the window open until you pack up:

  | OS | Command | Check |
  |---|---|---|
  | macOS | `caffeinate -dis` | `pmset -g assertions` lists PreventUserIdleDisplaySleep |
  | Windows | `powercfg /requests` to check; use Settings > Power as above, or run a keep-awake tool you trust | `powercfg /requests` shows the display request |
  | Linux (systemd) | `systemd-inhibit --what=idle:sleep --why="talk" sleep infinity` | `systemd-inhibit --list` shows the lock |

- [ ] Open the deck, drag it to the projector display, click once so keys go to it, go full screen. Open the presenter view and drag it to the laptop screen. Confirm both follow each other.
- [ ] Move the pointer off the projected display. Note where the dock, menu bar or taskbar hide.
- [ ] Walk the first scenes once, then return to the title. Test the end-of-talk hold or Q&A mode, then clear it.
- [ ] Reset the presenter timer.
- [ ] Test the clicker from where you will stand.

## 4. Back-of-room check

- [ ] From the back row, on the real screen, open three or four of the densest or lowest-contrast slides. Can you read them? Compare the dark, light and high-contrast modes on that screen and choose before the session starts.
- [ ] Check animations and timings on this laptop. If a transition stutters, switch to reduced motion or crossfades and close other tabs and apps.

## 5. At the start and at the close

- [ ] Title slide up, presenter view visible, timer ready, keep-awake command still running.
- [ ] At the close, hold on the final slide. If the room goes quiet for a minute, move the mouse or press Shift (not a deck key). Leave the lid open.

## 6. If it goes wrong

- **Laptop screen dark or locked:** move the mouse, press Shift, enter the password. Check the keep-awake command is still running and restart it.
- **Projector says no signal or blanks while the laptop is fine:** press the projector's source button, unplug and replug the adapter, run Detect Displays, click the slide and go full screen again. A projector that switched itself off needs about a minute to warm up: keep talking from the notes.
- **Full screen lost:** click the deck and press the full-screen key again.
- **Deck will not load:** open the PDF copy full screen from the laptop or the USB stick, and use the printed notes.
- **Projector failure plan:** if the display stays dead, present from the printed notes and hand out the handout. The argument has to survive on paper.

## 7. Fallback ladder

Go down a rung only when the one above fails.

1. The deck file on the laptop, opened locally.
2. The previous tagged build of the deck, from your backup folder.
3. The PDF copy on the laptop.
4. The PDF copy on the USB stick, opened on the room computer.
5. Printed notes and handout.

---

Part of [palimnote-templates](https://github.com/hyderhusainarastu/palimnote-templates). More at [github.com/hyderhusainarastu](https://github.com/hyderhusainarastu).
