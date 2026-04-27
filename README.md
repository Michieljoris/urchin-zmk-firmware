This repo has my personal keymap for a 14-34 keyboard and implementations for a zmk ([Urchin Keyboard](https://github.com/duckyb/urchin)) and kanata .. link.

Keymap features:
- 26 keys with combos and no layers and single thumbkey, otherwise called 'the spacebar'
- use one extra conceptual layer to reduce number of combos
- add 6 keys (32 keys total) to reduce combos again, still only base and one extra layer
- add 2 thumbkeys and one extra layer to be left with just one combo. On a 4 thumbkey keyboard left and right would mirror each other, each thumb accessing a the same space and mod-layer keys
- designed for easy transition from qwerty 
- can be used single handed with 2 thumbkeys, so 14-17 keys
- includes all letters, numbers, symbols, function, navigation and media keys. All can be modded with any combination of shift/alt/ctrl/gui, from 12 to 34 key layouts.
- single thumbkey versions don't use this key for layer change. They can also be used on regular keyboards. These normally don't have dedicated thumbkeys anyway just a spacebar.
- optional mod-combos instead of mod-taps. This side steps the problem of rolling mistypes.

Rationale (or personal preference/experience):

- I don't like layers, they're rather confusing, this goes even more for thumb controlled layers. We already have 4 modifiers, one of which is even a layer change (shift). Also, while a dedicated 32 key split keyboard is nice often I end up typing on a laptop keyboard or some other desktop keyboard. These don't have dedicated thumb keys, just a space bar.
- I don't like learning a new key layout, qwerty works fine and it's the default layout on almost all computers. 
- I want to commit to a layout, not a keyboard. The layout should work on any keyboard.
- I'm not optimizing for speed of typing but for convenience and ease of use. And facilitating the use of more ergonomic smaller and split keyboards when available.
- The thumb is the clumsiest finger on the hand, made for gripping, not fine movement. There's a reason pianists assign the thumb more than any other finger a special musical role. They're hard to control. 
- macos and linux treat the meta/super/cmd/gui key differently. So while it's practical to use the meta key for eg. windown management on linux, macos hogs the cmd key, it's kind of a control key. A hyper key (alt+ctrl+cmd) makes the keymap for uses like this portable again. This can be assigned to the singular thumbkey (spacebar) as a mod tap.
- design should be simple and logical and minimal. It should be possible to recreate it by memory or on paper by its design priniciples alone.

To achieve the above:
- mod taps for shift/alt/ctrl/gui on home row, except for gui. The vacant spot is used for layer change. 
- combos for numbers which become fn keys on the alternate layer
- any symbol that's not a shifted number is on the alternate layer together with keys not covered by the finger keys such as [], {}, -, =, `, \.
- media and nav keys fill up some more of the alternate layer
- leader key for settings such as bluetooth, reset etc.

Design principles:
- qwerty layout for all keys covered by the keys available, and logical placement of combos for the rest. Eg. the backtick is on a combo in the left hand, top row. 
- vim and cursor keys on same keys
- numbers as combos are always two horizontally adjacent fingers. Left hand takes five, right takes five. Symmetrical placement. Numbers should move from left to right.
- brackets, braces, parents etc should be easily accessible, the opening type especially, since editors automatically supply the closing one.
- cursor keys, home/end/pgup/pgdown keys, as combos should be logically placed.
- return, tab and esc are on central combos
- the 4 mod keys should be combineable in all permutations and with any key, and persistent if needed (not one shot)
- numbers and fn keys should be in same place
- an extra, optional layer. Right hand part is activated by the left hand, the left hand one by the right hand. Conceptually this is 'one' layer, but a few media keys can be snuck in to the activating side. 

For local zmk build:
- follow instructions on zmk site ... link
- includes shield from .. link.. for local build
- needs local clones of zmk leader and unicode modules ... link
- can be built on github actions as well TODO

[Download the firmware zip from the latest action run.](https://github.com/duckyb/zmk-urchin/actions/workflows/build.yml?query=is%3Asuccess+branch%3Amaster) Check [the ZMK docs](https://zmk.dev/docs/user-setup#installing-the-firmware) for instructions on how to flash it.
