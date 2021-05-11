---
redirect_from:
 - /making-a-macro
 - /making-a-macro.html
 - /wiki-en/making-a-macro
 - /wiki-en/making-a-macro.html
---

*Much of this article was written by [Cogwheel](User:Cogwheel "wikilink") (WoWInterface user [Cogwheel](http://www.wowinterface.com/forums/member.php?s=fb1425bc23be92c345b36cb94dd82662&action=getinfo&userid=17646)).*

This is an article on **making a macro**. A [macro](macro "wikilink") is a list of slash commands. Common slash commands include the following:

-   /say (/s)
-   /whisper (/w, /talk, /t)
-   /reply (/r)
-   /emote (/e, /em, /me)
-   /dance

With macros, these commands can be used from action buttons, and many of them can be used at once. Each unique command goes on its own line and is written exactly as it would be typed it in the chat box. For instance, a macro that makes the player yell "Everybody, dance now!" and burst into dance would be written thus.

`/y Everybody, dance now!`
`/dance`

A mostly complete list of slash commands is available at [List of Slash Commands](List_of_Slash_Commands "wikilink") though at the time of this writing some of the new commands in 2.0 have not been added. WoWWiki is a great source of additional information for macros, especially scripts using the /run command (which will be covered later).

**Note:** Remember, some macros run all at once. This means that when you click the button, the macro runs each command from start to finish before returning control to the game. This has two important effects. First, if you write a macro that takes a long time to execute (like /run for i=1, 100000000 do end), the game will freeze for as long as it takes to run the macro.

Second, and arguably more important, **there is no way to wait in a macro** without freezing the game. This fact will become much more apparent when we start dealing with the /cast command and its ilk. Some AddOns can provide a way to issue a command at a later time, but they can only be used for "benign" functions like chatting, emotes, and issuing commands to other AddOns (though equipping weapons in combat is allowed).

If you don't mind the game freezing, you can use this little workaround to make macros pause:

`/script debugprofilestart();while debugprofilestop()<wait_time do end;`

Where wait\_time is the time, in milliseconds, you want to wait. You can use this with multiple /cast commands, no problem, as long as you wait for the correct cooldown periods.

Making a macro
--------------

First, open up the macro window. You can do this either by opening the main menu and selecting Macros, or by typing /macro (/m) in the chat box. At the top of the window, you'll see two tabs: **General Macros** and ***Yourname* Specific Macros**. General macros are stored on an account-by-account basis and are shared by all your characters. Character specific macros are..., well, you can figure this one out yourself. :P Immediately under the tabs is a grid of 18 boxes where the macros are displayed. Under those, there is a single box which displays your currently-selected macro with a **Change Name/Icon** button next to it. Below that is the edit box where you actually type the macro. Finally, at the bottom you have a number of self-explanatory buttons.

To create a macro, click the **New** button at the bottom of the window. This brings up another small window off to the side where you choose the icon and type a name for the macro. If you choose the question mark icon (<img src="INV Misc QuestionMark.png" title="fig:" alt="" width="15" />), WoW will automatically pick an icon for your macro based on what spells or items are listed in the macro. Once you have chosen an icon and a name, click the Okay button.

**A few notes:** You can control what icon is shown in place of the question mark with the \#show commands. Although you can name two macros the same, it is better to avoid this since some functions of AddOns or even certain macro commands reference macros by name. You can also add custom icons to the list (see the Part III).

Now you will notice that the macro icon you chose has been added to the 18 boxes mentioned earlier (as much of the name as will fit is also displayed on the icon). The newly created macro will also be selected so now it's time to start writing your macro. Click in the edit box of the macro window to start typing.

**Note:** Macros have a 255 character limit. Rumor has it that this is because they store macros on the servers (since patch 3.0.2).

When you are done typing your macro, simply drag its icon from the grid and place it on an action button. The macro will be automatically saved when you first try to use it or when you close the macros window. Click the button, and there you have it!

Casting spells
--------------

During the normal course of play, you aren't likely to type many slash commands that are generally useful for macros. Sure, the occasional emote macro can make for some interesting role playing, but c'mon...There's got to be more to it than that...

There is. Enter /cast, the most common command you will see in macros. The /cast command allows you to cast any spell from your (or pet's) spell book by name. The simplest case is a command like:

`/cast Shadow Word: Pain`

This macro will cast your highest-rank Shadow Word: Pain on your target. It behaves exactly as if you had dragged SW:P onto that spot on your action bar. The action bar code recognizes the spell and will show [cooldown](cooldown "wikilink") and range feedback on the icon. In fact, if you choose the question mark icon mentioned earlier, the action bar will even show the icon for SW:P.

"Ho, hum," you might be thinking... Why not just put the spell on your bar? Well, that's where combining multiple commands comes in handy, and this is exactly what makes macros so useful. What if you're a mage and you want to let your party know that you're about to sheep something? Well, simply put the cast and /p message in a macro (there are better macros for this task—\[insert shameless plug for [CCWarn](http://www.wowinterface.com/downloads/info6826-CCWarn.html) AddOn here\]—but this is a nice, easy to understand example):

`/cast Polymorph`
`/p Sheeping %t! You spank it, you tank it!`

**Note:** Since the macro is executed all at once, the /p command will be issued when you start the cast, and will not care either way whether you have a valid target or whether Polymorph is on [cooldown](cooldown "wikilink"). This also means you can put the two commands in either order and it will have the same effect. If you want to say something only when you actually cast the spell, check out the AddOn [AfterCast](http://www.wowinterface.com/downloads/info4167-AfterCast.html). AfterCast schedules a slash command to run... well... after you cast a spell (within the limitations mentioned at the end of "What is a macro?"). For example:

`/aftercast /p Click the portal to get %t's lazy butt over here`
`/cast Ritual of Summoning`

**Note:** The Blizzard Terms of Use do not allow for any delay-casting or scheduling of secure casting in macros. Aftercast and AddOns like it will not and cannot circumvent this restriction!

### Notes about spell names and ranks

As of [Patch 4.0.1](Patch_4.0.1 "wikilink"), spells no longer have rank. Instead they level with the character.

Using items and trinkets
------------------------

Simple answer: the same way you cast a spell. The command for using an item is (you guessed it) /use. Like /cast, its simplest form takes the name of the item you want to use:

`/use Green Mechanostrider`

There are also a couple other forms of the /use command:

### /use &lt;inventory slot&gt;

This form of use allows you to use an item in the specified slot. See also [InventorySlotId](InventorySlotId "wikilink") for lists of the slot numbers. Example:

`/use 13`

Uses whatever is in your top trinket slot.

### /use &lt;bag&gt; &lt;slot&gt;

You can also use an item in a specific bag location. Lets say you always keep the food you want to feed your pet in the first slot of your backpack. You can easily write a macro to feed your pet as follows:

`/cast Feed Pet`
`/use 0 1`

Bags are numbered 0-4 from right to left (0 is always the backpack) and the slots are numbered starting at 1 going left to right, top to bottom (like reading):

`1  2  3  4`
`5  6  7  8`
`...`

or

`      1  2`
`3  4  5  6`
`7  8  9  10`
`...`

Trading risk of confusion for completeness, /cast and /use function in almost exactly the same way. The /cast command can use items and /use can cast spells. However, /use will actually 'right click' the item. So if you are attempting to /use a trinket it will equip it if it is not equipped but /cast will just cast the buff. In the event that the trinket is not equipped, /cast will result in an error message saying "You must equip this item to use it." This prevents accidentally changing gear. This isn't very useful for simple macros like you've seen so far. However, when you start dealing with macro options and sequences you'll be happy to know that you can intermingle items and spells in the same command.

Multiple actions with one click
-------------------------------

In general, you cannot cast more than one spell with a single click of a macro. Most spells and some items trigger the global [cooldown](cooldown "wikilink") (GCD) which keeps you from taking too many actions at once. Even if a spell fails to cast, if it **would** trigger the GCD, it prevents subsequent /casts in the macro from running. This was not the case prior to patch 2.0 which is why you may still come across macros like the following:

`/cast Overpower`
`/cast Execute`
`/cast Mortal Strike`
`/cast Sunder Armor`

**Macros like this do not work anymore**. As soon as Overpower fails to cast, the game will block all the other spells from casting as well, even though the GCD is not actually triggered.

There is a bit of good news, though. Certain spells *can* actually be cast at the same time in a single macro. Any spell that is **instant and does *not* trigger the GCD** can be followed by another cast ("Next Melee" abilities like Heroic Strike fall under this category too). The spell's tooltip will tell you if it's instant, but you have to use the spell (or check a spell database site like thottbot.com) to know if it triggers the GCD.

Prior to patch 2.3 it was necessary to place a /stopcasting command after the instant, non-GCD spells (but not items). The game engine assumed that after the first /cast is attempted, a spell is now in progress. /stopcasting removes this assumption and prevents the "Another action is in progress" error. Since the spell is instant, /stopcasting does not actually cancel the cast. Example:

`/cast Furious Howl`
`/stopcasting`
`/cast Blood Fury`
`/stopcasting`
`/cast Call of the Wild`

Note that since patch 2.3, this is no longer necessary. The above macro can be shortened to:

`/cast Furious Howl`
`/cast Blood Fury`
`/cast Call of the Wild`

Targeting
---------

Targeting is another common task in macros. This is accomplished either by using dedicated targeting slash commands which actually change your target or by using the \[@*unit*\] macro option on commands that accept them. When you use the macro option, you are actually casting the spell or using the item directly on the unit without changing targets. Macro options will be covered in great detail in Part II. For now, here's how to use the targeting commands.

A shotcut of `/target` is `/tar` so (`/target` ... = `/tar` ...).

The most basic targeting command (unsurprisingly) is /target. Its use is as simple as

`/target Cogwheel`

/target does a closest match which means if you do /target Cog and someone is standing near you (and no one named Cog is) it will target that someone named "Cogwheel". This is a plus or a minus depending on your situation. Unfortunately, it will also target irrelevant units (like corpses). This makes macros like the following much less useful than they might first appear.

`/target Blackwing Mage`
`/cast Curse of Agony`

If no Blackwing Mages are around, this might target someone in your raid who happens to have the letters B and L in their name. While they're safe from the wrath of your curse, it's still a bit disconcerting. Another problem is that it may target something 100 yards behind you that you don't really care about. (Patch 2.3 added the [/targetexact](#targetexact "wikilink") command to eliminate part of the problem.)

In addition to specifying the name of someone you would like to target, you can also provide a unit ID. Unit IDs are a way to identify a particular character, mob, NPC, etc. For instance, your current target can always be accessed by the "target" unit ID (obviously not the most useful for the command we're discussing at the moment :P). You yourself are accessed by the "player" ID, and if you have a pet it would be referenced by "pet." You can also append "target" to the end of any valid unit ID to arrive at that unit's target. There is a joke about Kevin Bacon involving a macro like:

`/target targettargettargettargettargettarget`

[UnitId](UnitId "wikilink") has a full list of allowed IDs.

### Other targeting commands

Here is a brief overview of the other targeting commands:

#### /assist

By itself, assist targets your target's target (e.g. if you are targeting someone, and that someone is targeting Iriel, /assist would make you target Iriel). You can also provide a name or unit to /assist and you will assist the specified entity:

`/assist Cogwheel`

There is an interface option which will automatically start you attacking if you end up with a hostile target.

#### /cleartarget

Leaves you with no target

#### /targetexact

Targets a unit with the exact name listed. If the name is spelled wrong or that unit is not near you, your target will not be changed.

#### /targetlasttarget, /targetlastfriend, /targetlastenemy

As the names suggest, these commands will target your previous target, your last targeted friend, or your last targeted enemy. If you previously had no target, this command will do nothing.

#### /targetenemy, /targetfriend

These commands cycle through the specified type of unit. /targetenemy is like pressing TAB, and /targetfriend is like pressing CTRL-TAB. You can also add a parameter of 1 which reverses the direction of the cycle (/targetenemy 1 is like pressing SHIFT-TAB).

**Note:** You can only use these commands **once per macro**.

`/targetenemy`
`/targetenemy 1`

`/targetfriend`
`/targetfriend 1`

#### /targetenemyplayer, /targetfriendplayer

These commands cycle through the specified type of player controlled units. They behave just like /targetfriend and /targetenemy except they will only target other players, ingnoring computer controlled units like NPC's mobs, pets, minions, creations, etc. They're mostly useful for PvP. Like /targetenemy, you can add a 1 to reverse the direction.

`/targetenemyplayer`
`/targetenemyplayer 1`

`/targetfriendplayer`
`/targetfriendplayer 1`

**Note:** You can only use these commands **once per macro**.

#### /targetparty, /targetraid

Cycles through your nearest party or raid members. Like /targetenemy, you can add a 1 to reverse the direction.

`/targetparty`
`/targetparty 1`

`/targetraid`
`/targetraid 1`

Pet control
-----------

As mentioned in the spell casting section, you can use /cast to cast your pet's abilities by name. In fact, Blizzard had to change the name of the Mage elemental's Frost Nova to Freeze because there was no way to use it in a macro. :P But as everyone with a pet is aware, that's nowhere near the end of the line for pet control. Luckily the Burning Crusade patches brought us a host of new pet commands:

### /petattack

Sends your pet to attack your target. You can also specify a name or unit ID and your pet will attack that instead.

### /petfollow

Causes your pet to follow you, cancelling its attack if necessary.

### /petstay

Causes your pet to hold at its current location until given another command.

### /petmoveto

Causes your pet to stay at a specified location.

### /petpassive, /petdefensive, /petassist

Sets the reaction mode of your pet just like the buttons on your pet bar.

### /petautocaston, /petautocastoff, /petautocasttoggle

These commands manipulate the auto-cast of a given pet spell. The first will always turn auto-cast on, and the second will turn it off. Example:

`/petautocaston Torment`
`/petautocastoff Suffering  `

Recently, a new command has been added which will toggle a pet's auto-cast spells, petautocasttoggle. Example:

`/petautocasttoggle Fire Breath`

This will turn the auto-cast on if it is currently off, or off if it is current on, which can entirely replace the former command depending on the planned use.

Controlling Feedback and Question mark icon (<img src="INV Misc QuestionMark.png" title="fig:" alt="" width="15" />) with \#show
--------------------------------------------------------------------------------------------------------------------------------

By default, WoW uses the first spell or item that appears in a macro to show [cooldown](cooldown "wikilink"), range, and availability feedback on the button, and to pick which icon to display when you use the question mark icon. Take our multi-spell macro from earlier as an example:

`/use Talisman of Ephemeral Power`
`/cast Arcane Power`
`/cast Presence of Mind`
`/cast Pyroblast`

With this macro, WoW chooses Arcane Power for the feedback. However, this is probably not what you really want. The main point of this spell is to cast Pyroblast. The first few lines merely exist as support spells to make the Pyroblast more effective. You can make the button behave as if Pyroblast were the first spell by adding the following line to the top of the macro:

`#show Pyroblast`

If you used the question mark icon for the macro, the button will even have the icon of Pyroblast without any extra effort on your part. The parameter to \#show (in this case Pyroblast) works the same way as the /cast and /use commands. You can use a spell name, item name, item id (item:12345), inventory slot, or bag and slot numbers. (only the first ability will be used since warlords of draenor)

Similar to \#show is \#showtooltip. Normally when you mouse over a macro on an action bar, your tooltip displays the name of the macro. This is not incredibly useful most of the time (especially if you use an AddOn like TheoryCraft to give you detailed spell information in tooltips). However, the \#showtooltip command allows you to specify a spell to use in the tooltip the same way as \#show. If you use \#showtooltip, you do not need to use \#show.

If you're happy with the spell that WoW is choosing for the feedback, you can use \#showtooltip without a spell to save space in your macro. WoW will still use whichever spell it was choosing before, but it will now show the tooltip info for that spell/item.

You cannot use \#show and \#showtooltip in the same macro, the second one will be ignored.

**Please Note:** unlike slash commands, \#show and \#showtooltip must be written in lower case letters.

### Conditionals for \#show(tooltip)

The \#showtooltip and \#show commands will also accept the [conditionals](HOWTO:_Make_a_Macro#Conditionals "wikilink") found further below. Here's a simple example:

`#showtooltip [modifier:shift] Conjure Food; Conjure Water`

This line at the top of the macro will show icon and tooltip corresponding to the Conjure Water spell, unless shift is held down, in which case Conjure Food will be used instead, regardless of what else the macro is doing and which spells it is using.

Other slash commands
--------------------

Now that you have a solid foundation, let's cover some of the other slash commands at your disposal. Some of these commands may seem a bit pointless at first glance, but when you combine them with the macro options from Part II, they can perform some neat tricks.

### Equipping items

There are three commands for equipping items: /equip, /equipslot, and /equipset. /equip simply takes an item name and will equip it to the default slot as if you had right-clicked it in one of your bags (i.e., a one-handed weapon will be equipped to your main hand). /equipslot takes an [inventory slot ID](InventorySlotId "wikilink") and an item name, and equips the item to the specified slot. Note that when using /equipslot, you must respecify the slot for each set of conditionals. If you use the Blizzard equipment manager and save an equipment set, you can use the /equipset command to use it. Examples:

Equip a weapon to default slot:

`/equip Honed Voidaxe`

Equip a trinket to the lower trinket slot:

`/equipslot 14 Carrot on a Stick`

Save two equipment sets. One called Tank that has a sword and shield equipped, one called DPS that has a two handed weapon equipped. Use this macro to switch between the two:

`/equipset [equipped:Shields] DPS; Tank`

If you have a shield on, it'll equip your saved DPS set, otherwise it'll equip your saved Tank set.

Swap between your offhand and a shield:

`/equipslot [equipped:Shields] 17 Merciless Gladiator's Cleaver; 17 Crest of the Sha'tar`

**Note:** If you are trying to equip two of the same weapon simultaneously into different slots, your macro will not work properly.

**Note:** AddOns are allowed to use the equipping functions directly, even during combat. By the same mechanism, you can use the equipping slash commands with AddOns like AfterCast or Chronos. You might have some trouble if the AddOn first checks whether the command is secure; the equipping commands are in the secure command list, though they aren't inherently secure.

### Sequencing spells and items

Many times you will find yourself casting a series of spells or use certain items in the same order on pretty much any mob you fight. To make this job a bit easier, we have the /castsequence command. /castsequence takes a list of spells and/or items separated by commas. These follow the same rules as /cast and /use. This means you can interchange spell names, item names, item IDs, inventory slots, and bag slot combinations. Each time you run the macro, it activates the current spell/item. If the spell or item is used successfully, the sequence will move to the next entry. **You must repeatedly activate the macro to use all the spells in the sequence**. Once you use the last entry in the list, it will reset to the beginning. Example:

`/castsequence Immolate, Corruption, Curse of Agony, Siphon Life`

This might be something you would use for a Warlock's opening attack. Note, however, that if Immolate fails to cast for some reason (out of mana, not in range, silenced, etc.), the sequence will remain at that point. Because of this, you cannot use a /castsequence to make a spammable macro like:

`/castsequence Overpower, Execute, Mortal Strike`

Before the spell list (**but always *after* the conditionals**), you can also specify reset conditions to start the sequence over before it reaches the end. The basic syntax for reset conditions is:

`reset=`*`n`*`/target/combat/shift/alt/ctrl`

Where *n* is the number of seconds of inactivity after which the macro should be reset. In other words, if more than *n* seconds pass without the macro being called, then the next time you call it the sequence will start from the first spell. Note that this is not the time since the *first* spell in the sequence was cast, but rather the time since the macro was last called (to cast *any* of the spells in the sequence). This is a very important distinction because it means **you cannot use a reset timer to account for [cooldown](cooldown "wikilink")**.

As to the other conditions, "target" resets the sequence when you change targets; "combat" when you leave combat; "shift", "alt", and "ctrl" when you activate the macro with one of those keys depressed. You can specify any number of these conditions separated by slashes as shown.

Example:

`/castsequence reset=10/shift Spell 1, Other Spell, Some Item`

To make a macro cycle through two different 'sets' of spells that should be used together, where each set can not be used at the same time (i.e trinkets with shared [cooldowns](cooldown "wikilink")) it is possible to use multiple instances of /castsequence to achieve this effect.

Example:

`/castsequence Beserking, Icy Veins`
`/castsequence Trinket 1, Trinket 2`

On the first button push this macro will cast Beserking and Trinket 1, on the second it will cast Icy Veins and Trinket 2.

If you used the question mark icon, WoW will automatically update the icon to the current element of the sequence. If you have other /casts or /uses (or complex conditionals) before the /castsequence, though, WoW will sometimes not be able to figure out which icon to use. In this case, you can specify the icon using \#showtooltip as described above

### Random spells and items

One of the most common requests on this forum is for a macro to use a random mount. This is extremely trivial thanks to the addition of /castrandom and /userandom. Like /castsequence, /castrandom and /userandom takes a list of spells and/or items separated by commas and picks one at random when you run the command. Example:

`/castrandom Swift Green Mechanostrider, Black Battlestrider, Summon Dreadsteed `

### Attacking

Change your target to *unit* and start auto-attacking.

`/startattack Cogwheel`

Stop auto-attacking.

`/stopattack`

### Action bar manipulation

There are two commands that allow you to change action bar pages: /changeactionbar and /swapactionbar. /changeactionbar takes a single number and will always switch to that page. One use of this is for hunters to emulate stances by having a pair of macros like:

`/cast Aspect of the Hawk`
`/changeactionbar 1`

and

`/cast Aspect of the Monkey`
`/changeactionbar 2`

/swapactionbar takes two page numbers and will swap between them each time it runs. If you're on a page other than one of the two specified, it will be change to the first of the two.

`/swapactionbar 1 2`

### Removing buffs

The /cancelaura command allows you to remove unwanted buffs. For example, a Death Knight without the Horn of Winter minor glyph cannot cast Horn of Winter if a glyphed version of the buff is already on them (from another Death Knight). The following macro solves this problem:

`/cancelaura Horn of Winter`
`/cast Horn of Winter`

### Leaving a form

With the exception of Warriors, any class with stances (Druids, Priests with [Shadowform](Shadowform "wikilink"), Rogues with [Stealth](Stealth "wikilink"), etc.) can use /cancelform to leave their current form. Example:

`/cancelform`
`/use Super Healing Potion`

In patch 2.3, /cancelform will be recognized instantly **for Druids**. Until then and for everyone else, you may have to click the button twice.

### Stopping a cast

/stopcasting was touched on briefly in other contexts but its main use, as you might guess, is used to stop another spell cast that's in progress. This is useful for making "panic buttons" that interrupt whatever you're doing at the moment in favor of something more important. On a Warlock, for instance, you can use the following macro:

`/stopcasting`
`/cast Shadowburn`

### Halting a macro early

/stopmacro is one of those commands that doesn't really come into its own unless you use it with macro options. Its main use is to implement "fall-through" logic to prevent you from continuing a macro if certain conditions are true. See "Using focus" at the end of part II for an example.

### Dismounting

`/dismount`

Basically self-explanatory.

### Saving a target for later action

The /focus command allows you to save a target to come back to later. For example, say your raid leader assigns you a target to sheep. First, select that mob, and type /focus. Now you can use a macro like the following to cast sheep on your focus:

`/cast [@focus] Polymorph`

Note that this is not the most efficient use of the focus feature. See "Using Focus" towards the end of Part II for a much more in-depth look at this mechanic.

### Simulating button clicks

The /click command takes the name of a button and acts like you clicked the button with your mouse. By default, it behaves like a left-click, but you can specify other mouse buttons in the command. There are a few ways to determine the name of the frame you're interested in:

-   You can use an AddOn. Some AddOns, including MoveAnything, give you a way to see the name of the frame underneath your mouse.
-   You can look through the UI code for the frame. This is really only applicable to people who are comfortable with AddOn programming.
-   You can bind the following macro by a key and then run it while your mouse over the frame in question:

`/run local f = GetMouseFocus(); if f then DEFAULT_CHAT_FRAME:AddMessage(f:GetName()) end`

/click can be used for many different purposes. You can chain together multiple macros by /click'ing buttons with other macros on them. For example, you might have a really long macro that doesn't fit into 255 characters. Put as much of it as you can in one macro and end it with the following line:

`/click MultiBarRightButton1`

The rest of the code would go into a new macro that you would then place on MultiBarRightButton1 (the first button of the right-hand vertical extra action bar).

You can also do things that normally wouldn't be available to macros. For instance, turning on auto-cast for a pet spell can't be done by Lua scripts and there isn't a secure command for it (until the next patch, at least). However, you can write a macro to pretend that you right-clicked on one of your pet bar buttons:

`/click PetActionButton5 RightButton`

This command will act like you right-clicked the 5th pet button from the left. The extra button parameter can also be LeftButton (the default), MiddleButton, Button4, or Button5.

On top of these uses, there are some more complex examples of /click branching towards the end of Part II.

#### Action bar button names

As shown above, MultiBarRightButton1 refers to the first button of the right-hand vertical extra action bar. MultiBarRightButton2 refers to the second button, and so on. Names for buttons on each of the standard action bars are as follows, replacing the *\#* with an appropriate number:

`ActionButton`*`#`*`                Main Bar*`
`BonusActionButton`*`#`*`           Dynamic bar that switches actions based on Druid Forms, Warrior Stances, and Rogue Stealth*`
`MultiBarBottomLeftButton`*`#`*`    Bottom Left Bar`
`MultiBarBottomRightButton`*`#`*`   Bottom Right Bar`
`MultiBarRightButton`*`#`*`         Right Bar`
`MultiBarLeftButton`*`#`*`          Right Bar 2 (to the left of "Right Bar")`
`PetActionButton`*`#`*`             Pet Bar`
`ShapeshiftButton`*`#`*`            Druid Forms, Paladin Auras, Warrior Stances, Death Knight Presences, Rogue Stealth, Hunter Aspects`
`ExtraActionButton`*`#`*`           Extra Action Button for fights like Ultraxion.`

\* The BonusActionBarFrame frame replaces the ActionBarFrame frame for all Druids, Warriors, Shadow Priests and Rogues and `/click` `ActionButton`*`#`* and `/click` `BonusActionButton`*`#`* do the same thing for these classes.

Advanced Scripting
------------------

### What scripts *can't* do

Scripts are very powerful tools that can make complex decisions based on a number of criteria. Because of this power, Blizzard has limited the types of things we're allowed to do with them in order to keep macros and AddOns from taking actions that should be controlled by the player. This section starts with what you can't do because you shouldn't to get your hopes up. While scripts do remain useful for quite a few purposes, you **cannot use them to cast spells, use items, change your action bar page or affect your target in any way**. You are limited to using the "secure" commands already shown for those tasks.

### Scripting

The WoW UI is controlled by code written with the Lua scripting language. You can take advantage of this scripting system in a macro with the /run command (equivalent to /script--I use /run to save a few characters). The whole script must be on one line, though you can have multiple /run commands in a single macro.

A full treatment of Lua and programming in general is well beyond the scope of this document. However, if you have some programming experience, you should head over to [Lua.org](http://www.lua.org/pil/) to learn the basics of Lua and if you don't have any programming experience, you may want to check out [LearnToProgram](http://pine.fm/LearnToProgram/) to get a foundation of the concepts used in scripts.

Blizzard provides many functions (called the API) which the Lua scripts can use to control the UI. You can view the API and other features of the UI system over at [Interface Customization](Interface_Customization "wikilink") (if you spend any considerable time with scripts and/or AddOns, WoWWiki will be indispensable). All the details of the UI environment can't be covered here, so some favorite scripts will be presented as an example. See the previously linked references and the [old Mod author resources sticky](https://web.archive.org/web/20100429142618/http://forums.worldofwarcraft.com/thread.html?topicId=11381244&sid=1)[1] for more information.

The following macro (on which CCWarn AddOn is based on) will whisper everyone in your raid to change their targets if they have the same target as you. This is to help keep them from breaking the sheep that this macro casts as well.

`/cast Polymorph`
`/run for i=1,GetNumRaidMembers()-1 do local u,t="raid"..i,"target"if UnitIsUnit(u..t,t)then SendChatMessage("Change targets! Trying to sheep...","WHISPER",nil,UnitName(u))end end`

There are two reasons that it looks as obfuscated as that. First, there is the 255 character limit (though there is a workaround in Part III); you often need to take certain shortcuts in order to get a script to fit in a macro. Second, you have to keep the entire script on one line. Under more ideal circumstances, that code would look more like:

`for i = 1, GetNumRaidMembers() - 1 do`
`    local unit = "raid"..i`
`    if UnitIsUnit(unit.."target", "target") then`
`        SendChatMessage("Change targets! Trying to sheep...", "WHISPER", nil, UnitName(unit))`
`    end`
`end`

Macro options
-------------

Macro options are a way to control actions based on various pieces of information. To dive right into an example, the following macro will cast Renew on a friendly target and Shadow Word: Pain on a hostile one.

`/cast [help] Renew; [harm] Shadow Word: Pain`

When you run this macro, the \[help\] condition is checked. This determines whether your target is someone you can cast beneficial spells on. If the \[help\] is true, it then casts Renew and the macro moves to the next line. Otherwise (either you have no target, or you can't cast a helpful spell on your target), it falls through to the next clause. Now it checks for the \[harm\] condition. \[harm\] is just like \[help\] but for offensive spells. If true, it casts Shadow Word: Pain. If it isn't true (no target or you can't harm your target) then it does nothing because there are no more clauses.

Note: The \[harm\] check out could have been left and it would have functioned in much the same way. However, if you have no target or your target can be neither helped nor harmed, you would receive an error message or, depending on the spell, the target selector cursor.

The macro will now search for the selected target. If the target is \[help\] then it will use its helpful spell. If the target is \[harm\] then it will use its harmful spell. But nothing will happen when you havent selected any target. Not even when you have "Selfcast" enabled in the interface options. but with the following macro it will use selfcast when nothing is selected.

`#showtooltip`
`/cast [help] Healing Touch; [harm] Wrath else `
`/cast [@player] Healing Touch`

It is important to note that this macro will not cast Renew or Shadow Word: Pain on your focus target if you use it while holding the focus cast key (alt by default). However, the focus cast key will always return false when used in a macro conditional. To get around that, you have two options. First, you could unbind your focus cast key and make a macro using that key for every spell you would ever want to cast on a focus. Or, you could take the much more efficient route and just use a different modifier. The following example uses

`#showtooltip`
`/cast [mod:ctrl, target=focus, help] Renew else`
`/cast [mod:ctrl, target=focus, harm] Shadow Word: Pain else`
`/cast [harm] Shadow Word: Pain; [help] Renew else`
`/cast [@player] Renew`

This macro will effectively function as if you had Renew and Shadow Word: Pain bound to the same key, and it will cast whichever is applicable. The first line checks if the control key is held, and if it is, casts Renew at your friendly focus or Shadow Word: Pain at your harmful focus. (Note that the control key must be used here by default if this macro is bound to a number from 1-6 because Shift+1 through Shift+6 switches action bars, and alt is the focus cast key. If either of those are unbound, then shift and alt will work just as well). The third line checks if your target is hostile or helpful and casts Shadow Word: Pain or Renew accordingly. The last line casts Renew on yourself if none of the other conditions are met.

In short, this is a sample macro, using boolean (true/false) conditions A, B, C, and D, and spells 1, 2, and 3, that shows how logical conditions work.

`#showtooltip`
`/cast [A, B] [C] Spell 1; [D] Spell 2; Spell 3`

This macro checks conditions in the following order:

1) Are A and B both true? If so, cast spell 1.

2) Is C true? If so, cast spell 1.

3) Is D true? If so cast spell 2.

4) If none of the above are true, cast spell 3.

Commands that accept options
----------------------------

Only the "secure" commands respond to macro options. In fact, the secure commands are the reason macro options were created in the first place. Insecure commands like chatting, emotes, etc. can be scripted using Lua and the /run command. Furthermore, Blizzard didn't want to confuse people who use semicolons in their chat messages. If /say could use macro options, the following would always just say "Hello":

`/say Hello; I'm a n00b`

The following is a list of all the secure commands currently available in WoW:

-   1.  show \*
-   1.  showtooltip \*
-   /assist
-   /cancelaura
-   /cancelform
-   /cast
-   /castrandom
-   /castsequence
-   /changeactionbar
-   /clearfocus
-   /cleartarget
-   /click
-   /dismount
-   /equip +
-   /equipslot +
-   /equipset +
-   /focus
-   /petagressive
-   /petattack
-   /petautocastoff
-   /petautocaston
-   /petdefensive
-   /petfollow
-   /petpassive
-   /petstay
-   /startattack
-   /stopattack
-   /stopcasting
-   /stopmacro
-   /swapactionbar
-   /target
-   /targetenemy
-   /targetenemyplayer
-   /targetfriend
-   /targetlasttarget
-   /targetparty
-   /targetraid
-   /use
-   /usetalents +
-   /userandom

\* \#show and \#showtooltip are not technically secure commands, but they operate with macro options just like /use and /cast.

+ /equip, /equipslot, /equipset and /usetalents are not technically secure since their functionality is available to AddOns and macro scripts.

If you would like a way to use macro options for insecure commands, there are AddOns that provide such capability. The AddOn, [MacroTalk](http://www.wowinterface.com/downloads/info6853-MacroTalk.html), adds a number of /opt\_\_\_ commands for each chat command and a generic /opt command that lets you use options to choose other full (insecure) slash commands.The newest SuperMacro may provide this functionality as well. [Macro Broker](http://www.wowinterface.com/downloads/info12573-MacroBroker.html) provides this as well through a new command, /eval.

==\[@*unit*\] (previously \[target=*unit*\])== In addition to condition checking, the macro option system provides us with a way to set the target of various actions. For example, the following macro will always use the bandages on yourself (self-cast) regardless of your target:

`/use [@player] Heavy Netherweave Bandage`

This can be helpful for those that prefer not to utilize the UI's **Auto Self Cast** feature under **Main Menu**\\**[Interface](Interface "wikilink")**\\*Combat*.

(You can also use \[target=player\], however the \[@player\] format is preferred because it uses fewer characters.)

Besides setting the target of the action itself, the \[@unit\] assignment also sets the unit that the conditionals are checked against. Since that probably didn't make much sense, here's a macro that combines concepts from both of the examples you've seen so far:

`/cast [help] [@targettarget, help] [@player] Flash Heal`

First it checks against \[help\]. If it's true, then it passes Flash Heal to /cast. Otherwise it moves on to the next condition, \[@targettarget, help\]. Now it checks for help again, but this time it's checking to see if your target's target is friendly. If it is, then it will pass Flash Heal to /cast, but this time it also tells /cast that it should be cast on your target's target. If it still hasn't found a valid target yet, it'll move onto the next condition, \[@player\]. Since there are no actual conditions in there, it will always be true, so Flash Heal is sent to /cast with you, the player, as the target.

Syntax overview
---------------

There can be an awful lot of confusion around how macro options work, so this will be an early opportunity to break down the general concepts behind them. There will be some real-world examples using actual options. Don't worry too much if you don't understand what they mean. All options will be covered in detail later on.

### General options syntax

All slash commands basically work the same way. You have a command, and a set of parameters. The parameters depend on the command, and some commands don't take any. Here are a few examples:

`/cast Smite`
`\___/ \___/`
`  |     |`
`  |  parameters`
`  |`
`command`
`/petattack`
`\________/ \_/`
`    |       |`
`    |   parameters (empty)`
`    |`
`command`
`/castsequence reset=target Immolate, Corruption, Curse of Agony, Siphon Life`
`\___________/ \____________________________________________________________/`
`      |                                    |`
`   command                            parameters`

Macro options allow you to choose a set of parameters based on a number of criteria. At the highest level, you have a set of criteria/parameter groups separated by semicolons. The semicolons can be seen as an "else" or an "else if." The criteria consist of zero or more sets of conditions. Each condition set is enclosed with square brackets. Here is an illustration of this basic syntax.

`/command [conditions] [more conditions] parameters; [conditions] parameters ...`

As you saw in the basic examples above, the command is evaluated from left to right. As soon as it finds a set of conditions that are true, it runs the command with the corresponding parameters. If there are no conditions in a clause, it will always be true. In fact, you can imagine a single-spell /cast command as a macro option with one clause that has no conditions. When the command does not have any conditions that are true, it will not execute at all.

### Condition syntax

Each set of conditions is a simple comma-separated list. They can appear in any order, though \[target=\] is always taken into account first, before any of the conditionals. Think of the comma as an "and." A condition like \[help, nodead, target=focus\] means "My focus is friendly AND not dead."

**Notice:** Conditions are case-sensitive. If you use \[Help\] instead of \[help\], the macro will generate an error. However, this does not necessarily include the condition's parameters (described below). Still, it's usually better to consistently capitalize as things appear. Write spells and items just like you see in their tooltips. Follow the examples in this guide precisely.

Conditions themselves have a few building blocks. First off, as you just saw with "nodead", you can put "no" in front of a condition to mean the opposite. Notice that \[nohelp\] does not mean the same thing as \[harm\]. \[harm\] and \[help\] both return true only if there is a target to begin with. Furthermore, there are some targets that can neither be helped nor harmed (unflagged players of the other faction, non-combat pets, escort quests, etc.).

Some conditions also take their own sets of parameters. For example, \[stance\] by itself means "In any stance" (useful for every class with stances except Warriors since they are always in a stance). However, you can also specify one or more particular stances to check. The set of parameters begins with a colon (:) and each parameter is separated with a slash (/) that means "or." Here's a generic illustration of the syntax of a single condition where everything inside angle brackets (&lt;&gt;) is optional.

`[<no>condition<:parameter</parameter</parameter<...>>>>]`

Here's a simple example that uses Shield Bash in Defensive or Battle Stance, but switches into Defensive Stance if you're in Berserker:

`/cast [stance:1/2] Shield Bash; Defensive Stance`

This can be simplified to pseudo-code English as "IF currently in stance 1 OR in stance 2 then use Shield Bash ELSE switch to Defensive Stance.

Note: "no" applies to the whole condition and all of its parameters. This means that \[nostance:1/2\] would mean "anything but stances 1 or 2"

### Complete EBNF syntax

For those who are familiar with EBNF notation, the entire macro option syntax can be represented as follows:

`command = "/", command-verb, [ {command-object, ";" } command-object] ]`
`command-verb = ? any secure command word ?`
`command-object = { condition } parameters`
`parameters = ? anything which may be passed to the command word ?`
`condition = "[" condition-phrase { "," condition-phrase } "]"`
`condition-phrase = ([ "no" ], option-word, [ ":" option-argument { "/" option-argument } ]`
`                   | "target=", target)`
`option-argument = ? any one-word option, such as 'shift, 'ctrl', 'target', '1', '2' ?`
`target = ? a target pattern ?`

### Empty parameters

One source of confusion comes in dealing with parameterless commands. A very common error when writing macros is to add an extra semicolon to the end, but this creates some unexpected bugs. Take the following macro:

`/petattack [@focus, harm];`

To the uninitiated, that looks like it'll send your pet after your focus if it's harmful, and do nothing otherwise. However, let's look at a breakdown of this macro:

```
/petattack [@focus, harm]  ;
\________/ \____________/ V V V
    |               |     | | |
 command         options  | | parameters (empty)
                          | |
                          | options (empty)
                          |
                          parameters (empty)
```

See that extra blank set of options and parameters? Remember that a blank set of options always evaluates to true, so that second empty parameter gets passed to /petattack if the first conditions are false.

### Empty conditions

Sometimes you may want a command to cast on a particular target under certain circumstances but behave like normal if those conditions aren't true. In this case you will want to use an empty set of conditions which will always evaluate to true. The following macro will cast Flash of Light on the unit under your mouse. If you have no mouseover or it's hostile, the macro will behave like a plain /cast Flash of Light, casting on your target and respecting self-cast key and auto-self-cast interface option.

`/cast [@mouseover, help] [ ] Flash of Light`

===\[target=\] or \[@\] versus unit parameters=== Some commands accept units directly as their parameters. For example, /target party1 will target your first party member. The command /target \[@party1\] while a bit more verbose has the equivalent behavior. However, in most cases the designers don't want us to be able to test conditions on one unit and then act on another, so you must use one or the other. E.g., a macro like the following will not work as expected:

`/target [@focus, dead] party1`

WoW will ignore party1 because you set a unit with the \[@\] targeting option. There are some specific exceptions to this rule. A few commands have "key units" that are fundamental to the command. If you use that unit in your \[@\] option, WoW will allow you to specify another unit or will use the default unit for the command if you don't specify one. That last bit needs a concrete example:

`/focus [@focus, dead] [@focus, noharm] target`

In this case, the key unit is focus. Since we are using \[@focus\], WoW will send "focus" to the /focus command. We could also have left off the "target" at the end since the /focus command defaults to your target. Below is a list of all commands with key units, and their default units if any. To reiterate for clarity, the key unit is a unit you can use in \[@\] option that will allow you to send another unit to the command. The Default Unit is the unit that will be sent to the command if you don't provide one.

|Command      | Key Unit  | Default Unit|
|   ------------- ----------- -------------|
|   /target      | target    ||
|   /focus       | focus     | target|
|   /startattack | target    | target|
|   /petattack   | pettarget | target|

Conditionals
------------

Now you'll get to see the complete list of conditionals and what they mean. Each conditional will be treated more thoroughly below.

### Complete list

Below is the entire list of conditionals that are available to the macro system. One of the goals in the 2.0 patch was to eliminate a lot of old "smart buttons" that allowed people to essentially play the entire game spamming one key repeatedly. However, many tasks people used macros to simplify were deemed OK and given Blizzard's blessing via the macro options.

If you don't see a condition listed here, then there is no way to check for it and take a combat-related action. These are essentially non-negotiable though they may be augmented in the future.

Many of these can be checked for falseness instead of trueness. For example, \[nocombat\] is a valid conditional and will only perform the actions following it if you are not in combat.

-   **actionbar:1/.../6** or **bar:1/.../6** — Given action bar page is selected
-   **bonusbar:5** — The possess bar is active (controlling a vehicle or another player)
-   **button:1/.../5/*&lt;virtual click&gt;*** or **btn:1/.../5/*&lt;virtual click&gt;*** — Macro activated with the given mouse button
-   **channeling:*&lt;spell name&gt;*** — Channeling the given spell
-   **combat** — In combat
-   **cursor** — What the cursor is currently holding, see [API\_GetCursorInfo](API_GetCursorInfo "wikilink") for types
-   **dead** — Target is dead
-   **equipped:*&lt;item type&gt;*** or **worn:*&lt;item type&gt;*** — item type is equipped (item type can be an inventory slot, [item type](ItemType "wikilink"), or item subtype)
-   **exists** — Target exists
-   **flyable** — In a zone where flying is allowed (this does not check if you have [Cold Weather Flying](Cold_Weather_Flying "wikilink"); if you are in a flyable zone, but do not have this skill, the macro fails)
-   **flying** — Mounted or in flight form AND in the air
-   **group:party/raid** — You are in the given type of group
-   **harm** — Can cast harmful spells on the target
-   **help** — Can cast helpful spells on the target
-   **indoors** — Self explanatory
-   **modifier:shift/ctrl/alt** or **mod:shift/ctrl/alt** — Holding the given key
-   **mounted** — Self explanatory
-   **outdoors** — Self explanatory
-   **party** — Target is in your party
-   **pet:*&lt;pet name or type&gt;*** — The given pet is out
-   **raid** — Target is in your raid/party
-   **spec:1/2** — Currently active class specialization
-   **[stance](Stance "wikilink"):0/1/2/.../n** or **form:0/.../n** — In a stance
-   **stealth** — Stealthed
-   **swimming** — Self explanatory
-   **talent:&lt;*tier\#*&gt;/&lt;*column\#*&gt;** - talent from column\# of tier\# is selected
-   **unithasvehicleui** — The target of the macro has vehicle UI
-   **vehicleui** — The player has vehicle UI

### help and harm

The \[help\] condition is true when the unit can receive a beneficial effect, e.g., a healing spell. The \[harm\] condition is true when the unit would get an adverse effect, e.g., a damaging spell.

### exists

This determines whether the given unit exists. In other words, if you don't have a target, \[exists\] will return false. If you have a focus, \[target=focus, exists\] would be true. Note that in some cases \[exists\] is unnecessary. \[help\], \[harm\], \[dead\], \[party\], and \[raid\] all imply \[exists\] if they're true.

### dead

If you have a target and it's dead, this will be true.

### stance and form

  
stance:0/1/2/.../n or form:0/1/2/.../n

Stance is the generic term used for Warriors', Druids', Rogues' (Stealth), Priests' (Shadowform) and Shaman's (Ghost Wolf) forms. Stances are only applicable to situations where certain abilities are only usable in specific forms. Because of this, Paladin auras and Death Knight presences (despite being on the shapeshift bar), and Hunter aspects are NOT considered stances.

The simplest form of \[stance\], as mentioned previously, means that you are in any stance whatsoever. It is equivalent to \[stance:1/2/3/.../n\] where n is the number of stances you have. \[stance:0\] is equivalent to \[nostance\] so you can use a conditional like \[stance:0/3\] to evaluate as true if you are either in stance 3 or not in any stance.

Form is an alias for stance. The condition \[form:1\] will work exactly the same as \[stance:1\].

The stances themselves are ordered the same way as they appear on your shapeshift bar. So a Druid with Bear, Aquatic, Cat, and Travel forms would have stances 1 through 4. Here is a simple chart to help you remember stance numbers:

|          | Warrior                                  | Druid                                                                                                                     | Priest                                                  | Rogue                                   | Shaman                              | Warlock                                      |
|----------|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|-----------------------------------------|-------------------------------------|----------------------------------------------|
| Stance 1 | [Battle](Battle_Stance "wikilink")       | [Bear](Bear_Form "wikilink")                                                                                              | [Shadowform](Shadowform "wikilink") or                  
                                                                                                                                                                                   [Spirit of Redemption](Spirit_of_Redemption "wikilink")  | [Stealth](Stealth "wikilink")           | [Ghost Wolf](Ghost_Wolf "wikilink") | <s>[Demon Form](Metamorphosis "wikilink")<s> |
| Stance 2 | [Defensive](Defensive_Stance "wikilink") | [Cat](Cat_Form "wikilink")                                                                                                |                                                         | [Shadow Dance](Shadow_Dance "wikilink") | |                                   |                                              |
| Stance 3 | [Berserker](Berserker_Stance "wikilink") | [Travel](Travel_Form "wikilink") (includes [Aquatic](Aquatic_Form "wikilink") and [Flight](Flight_Form "wikilink") forms) | |                                                       |                                         |                                     |                                              |
| Stance 4 |                                          | [Moonkin](Moonkin_Form "wikilink")                                                                                        |                                                         |                                         |                                     |                                              |
| Stance 5 |                                          |                                                                                                                           |                                                         |                                         |                                     |                                              |
| Stance 6 |                                          |                                                                                                                           |                                                         |                                         |                                     |                                              |

Note: If a Druid is missing a form, all the higher-number ones will be shifted upwards on the chart. Also, Tree of Life does not have the word "Form".

If the player is using Glyph of the Stag and/or Tree of Life, this table will not be accurate.

Note: If a priest has both Shadowform and Spirit of Redemption, Stance 2 is Spirit of Redemption.

Example:

`/cancelform [noform:1/3]`
`/cast [form:1/3] Faerie Fire (Feral)(); [noform] Faerie Fire`

In Bear and Cat forms, this will cast Faerie Fire (Feral). In caster form, it will cast Faerie Fire. In any other stance, running the macro will return you to caster form. Note that after patch 2.3, /cancelform will register instantly so it will immediately cast Faerie Fire after leaving a form.

### stealth

This works like \[stance:n\] and can be used for any class other than rogues that have a stealth ability, like druid cat form stealth, Night Elves' shadowmeld, etc.

It is redundant for rogues because \[stance:1\] and \[stealth\] do exactly the same thing for them.

### modifier:shift/ctrl/alt

Modifier keys are a convenient way to save action bar space and make certain decisions. Say you want an implied targeting macro but use one spell normally and another spell when you're holding down a modifier key:

`/cast [modifier, help] [modifier, @targettarget, help] Flash Heal; [help] [@targettarget] Greater Heal`

This macro will cast a helpful spell on either your target if it's friendly, or your target's target otherwise. When you hold any modifier key, it will cast Flash Heal. Otherwise it will cast Greater Heal.

For a less complicated example, the following macros all function identically. They will all cast spell A on your target, or spell B if the control key is held:

`/cast [mod:ctrl] Spell B; Spell A`

`/cast [@target] Spell A; [mod:ctrl, @target] Spell B`

`/cast [nomod] Spell A; [mod:ctrl] Spell B`

Of course, you can specify particular modifier keys for more control a la \[modifier:shift/ctrl\] which means "shift or control." If you want to specify both, you need two modifier conditionals: \[modifier:shift, modifier:ctrl\]. If you want to create a macro with one modifier for spell x and two modifiers, where one is the same as for x, for spell y you have to write the two modifiers first: `/cast` `[modifier:alt,` `modifier:ctrl,` `target=focus]` `Chimera` `Shot;` `[modifier:ctrl]` `Arcane` `Shot;` `Steady` `Shot`

Beware if you're using keybindings for your macros. If you bind A to a macro with, say, \[modifier:shift\] and you have something else bound to SHIFT-A, the SHIFT-A binding will take precedence and your macro will not run.

The shorter version of this conditional — mod — may be used to save characters in your macro.

#### Modifier variables

While modifier keys can only be one of shift, ctrl, or alt, there are a number of system variables that you can use in your modifier conditions as well. For instance, the SELFCAST variable means "whatever your self-cast modifier is set to." The default is alt (holding the alt key while casting a spell will attempt to cast it on yourself) though some AddOns give you the option to change this. If you create a macro like:

`/cast [modifier:SELFCAST, @player] [@mouseover] [ ] Greater Heal`

It will work as expected no matter what you have set as your self-cast key. Some other variables and their defaults (though with arguably much less utility) are as follows:

-   AUTOLOOTTOGGLE (shift)
-   STICKYCAMERA (ctrl)
-   SPLITSTACK (shift)
-   PICKUPACTION (shift)
-   COMPAREITEMS (shift)
-   OPENALLBAGS (shift)
-   QUESTWATCHTOGGLE (shift)

### button:1/2/.../5/*&lt;virtual click&gt;*

Similar to \[modifier\], \[button\] allows your macro to respond differently based on which mouse button is being used to activate the macro. Button numbers 1-5 correspond to left, right, middle, button 4, and button 5, respectively. If your macro is activated by a keybinding, \[button:1\] will always be true. As an example, here is the macro you can use for mounting:

`#show Swift Green Mechanostrider`
`    /userandom [nobutton:2, flyable, nomounted] Ebon Gryphon; [nomounted] Black Battlestrider, Swift Green Mechanostrider`
`    /dismount [noflying] [button:2]`

Behavior when not mounted: left-clicking will pick Ebon Gryphon if it can be used (flyable), otherwise it will randomly pick the Black Battlestrider or the Swift Green Mechanostrider. Right-clicking will always pick one of the mechachickens.

Behavior when mounted: left-click will only dismount if not flying. Right-click will always dismount.

The "virtual click" can usually be ignored, but if you use a bar mod it can be useful. Action bars that respond to various state changes translate clicks to virtual ones that determine which action to use. Because these virtual clicks are AddOn-specific, we won't go into any further detail here.

### equipped:*&lt;item type&gt;*

\[equipped\] allows you to determine if a particular type of gear is equipped. The item type can be an inventory slot name, an item type, or an item subtype. See [ItemType](ItemType "wikilink") and [InventorySlotName](InventorySlotName "wikilink") for lists of these types. Here is the macro you can use to pick Shield Bash or Pummel depending on what you've got equipped:

```
#show [equipped:Shields] Shield Bash; Pummel
/cast [equipped:Shields,stance:1/2] Shield Bash; [equipped:Shields] Defensive Stance; [stance:3] Pummel; Berserker Stance
```

The \#show line is used to make it show either Shield Bash or Pummel. Without it, it would show the stance spells as well, when applicable. Here's some pseudocode that illustrates how the second line works:

```
if a shield is equipped and you're in Battle or Defensive stance then
    /cast Shield Bash`
else if a shield is equipped then
    /cast Defensive Stance
else if you're in Berserker stance then
    /cast Pummel
else
    /cast Berserker Stance`
```

Here's another macro that lets you cast Overpower with a bit more vigor:

`/equip [noequipped:Two-Handed Axes] Crystalforged War Axe`
`/cast [nostance:1] Battle Stance; [equipped:Two-Handed Axes] Overpower`

### channeling:*&lt;spell name&gt;*

Normally, if you are channeling a spell and begin casting another spell, it will cancel the channel. This option allows you to keep that from happening, and also has a few other uses. For instance, maybe you do want to cancel one particular spell but not another. \[channeling\] alone matches any spell and you can also list an arbitrary number of spell names to check.

Note: channeling is NOT the same as casting. The \[channeling\] conditional only applies to spells like Arcane Missiles, Drain Life, Mind Flay, etc. where after the initial cast, the spell makes its effect over time.

### actionbar:1/.../6

The default UI provides a number of action bar pages. These pages only affect the lower left action bar that is visible by default. Luckily, you can make macros that respond to different action bar pages and place them on the other action bars. One example is for a hunter to emulate stances using their aspects:

```
/swapactionbar 1 2
/cast [actionbar:1] Aspect of the Hawk; Aspect of the Monkey
```

This macro will switch between action bars 1 and 2. When it switches to bar 1 it casts Aspect of the Hawk, and when it goes to bar 2 it casts Aspect of the Monkey.

### pet:*&lt;pet name or type&gt;*

Every class with a pet will find this one useful. It allows you to choose an action based on which pet you have out. You can specify your pet's name or your pet's type (Voidwalker, Boar, Imp, Wolf, etc.). \[pet\] by itself matches any pet. For example, a Mage can choose between their elemental's Freeze spell or their own Frost Nova:

`/cast [pet] Freeze; Frost Nova`

If you are not certain of the pet's type, you can run this command after summoning the pet. Do not use this as part of the macro, only for testing:

`/script print(`[`UnitCreatureFamily`](API_UnitCreatureFamily "wikilink")`("pet"))`

### combat

True if you are in combat.

### mounted, swimming, flying, indoors and outdoors

These are all fairly self-explanatory. They all apply to you, the player.

### flyable

As briefly mentioned above, \[flyable\] determines whether you are in the Outland or Northrend where you're allowed to use a flying mount.

As of Cataclysm you can use a flying mount in Kalimdor, the Eastern Kingdoms and Deepholm If you have the Cataclysm expansion set and if you are a level 60 and have the Expert Riding skill and the Flight Master's License (info From [comments on Wowhead](http://www.wowhead.com/spell=34090#comments) and )

At Patch 3.0.8 it is bugged in Dalaran and Wintergrasp. This zones are reported as flyable, but it is not possible to fly there.

As of Patch 3.2, flyable now works as expected in Dalaran and Wintergrasp (except during the battle for Wintergrasp).

### party and raid

These return true if the target is in your party or raid, respectively.

### group:party/raid

This lets you determine whether you are in the given group type. \[group\] is equivalent to \[group:party\]. \[group:raid\] implies \[group:party\]. This can be useful for buffing classes. For example:

`/cast [group, nomodifier] Arcane Brilliance; [help] [target=player] Arcane Intellect`

If you're in a group it will normally cast Arcane Brilliance. If you're holding a modifier key or you're solo, it will cast Arcane Intellect on a friendly target or yourself.

### talent:&lt;*tier\#*&gt;/&lt;*column\#*&gt;

Returns true if you have selected the talent from the specified tier (1-7) and column (1-3) combination. Useful if you want to use the same button to cast two (or more) diffrent spells from the same talent tier:

`/cast [talent:3/1] Call of the Elements; [talent:3/3] Totemic Projection `

If you have selected Call of the Elements (tier 3 column 1 Shaman talent) the macro will cast it. If you have selected Totemic Projection (tier 3 colmn 3 Shaman Talent), it will be cast instead.

Toggleable abilities
--------------------

As of patch 2.3.2, the cast command toggles abilities on and off. From the official patchnotes:

/cast will toggle spells again unless the name is prefixed with an exclamation mark, e.g. /castsequence Steady Shot, !Auto Shot
Examples of such toggleable abilities are Stealth, Shoot or Mass Dispel (the green targeting circle). If you want to spam such a macro without toggling the ability immediately off, prefix its name with an exclamation mark.

```
/cast !Stealth
/cast !Mass Dispel
/cast !Shoot
```

Macro option applications
-------------------------

Many of the commands introduced in Part I don't really come into their own until you add macro options to the mix. You've seen a few simple examples recently, but there's still a bit more to cover. The next couple sections will tie up these loose ends and hopefully give you some inspiration to start you on your way.

### Using Focus

Focus is a [unit ID](UnitId "wikilink") like target, player, or raidpet1target. It allows you to reference a mob, player, or NPC you specify. The simplest usage of focus is with key bindings. There are two focus-related functions in the bindings menu: Focus Target, and Target Focus. Focus Target sets your focus to whatever you are currently targeting (it will clear your focus if you have nothing targeted). Once you have a focus set, you can use it as a unit ID for any other command. Target Focus will, as you might guess, target the entity you have focused. However, these bindings don't really take full advantage of focus. In order to get the most bang for your buck, you will need to use macros with macro options.

One of the most common uses is to set a crowd control target. A mage can select a mob to sheep and set it as their focus. Now they can change targets for DPS and use the following macro whenever they need to re-sheep.

`/cast [@focus] Polymorph`

Or maybe a healer could set their focus to the main tank. With an AddOn like FocusFrame, they would then have a frame devoted to their main tank that they could easily use for healing.

In addition to the key bindings, there are also the /focus and /clearfocus slash commands. Without any parameters, /focus works exactly like the key binding, setting your current target as your focus. You can also specify any valid unit ID (see Targeting above) or name as a parameter to /focus:

`/focus party3target`

Here is an example of more advanced focusing:

```
/focus [@focus, noharm] [@focus, dead] [modifier]
/stopmacro [@focus, noexists]
/cast [@focus] Polymorph
```

The first line sets your focus to your current target (or clears your focus if you don't have a target) in one of the following situations:

-   You don't have a harmful focus (either it's friendly or doesn't exist)
-   Your current focus is dead
-   You are holding down a modifier key (in case you want to change your focus after you already have a valid one)

The second line keeps the macro from proceeding if you don't have a focus. Finally, it casts Polymorph on your focus. This gives you a one-button solution for your crowd control with focus. You may notice that we could have used an exists condition in the /cast command instead of a separate /stopmacro command. However, /stopmacro affords us a bit more flexibility by stoping any other commands we may add to the macro later (like a warning in /p).

It's possible to swap your target and your focus, giving you in effect two targets you can toggle between:

```
/cleartarget [@target, dead]
/clearfocus [@focus, dead]
/target focus
/cleartarget [@focus, noexists]
/targetlasttarget
/focus target
/targetlasttarget
```

The first two lines clear the target and/or focus if they are dead (if you really want to keep track of multiple dead targets, e.g. to resurrect or loot them, then delete those lines). The fourth is needed because /target focus doesn't clear your target if you have no current focus (without it, the fifth line would then retrieve your previous target).

### Macro Branching with /click

Say you want a button that chooses between three different spells based on shift, ctrl, or no modifier and two different targets depending on left or right click. This can be done all in one like the following:

`/cast [mod:shift, button:2, @player] [mod:shift, @party1] Greater Heal; [mod:ctrl, button:2, @player] [mod:ctrl, @party1] Flash Heal; [nomod, button:2, @player] [nomod, @party1] Renew`

That's quite an unwieldy bit of script there. We can split it onto multiple lines for clarity and remove some redundancies to save room but it's still a bit of a beast:

```
/cast [mod:shift, button:1, @party1] [mod:shift, @player] Greater Heal
/cast [mod:ctrl, button:1, @party1] [mod:ctrl, @player] Flash Heal
/cast [button:1, @party1] [@player] Renew
```

However, by using one master macro to choose the target based on mouse button and two macros to choose the spells based on modifier key, we can make it much easier to follow. For the sake of these examples, macros 2 and 3 are on MultiBarLeftButton2 and MultiBarLeftButton3, respectively.

Macro 1:

`/click [button:1] MultiBarLeftButton2; MultiBarLeftButton3`

Macro 2:

`/cast [mod:shift, @party1] Greater Heal; [mod:ctrl, @party1] Flash Heal; [@party1] Renew`

Macro 3:

`/cast [mod:shift, @player] Greater Heal; [mod:ctrl, @player] Flash Heal; [@player] Renew`

Custom icons
------------

If you would like to use custom icons for your macros, you can place them in your World of Warcraft\\Interface\\Icons folder (creating this folder if it doesn't exist). The files must follow the same guidelines for UI textures. Namely, they must be either BLP files or 24-bit/32-bit alpha uncompressed TGA files. Their dimensions must be powers of two up to 512 (e.g. 32x32, 512x128). Note: any images that aren't square will look squished on your action bar.

Keeping macros on multiple computers
------------------------------------

As of [Patch 3.0.2](Patch_3.0.2 "wikilink") [<sup><font color="orange">1</font></sup>](Patch_3.0.2#User_Interface "wikilink"), macros are now kept 'server-side', so there is "...no longer a need to reconfigure them when logging in using another computer."

Videos
------

★ WoW Macro Tutorial - Part 1 How to Make Your Own-0|Part 1 How to Make Your Own ★ WoW - Macro Tutorial - Part 2 How to Make Advanced Macros|Part 2 How to Make Advanced Macros

External links
--------------

-   [Macrotoon](http://www.macrotoon.com) - Up to date macros for all classes (Domain for Sale and previous Content not available) status: 12-15-2014
-   [WoW Lazy Macros](http://wowlazymacros.com) - Lazy macros for all damage and tank classes
-   [Cogwheel's Complete Macro Guide](http://forums.worldofwarcraft.com/thread.html?topicId=96143900&sid=1) - Original copy of this
-   [Fitzcairn's Macro Explain-o-matic](http://www.macroexplain.com)
-   [WoW Mastery](http://wowmastery.org) - Make Macros Easily within Minutes (Has anyone checked this site thats recommended in this blog, this reeks of an account hacking scam 100 miles against the wind)
-   \[<http://www.icy-veins.com/search?cx=partner-pub-1793336457812477%3A5162971253&cof=FORID%3A10&ie=UTF-8&q=macro&sa.x=0&sa.y=0&siteurl=www.icy-veins.com%2Fwow%2F&ref>=&ss=0j0j1&siteurl=www.icy-veins.com%2Fwow%2F&ref=&ss=0j0j1 Icy Veins search for "macros"\] is useful for learning macros by examples from others

[1]
