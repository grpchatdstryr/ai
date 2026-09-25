# Apple Shortcuts Automations

## Daily Walk

Sources: IMG_1601.PNG and IMG_1602.PNG.

### Triggers

- At sunset.
- Or 15 minutes before sunset.

### Actions

1. Get the current date.
2. Show notification: “The sun sets soon, get ready for your walk!”
3. Open Fitness.
4. Set a Duration measurement to 20 min.
5. Start a timer for the Measurement variable, with the timer unit set to seconds.
6. Append “Ran on [Date]” to the note “Run Tracking”.

## Turn On Grayscale

Source: IMG_1600.PNG.
The screenshot truncates the title after “Turn On Grayscale (iPh...”.

### Trigger

- At 10:00 PM.

### Actions

1. Get the Device Model.
2. If Device Model contains “iPhone”:
   - Turn color filters On.
   - Switch to Wallpaper 6.
3. End If.

## Turn Off Grayscale

Source: IMG_1599.PNG.
The screenshot truncates the title after “Turn Off Grayscale”.

### Trigger

- At 7:00 AM.

### Actions

1. Get the Device Model.
2. If Device Model contains “iPhone”:
   - Turn color filters Off.
   - Switch to Wallpaper 5.
3. End If.

## It’s 10 PM

Source: IMG_1598.PNG.

### Trigger

- At 10:00 PM.

### Action

1. Show notification: “Close YouTube/TV for the night”.

## It’s 9:55 PM

Source: IMG_1597.PNG.

### Trigger

- At 9:55 PM.

### Action

1. Show notification: “5 minutes until 10:00 PM”.

## On Call - Turn On Ringer

Source: IMG_1604.PNG.

### Trigger

- At 10:00 PM.

### Actions

1. Find Calendar Events where all of the following are true:
   - Title contains “On call”.
   - Start Date is today.
   - Sort by: None.
   - Limit: Off.
2. If Calendar Events has any value:
   - Turn Silent Mode Off.
   - Show notification: visible text begins with “🚨”; the rest is obscured.

The remaining actions and the end of the conditional are not visible.

## On Call - Turn OFF Ringer

Source: IMG_1603.PNG.

### Trigger

- At 8:55 AM.

### Actions

1. Find Calendar Events where all of the following are true:
   - Title contains “On call”.
   - Start Date is today.
   - Sort by: None.
   - Limit: Off.
2. If Calendar Events has any value:
   - Turn Silent Mode On.
   - Show notification: visible text begins with “🔇”; the rest is obscured.

The remaining actions and the end of the conditional are not visible.
