AnyList Recipe PDF Maker
==========================
An Applescript to automatically create PDFs of your AnyList Recipes

---

1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Setup](#setup)
4. [Run](#run)
5. [Teardown](#teardown)

## Overview
[AnyList](https://www.anylist.com/) is a great app/website for creating shopping lists and managing recipes.  

Unfortunately, it does not have a way to backup or bulk export recipes.  This makes it difficult to (A) backup recipes
and (B) share them with others.  You can email or print/pdf individual recipes, but that's not great if you want
to backup or share more than a few at a time.

I briefly looked into parsing the data directly from the server, but it's some kind of protobuf format that I don't feel
like spending the effort to reverse engineer; and then have to figure out how to reformat nicely.  Instead, we can just
script printing each recipe to a PDF using AppleScript!

This is still pretty rough around the edges, but I'm hoping to make improvements over time.  Make sure to follow the
steps below carefully each time.

## Prerequisites
- Mac OS X (probably Big Sur (11.4)+)

## Setup
1. Requires Safari to allow javascript from Apple Events, but you might want to turn it off when done for security
   - See [this page](safari-applescript-enable.md) for details
1. Go to https://anylist.com/web in Safari and login
1. Click "View All Recipes" on the "Recipes" page
   1. If you want to print a subset of recipes, feel free to select a different collection
1. Select the first recipe in the list
1. Set print directory and other print settings (if you did this last time, then it's not necessary to set again - it should remember)
   1. Press cmd+p to open the print dialog
   1. Configure any print settings you want (e.g. "Print headers and footers", etc)
   1. Click "PDF" and select "Save as PDF"
   1. Select a directory
   1. Cancel out of all dialogs to get back to the Anylist webpage

## Run
1. Make sure to follow the [Setup](#setup) above
2. Open script in Script Editor and run it (play button)
   1. If you've never run an AppleScript before, you may have to give permissions
3. Leave the computer alone while it runs just in case

## Teardown
1. Disable javascript from Apple Events in Safari
   - See [this page](safari-applescript-enable.md) for details
