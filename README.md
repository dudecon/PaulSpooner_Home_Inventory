# Home Inventory Vault

This README is written in plain simple Markdown so it displays correctly in Notepad's View > Markdown > Formatted mode.

Note: The other .md files in this vault (the actual inventory notes) use a special visible data block at the top. This README does not, so it stays easy to read in Notepad.

## How This Vault Stores Data

Every single .md file starts with a visible block like this:

\---

type: something

name: Example Name

... other lines ...

\---

This is NOT hidden Obsidian frontmatter. The backslashes before the --- and the [[ links are on purpose so the text stays readable as plain text.

## Folder Structure

- Locations/         = Fixed places (house, rooms, garage, property). Use "parent" to nest them.
- Containers/        = Movable storage (bags, buckets, boxes, toolboxes). Use "parent" to say where they live.
- Items/             = Things you actually own. Each gets its own file with specs, photos, location.
- Projects/          = Things you plan to build, fix, or 3D print.
- Wishlist-Locations/, Wishlist-Items/, Wishlist-Containers/ = Future plans.
- attachments/       = Photos and manuals. Link them from the data block at the top of a file.

## The Visible Data Block (the most important part)

All your notes use a visible data block at the very top. When you create a new file, copy one of the patterns below exactly, including the \--- lines and the &#x20; prefixes on indented lines.

The &#x20; is a literal string that appears in every existing file (it came from an old copy-paste). It makes the lines look indented when the file is viewed in some programs.

### Location Template (for files in Locations/)

Copy this block exactly to the top of a new location file:

\---

type: location

name: My New Room

parent: \[\[Garage]]

tags: \[location, workshop]

utilities: "Power, lights, heat"

dimensions-internal:

&#x20; length:   12 ft    #

&#x20; width:    10 ft    #

&#x20; area:     120 sq ft  #

&#x20; notes: "needs paint"

\---

After the block, write normal Markdown:

# My New Room

Description here.

## Quick Contents List

- item one
- item two

## To-Do

- [ ] something

See real examples: Locations/House.md, Locations/Garage.md, Locations/Tool-Room.md

### Container Template (for files in Containers/)

Copy this block exactly:

\---

type: container

name: My New Toolbox

parent: \[\[Garage-Closet]]

tags: \[container, tool-bag]

dimensions-internal:

&#x20; length:   20 in    #

&#x20; width:     9 in    #

&#x20; height:    9 in    #

\---

After the block add description and a Quick Contents List.

See real examples: Containers/Hammer-Toolbox.md, Containers/Screw-Bucket.md, Containers/Craftsman-Bag.md

### Item Template (for files in Items/)

Copy this block exactly:

\---

type: item

name: Example Cordless Tool

brand: Milwaukee

model: 2401-20

serial: \[enter serial here]

value: 40

purchase-date: \[YYYY-MM-DD]

condition: good

quantity: 1

tags: \[power-tool, milwaukee]

photos: 

&#x20; - attachments/my-photo.jpg

location: \[\[Screw-Bucket]]

\---

After the block write normal notes, key specs, etc.

Variations you will see in real files:
- Many items have lots of "TBD" fields + a "Verification steps" list (see Framing-Nailer.md and Pancake-Air-Compressor.md)
- Some use extra fields like accessories, parent-item, requires-utilities, provides-utilities

See real examples: Items/Cordless-Screwdriver.md, Items/Electric-Lawnmower.md, Items/Angle-Grinder.md

### Wishlist Item Template (for files in Wishlist-Items/)

Copy this block exactly:

\---

type: wishlist-item

name: 30 Gallon Air Compressor

status: planned

priority: high

cost-est: 300-600

tank-size-desired: 20-30 gal

features-desired: 

&#x20; - wheeled

&#x20; - 4+ SCFM at 90 PSI

brand-options: 

&#x20; - Fortress

&#x20; - Husky

compatible-with: \[\[Framing-Nailer]]

target-location: \[\[Garage]]

tags: \[compressor, wishlist]

\---

See real examples: Wishlist-Items/30Gal-Wheeled-Air-Compressor.md, Wishlist-Items/Brad-Nailer-Pneumatic.md

### Wishlist Location Template (for files in Wishlist-Locations/)

Copy this block exactly:

\---

type: wishlist-location

name: Ideal Pneumatic Workshop

status: planned

priority: high

estimated-total-cost: 500-800

project: Workshop upgrade 2026

instantiate-when: "next big reorganization"

\---

See real example: Wishlist-Locations/Ideal-Pneumatic-Workshop.md

### Wishlist Container Template (for files in Wishlist-Containers/)

Note: these currently use "type: container" plus a special status line.

Copy this block exactly:

\---

type: container

name: Nailgun Supplies Bin

parent: \[\[Garage]]

tags: \[container, supplies]

dimensions-internal:

&#x20; length: TBD in

&#x20; width: TBD in

&#x20; height: TBD in

status: wishlist-container

priority: medium

cost-est: 50-120

\---

See real example: Wishlist-Containers/Nailgun-Supplies.md

### Project Template (for files in Projects/)

Copy this block exactly:

\---

type: project

name: Build M12 Dummy Battery

status: planned

priority: medium

target-item: \[\[Cordless-Screwdriver]]

location: \[\[Screw-Bucket]]

estimated-cost: 45

\---

After the block add goal, parts list, and a Tasks section with checkboxes.

See real example: Projects/M12-Dummy-Battery-Adapter.md

## Key Rules and Quirks

- Always start the file with the \--- block.
- Inside the data block, escape brackets like this: \[ and \[\[
- Use the literal characters &#x20; (ampersand hash x 2 0 semicolon) on any indented lines under dimensions, photos, features-desired, etc. This matches every existing file.
- Links between files use the form \[\[Exact File Name Without .md]]
- You do not need a separate file for every single screw or nail. Use "Quick Contents List" sections inside a container or location note for small stuff.
- When you buy something from a wishlist: move the .md file to the real folder, change the type and status lines, fill in real values, and add a photo link.

## Photos

Put photos in the attachments/ folder.

Reference them like this inside the data block:

photos: 

&#x20; - attachments/lawnmower.jpg

## Next Steps

1. Use the templates above when creating new notes.
2. Keep the visible data block at the top of every file consistent.
3. Add real photos when you can.

When something moves from "planned" to "owned", move its file and update the top block. The folder names + the type/status lines tell the whole story.

