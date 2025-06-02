# Graphic-video-card-Vesa-VBE-modes-list

This repository simply contains some plain text lists generated with VIDMODES.COM with a dos batch file, and is in response to the Github project:

"Modern Generic SVGA driver for Windows 3.1" by "PluMGMK"

"https://github.com/PluMGMK/vbesvga.drv"

This driver also works with Windows 98se. (and it's fast)

The lists contain the ID strings (often a gpu name) of the tested card and the Vesa "VBE" resolutions offered by the card. These resolutions seem to lag behind date-wise, the resolutions offered by the monitor manufacturers.

Cross referencing the ID string / GPU name with information on Wikipedia may give you a starting point to finding the name of an actual retail or OEM video card.

As an example, the only video card that I've found so far to support 1920x1200x24/32 under VBE had the ID = "(C) 1988-2010, Advanced Micro Devices, Inc. OLAND 01.00" and this ID string came from a "Dell NMN1D Radeon R5-430 1GB GDDR5 PCIe x16 Low Profile Graphics Card"

A card that supports a given resolution under it's own proprietary windows or Linux driver will not necessarily offer the same resolution under VBE. The higher the resolution and the older the card, the more unlikely this becomes.

Many video cards can read information supplied by the video monitor about the screen's video capabilities via electrical signals in the video data lead, vga, dvi, hdmi etc. These electrical signals are referred to as DDC or E-DDC "Enhanced-Display Data Channel" the data supplied has "many names" such as E-EDID "Enhanced Extended Display Identification Data" and can be very confusing. Suffice to say "some cards" will use this information to restrict the list of "offered" VBE resolutions, at least I beleive I've seen this behaviour.

EnTech's Monitor Asset Manager (moninfo.exe) can read the Display Data Channel information and display it in a human readable form.

Note: If moninfo.exe cannot read the DDC it will only offer you some "sample" data to read, or if it finds some proprietary windows driver data in the "Registry" it will also supply that info as well. This mostly applies to laptops, as they don't usually have DDC. Finally if moninfo.exe does find the DDC data, it will list it under the name "Real-time".

It is difficult to prove a negative, but despite vesa documentation such as the "Generalized Timing Formula Standard" I am of the opinion that it is not possible to select different (custom) resolutions via the VBE command set, but only modify the vertical & horizontal refresh rates of existing VBE offered resolutions.

You will find a lot duplication in the lists, some of this is because the card has been read twice, and a other times different cards give the same data.

It would useful if someone were to write a parsing routine to re-write the data in a more accessible format for listing multiple cards, that could be easily searched and viewed  perhaps in an html format. Then this data could be kept and updated on a forum such as "vogons.org"

All data is good, negative or positive is all worth while, not just high end card info.
