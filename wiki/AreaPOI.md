## Structure


| Column | Field | Type | Notes
| ---| ---| ---| ---
| 1 | ID | Integer |  
| 2 | importance | Integer |  
| 3 | NormalIcon | Integer | This is getting displayed normally.
| 4 | NormalIcon50% | Integer | Destructible building being neutral at 50%.
| 5 | NormalIcon0% | Integer | Destroyed neutral building.
| 6 | HordeIcon | Integer | Building at 100% captured by the horde.
| 7 | HordeIcon50% | Integer | Destructible building being neutral at 50%.
| 8 | HordeIcon0% | Integer | Destroyed horde building.
| 9 | AllianceIcon | Integer | Building at 100% captured by the alliance.
| 10 | AllianceIcon50% | Integer | Destructible building being neutral at 50%.
| 11 | AllianceIcon0% | Integer | Destroyed alliance building.
| 12 | factionID | Integer | This being an icon would make no sense. Walls for cities? Oo
| 13 | X | Float | Coordinates of the POI. Global ones.
| 14 | Y | Float |  
| 15 | Z | Float |  
| 16 | continentID | iRefID | And on which map that POI is.
| 17 | flags | Integer | Flags defining, where this icon is shown. &4: Zone, &128: BG, &512: showInBattle(mini)Map, Old: See this.
| 18 | Area | iRefID |  
| 19 | Name | Loc |  
| 36 | Description | Loc | The alert triggered on the zone (World Event/PvP states mostly).
| 53 | worldState | Integer | Most likely the value defines the icon.
| 54 | worldMapLink | Null | (WotLK)

** **

**Description of the fields**

**Icons**

The icons are not referenced somewhere but are in the Interface\Minimap\POIICONS file which is a 256*256 file with 16*16 pixel icons.

|   | + 0 | + 1 | + 2 | + 3 | + 4 | + 5 | + 6 | + 7 | + 8 | + 9 | + 10 | + 11 | + 12 | + 13 | + 14 | + 15 |  |
| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---| ---
| 0 | none | av - mine - N | av - mine - H | av - mine - A | graveyard - N / A | city | tower |  ! Flag | graveyard normal | tower - N / A | tower - H | tower - A | tower - N / H | graveyard - H | graveyard - N / H | graveyard - A
| 16 | ab - gold mine - N | ab - gold mine - N / A | ab - gold mine - A | ab - gold mine - N / H | ab - gold mine - H | ab - lumber mill - N | ab - lumber mill - N / A | ab - lumber mill - A | ab - lumber mill - N / H | ab - lumber mill - H | ab - blacksmith - N | ab - blacksmith - N / A | ab - blacksmith - A | ab - blacksmith - N / H | ab - blacksmith - H | ab - farm - N
| 32 | ab - farm - N / A | ab - farm - A | ab - farm - N / H | ab - farm - H | ab - stables - N | ab - stables - N / A | ab - stables - A | ab - stables - N / H | ab - stables - H | Naxxramas invasion | sandworm | flag - A | flag - H | flag - N | medal - A | medal - N / A
| 48 | medal - H | medal - N / H | tower - destr. 50% - A | tower - destr. - A | tower - destr. 50% - H | tower - destr. - H | tower - destr. 50% - N | tower - destr. - N | bridge? - 100% - gray | bridge? - 50% - gray | bridge? - 0% - gray | bridge? - 100% - red | bridge? - 50% - red | bridge? - 0% - red | bridge? - 100% - blue | bridge? - 50% - blue
| 64 | bridge? - 0% - blue | building - 100% - gray | building - 50% - gray | building - 0% - gray | building - 100% - red | building - 50% - red | building - 0% - red | building - 100% - blue | building - 50% - blue | building - 0% - blue | gate - 100% - gray | gate - 50% - gray | gate - 0% - gray | gate - 100% - red | gate - 50% - red | gate - 0% - red
| 80 | gate - 100% - blue | gate - 50% - blue | gate - 0% - blue | wall_ho - 100% - gray | wall_ho - 50% - gray | wall_ho - 0% - gray | wall_ho - 100% - red | wall_ho - 50% - red | wall_ho - 0% - red | wall_ho - 100% - blue | wall_ho - 50% - blue | wall_ho - 0% - blue | wall_vert - 100% - gray | wall_vert - 50% - gray | wall_vert - 0% - gray | wall_vert - 100% - red
| 96 | wall_vert - 50% - red | wall_vert - 0% - red | wall_vert - 100% - blue | wall_vert - 50% - blue | wall_vert - 0% - blue | crossed swords | gate - 100% - yellow | gate - 50% - yellow | gate - 0% - yellow | gate - 100% - violet | gate - 50% - violet | gate - 0% - violet | gate - 100% - green | gate - 50% - green | gate - 0% - green | 0
| 112 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |  : |   |   |   |  

** **
