## Structure

| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 1 | ID | Integer | Criteria ID
| 2 | Achievement | iRefID | Reference to the achievement this criteria is needed for.
| 3 | Type | Integer | Which type is this criteria? This defines the rows below. See below.
| 4 | asset_id | Integer | Main requirement
| 5 | Quantity | Integer | Main requirement count
| 6 | start_event | Integer | additional requirement 1 type
| 7 | start_asset | Integer | additional requirement 1 value
| 8 | fail_event | Integer | additional requirement 2 type
| 9 | fail_asset | Integer | additional requirement 2 value
| 10-25 | Description | Loc | Criteria description.
| 26 | ? |   | Mostly 16712190, but not always
| 27 | Flags | Integer | display flags: 1: shows progress bar (other flags I don't know)
| 28 | timer_start_event | Integer |  
| 29 | timer_asset_id | Integer |  
| 30 | timer_time | Integer | Complete quest in %i seconds.
| 31 | ui_order | Integer |  

** **

**Description of the fields**

This describes rows 3 to 9 by type (row 2). There may be more types. Unlisted fields are zero.

This information is retrieved from DBCStructure.h.

**KILL_CREATURE = 0**

Also used for player deaths..


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | creatureID | Integer
| 5 | killCount | Integer

** **

**WIN_BG = 1**

There are further criterias instead just winning


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Map | iRefID
| 5 | winCount | Integer

** **

**REACH_LEVEL = 5**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | level | Integer

** **

**REACH_SKILL_LEVEL = 7**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | skillID | iRefID | SkillLine.dbc or what?
| 5 | skillLevel | Integer |  

** **

**COMPLETE_ACHIEVEMENT = 8**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Achievement | iRefID

** **

**COMPLETE_QUEST_COUNT = 9**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | totalQuestCount | Integer

** **

**COMPLETE_DAILY_QUEST_DAILY = 10**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | numberOfDays | Integer

** **

**COMPLETE_QUESTS_IN_ZONE = 11**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | zoneID | Integer
| 5 | questCount | Integer

** **

**DAMAGE_DONE = 13**


**COMPLETE_DAILY_QUEST = 14**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | questCount | Integer

** **

**COMPLETE_BATTLEGROUND = 15**

 
**DEATH_AT_MAP = 16**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Map | iRefID

** **

**DEATH_IN_DUNGEON = 18**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | manLimit | Integer

** **

**COMPLETE_RAID = 19**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | groupSize | Integer | can be 5, 10 or 25

** **

**KILLED_BY_CREATURE = 20**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | creatureEntry | Integer

** **

**FALL_WITHOUT_DYING = 24**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | fallHeight | Integer

** **

**DEATHS_FROM = 26**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | EnvironmentalDamage | iRefID

** **

**COMPLETE_QUEST = 27**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | questID | Integer
| 5 | questCount | Integer

** **

**BE_SPELL_TARGET = 28**

 
**BE_SPELL_TARGET2 = 69**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Spell | iRefID
| 5 | spellCount | Integer |  

** **

**CAST_SPELL = 29**

 
**CAST_SPELL2 = 110**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Spell | iRefID
| 5 | castCount | Integer

** **

**BG_OBJECTIVE_CAPTURE = 30**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | unknow | Integer | // value 42 = capture the flag
| 5 | count(?) | Integer | // how many captures required

** **

**HONORABLE_KILL_AT_AREA = 31**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Area | iRefID
| 5 | killCount | Integer

** **

**WIN_ARENA = 32**

 
**PLAY_ARENA = 33**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Map | iRefID

** **

**LEARN_SPELL = 34**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Spell | iRefID

** **

**OWN_ITEM = 36**


**WIN_RATED_ARENA = 37**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | unused | Integer |  
| 5 | count | Integer |  
| 6 | flag | Integer | 4=in a row

** **

**HIGHEST_TEAM_RATING = 38**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | teamtype | Integer | {2,3,5}

** **

**REACH_TEAM_RATING = 39**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | teamtype | Integer | {2,3,5}
| 5 | teamrating | Integer |  

** **

**LEARN_SKILL_LEVEL = 40**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | skillID | iRefID | SkillLine.dbc or what?
| 5 | skillLevel | Integer | apprentice=1, journeyman=2, expert=3, artisan=4, master=5, grand master=6

** **
**USE_ITEM = 41**

 
**LOOT_ITEM = 42**

 
**EXPLORE_AREA = 43**

This areaReference is **NOT** the index from AreaTable.dbc. It's from WorldMapOverlay.dbc.


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | areaReference | Integer

** **

 
**OWN_RANK = 44**

This rank is **NOT** the index from CharTitles.dbc


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | rank | Integer

** **

 
**BUY_BANK_SLOT = 45**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | numberOfSlots | Integer

** **

 
**GAIN_REPUTATION = 46**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | Faction | iRefID |  
| 5 | reputationAmount | Integer | Total reputation amount, so 42000 = exalted

** **

 
**GAIN_EXALTED_REPUTATION= 47**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | numberOfExaltedFactions | Integer

** **

 
**VISIT_BARBER_SHOP = 48**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | numberOfVisits | Integer

** **

 
**EQUIP_EPIC_ITEM = 49**

Where is the required itemlevel stored?


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | itemSlot | Integer

** **

 
**ROLL_NEED_ON_LOOT = 50**

 
**ROLL_GREED_ON_LOOT = 51**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | rollValue | Integer
| 5 | count | Integer

** **

 
**HK_CLASS = 52**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Class | iRefID
| 5 | count | Integer

** **

 
**HK_RACE = 53**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Race | iRefID
| 5 | count | Integer

** **

 
**DO_EMOTE = 54**

| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | Emote | iRefID |  
| 5 | count | Integer | count of emotes, always required special target or requirements

** **

 
**HEALING_DONE = 55**

 
**GET_KILLING_BLOWS = 56**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | unused | Integer |  
| 5 | count | Integer |  
| 6 | flag | Integer | 3 for battleground healing
| 7 | Map | iRefID |  

** **

 
**EQUIP_ITEM = 57**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | Item | iRefID
| 5 | itemCount | Integer

** **

 
**MONEY_FROM_QUEST_REWARD= 62**

 
**LOOT_MONEY = 67**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | goldInCopper | Integer

** **

 
**USE_GAMEOBJECT = 68**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | goEntry | Integer
| 5 | useCount | Integer

** **

 
**SPECIAL_PVP_KILL = 70**

Are those special criteria stored in the dbc?


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | killCount | Integer

** **

 
**FISH_IN_GAMEOBJECT = 72**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | goEntry | Integer
| 5 | lootCount | Integer

** **

 
**LEARN_SKILLLINE_SPELLS = 75**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | SkillLine | iRefID
| 5 | spellCount | Integer

** **

 
**WIN_DUEL = 76**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | duelCount | Integer

** **

 
**HIGHEST_POWER = 96**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | powerType | Integer | 0=mana, 1=rage, 3=energy, 6=runic power

** **

 
**HIGHEST_STAT = 97**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | statType | Integer | 4=spirit, 3=int, 2=stamina, 1=agi, 0=strength

** **

 
**HIGHEST_SPELLPOWER = 98**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | spellSchool | iRefID | SkillLine or Resistances ?

** **

 
**HIGHEST_RATING = 100**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | ratingType | Integer

** **

 
**LOOT_TYPE = 109**


| **Column** | **Field** | **Type** | **Notes**
| ---| ---| ---| ---
| 4 | lootType | Integer | 3=fishing, 2=pickpocket, 4=disentchant
| 5 | lootTypeCount | Integer |  

** **

 
**LEARN_SKILL_LINE = 112**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | SkillLine | iRefID
| 5 | spellCount | Integer

** **

 
**EARN_HONORABLE_KILL = 113**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | killCount | Integer

** **

 
**ACCEPTED_SUMMONS = 114**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | Here comes a 1 in, because it's a Statistic | Integer

** **

 
**ACHIVEMENTPOINTS_REACHED = 115**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | unused | Integer

** **
 
**RANDOM_DUNGEON_PLAYERCOUNT = 119**


| **Column** | **Field** | **Type**
| ---| ---| ---
| 4 | unused | Integer
| 5 | PlayerCount | Integer

** **


