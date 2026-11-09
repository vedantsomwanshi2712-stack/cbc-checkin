# CBC Check-in

The check-in page for **Claude Builder Club, IIT Delhi** meetings.

**Live page:** https://vedantsomwanshi2712-stack.github.io/cbc-checkin/

The page is only open during club meetings. At any other time it shows a "Check-in is closed" message.

---

## For members

1. Open the link or scan the QR code shown at the meeting.
2. Fill in the form and submit.
3. That's it. You can't check in after the meeting ends.

## For organisers

Everything is controlled from the settings block at the top of the `<script>` in `index.html`.

### Open or close check-in

1. Open `index.html` in this repo and click the **pencil icon** to edit.
2. Change the master switch:
   ```js
   var OPEN = true;   // check-in is live
   var OPEN = false;  // check-in is closed
   ```
3. Click **Commit changes**. The live page updates within a minute or two.

### Open and close automatically (optional)

Set a time window in India time, and the page opens and closes by itself:

```js
var OPENS_AT  = "2026-11-12T18:00";
var CLOSES_AT = "2026-11-12T19:30";
```

Leave both as `""` to rely only on the `OPEN` switch. `OPEN` must still be `true` for the window to apply.

### Change the closed message

```js
var CLOSED_TITLE = "Check-in is closed";
var CLOSED_TEXT  = "This form is only open during Claude Builder Club meetings.";
```

## Meeting-day checklist

- [ ] Set `OPEN = true` before the meeting starts
- [ ] Show the link or QR code on the projector only
- [ ] Set `OPEN = false` as soon as the meeting ends

---

Hosted on GitHub Pages. Maintained by the CBC IIT Delhi team.
