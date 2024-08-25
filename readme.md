# badger-whome
**A Badger2040 app for plural people**

A name and pronouns badge that can be changed using the front buttons on the Badger2040, so that you can have multipul different name and pronoun sets avaible for use. Designed by a plural person for use at events where it can be out, but there are multipul other uses for it including characters, cosplays, furonas, etc.

## Setup

- Copy the `whome` and `examples` directories from this repostory to the root of the badger
- Rename `parts-example.json` to `parts.json` 
- Edit `parts.json` to include the information that you with the Badger to display

### /whome/parts.json

There is an example file in `/whome` to use this file it needs renaming from `parts-example.json` to `parts.json`, and editing to include the information that you wish the badge to show.

Future upgrade: this file will also be generated by my serve-whome project, but this feature is not yet implimented.

``{
    "label": {
        "name": "Display Name",
        "pronouns": "They / Them",
        "tag": "I'm the coolest one of us",
        "pips": "4"
    }
}`` 

**label** - each label needs to be unique, if there is a matching .jpg file in the /alt-parts/ directory it will display that in the bottom right 64px of the screen, it will not scale so will only who the top left 64px most of the image, if there is no matching image file it will display the default image

**name** - the name that you want displayed in the top row of the screen ( max 8 characters )

**pronouns** - medium sized text displayed under your name ( max 10 characters )

**tag** - some fun text to be displayed at the bottom of the screen, under pronouns ( max 2 lines of 20 characters, but wrapping will make this less )

**pips** - the pips space can display beween 0 and 4 pips with half pips, so this accepts any number between 0 and 8, numbers higher than 8 will just display 4 full pips, non-numbers or numbers less than 0 will display no pips 

## Useage

Select alt-parts from the badger os menu, then use the up and down arrow buttons to select which name and pronoun set you wish to display. The buttons will wrap around, when you get to the end / beginning.

*A future expansion of this will include the ability to quick switch to the first three enteries in `parts.json` but right now that fuctionality just picks the first three alpherbetically by label.* - known bug, it picks random peeps from the list as list not sorted