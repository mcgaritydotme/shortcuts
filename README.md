# shortcuts

Sharing my most-used macOS and iOS shortcuts for the benefit of others.

Instructions for importing these are described on the [Apple Support site](https://support.apple.com/en-gb/guide/shortcuts-mac/apd02bffbaac/mac).

## [Apple Notes](apple_notes)

### Create Meeting Notes in Apple Notes ###

Creates a brand-new Apple Notes note, pre-populated with sections to capture meeting attendees & minutes, then organizes it customer- or organization-specific tags.

## [Bear](bear)

### Create Meeting Notes in Bear ###

Functionally the same as [Create Meeting Notes in Apple Notes](https://github.com/mcgaritydotme/shortcuts/blob/main/README.md#create-meeting-notes-in-apple-notes), but instead creates the brand-new note in Bear and "pre-files" it into a customer- or organization-specific tag under #Work/Meeting-Notes.

## [Day One](day_one)

### Add to Daily Note ###

Appends user input to a daily note within Day One (or creates the note if it doesn’t already exist for the current date).  This is configured to be pinned to the Menu Bar, which allows you to run it by navigating to menu bar > Shortcuts > Add to Daily Note

### Import PDFs into Day One ###

For the folder selected at runtime, extracts the text from any PDF file and creates separate Day One entries in the journal named "Journal" (edit the shortcut to pick an alternative destination).  Creation date of the PDF file is used as the Day One entry date.  Each new Day One entry is tagged with "Import".

## [macOS](macos)

### Batch-Resize Images ###

For one or more images selected, batch-resizes each and saves as a new image in the same folder.  Invoked as a Quick Action from the macOS Finder menu.  Final image size and crop starting location can be configured within the shortcut.  Note: this may also work from iOS, I just haven't tested it from there.

## [Notion](notion)

### Create Notion Gallery Header ###

For an image selected from your local device, it will overlay said image over a white background which is sized to best-fit within [Notion gallery headers](https://www.notion.so/help/galleries), which is typically 1500 px wide x 600 px tall.  If your selected image is too long or short, it will also be resized to fit vertically.

## [Safari](safari)

### Avert Paywall ###

Takes any URL (including those not already open in Safari) and processes them thru [archive.today](https://archive.today), which bypasses nearly all paywalls.

## [Things 3](things_3)

### Create GTD Weekly Review

Creates a new project for GTD weekly review. Adjust the included JSON to customize to-dos to match your review style / needs.  This supports adding descriptions and checklists to individual to-dos.

> [!IMPORTANT]
> This shortcut assumes you have an existing area named "Weekly Routines" to hold the project.  If not, edit the shortcut to reference a different Area (or none at all).

Example output after running the shortcut:

![Screenshot of Create GTD Weekly Review results](things_3/Create%20GTD%20Weekly%20Review%20Results.jpg)

### Get Things 3 Project URL

For a selected project, returns a callback URL that can be used to navigate directly to the project.  Useful for generating a URL to store in note-taking systems like Craft, Notion, Bear, etc.

### Someday Projects Hygiene

For each Project with Start = Someday, loops thru child to-dos to set their Start = Someday as well

## Notes to Self

### Signing Shortcuts

Starting with iOS 15, exported Shortcuts (like those within this repository) require signing before others can import them.  More about signing Shortcuts is available in the [official documentation](https://support.apple.com/en-au/guide/shortcuts-mac/apd455c82f02/7.0/mac/14.0#apd7006838ef).

This is accomplished using the following Terminal command in macOS:

`shortcuts sign --mode anyone --input "Import PDFs Into Day One.shortcut" --output "New Shortcut.shortcut"`

There’s apparently a bug in macOS Sonoma — specifically 14.14.1 — which prevents signing.  No matter what, it results in the following error:

`ERROR: Unrecognized attribute string flag '?' in attribute string "T@"NSString",?,R,C" for property debugDescription`

My workaround for now is signing the Shortcuts from my older MacBook Pro that is running macOS Big Sur 11.7.10.
