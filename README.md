# HanziCopyTool

HanziCopyTool is an add-on for Anki 2.1, which was requested on the r/anki subreddit.
The add-on is used to add gifs of the stroke order of hanzi characters, which are on a note.
The gifs are copied from notes of [this](https://ankiweb.net/shared/info/39888802) deck and must be dowloaded in order to use this add-on.

# Setup
Download the repository as a zip archive and extract it into the add-ons directory of Anki 2.1.
This directory can be found by opening anki and clicking Tools -> Addons -> View Files.
Then open the file hanzi_copy_tool.py with an editor of your choice.
Change the value the following variables:

TARGET_MODEL: The name of the note type to which the gif files will be copied to. TARGET_LOOKUP: The name of the field, which is contains a word or pharse with hanzi characters.
TARGET_FIELD: The name of the field, to which the gifs will be copied.

The default values use the Basic note type with the Front and Back field.
There are also variables used to specify the note type and fields of the notes, from where the gifs are copied.
These are already configured to work with the above deck.
However it is possible that the name of the note type as been changed during importing.
You can either rename the note type to 'Hanzi Writing' or you can change the value of the variable SOURCE_MODEL to match the name.


# Usage
The add-on adds a new button to the note editor.
When the button is clicked, the add-on will use the hanzi characters of the lookup field and copy the givs that could be found to the target field.
Note that everything inside the target field will be replaced with the found gifs.
It is possible, that a gif for a character could not be found.
A notification is shown in this case.
The same action can be performed with the hotkey 'CTRL+H'.

Using the note browser it is possible copy the gifs to multiple notes.
Open the browser and select the notes to which the gifs need to be copied to.
The click Edit -> Bulk Copy Hanzi Stroke Order to execute the process.
With this method the target field will only be written when it is empty.
Already existing content in the field will not be chagned.
Notes where certain gifs could not be found will be taged with "Hanzi_Tool_Error".
Use the filter inside the browser to review those notes.

# Misc
The icon used for the button in the note editor comes from Feather and can be found [here](https://feathericons.com/). 
