---
ID: 79
post_title: wotlk-achievement-criteria
author: yehonal
post_date: 2017-05-23 16:21:30
post_excerpt: ""
layout: page
_permalink: >
  https://wowgaming.altervista.org/wp/wotlk-achievement-criteria/
published: true
tags: [ ]
categories:
  - Wrath of The Lich King
---
<div id="content">
        <h2 id="structure">Structure</h2>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>ID</td>
      <td>Integer</td>
      <td>Criteria ID</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Achievement</td>
      <td>iRefID</td>
      <td>Reference to the achievement this criteria is needed for.</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Type</td>
      <td>Integer</td>
      <td>Which type is this criteria? This defines the rows below. See below.</td>
    </tr>
    <tr>
      <td>4</td>
      <td>asset_id</td>
      <td>Integer</td>
      <td>Main requirement</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Quantity</td>
      <td>Integer</td>
      <td>Main requirement count</td>
    </tr>
    <tr>
      <td>6</td>
      <td>start_event</td>
      <td>Integer</td>
      <td>additional requirement 1 type</td>
    </tr>
    <tr>
      <td>7</td>
      <td>start_asset</td>
      <td>Integer</td>
      <td>additional requirement 1 value</td>
    </tr>
    <tr>
      <td>8</td>
      <td>fail_event</td>
      <td>Integer</td>
      <td>additional requirement 2 type</td>
    </tr>
    <tr>
      <td>9</td>
      <td>fail_asset</td>
      <td>Integer</td>
      <td>additional requirement 2 value</td>
    </tr>
    <tr>
      <td>10-25</td>
      <td>Description</td>
      <td>Loc</td>
      <td>Criteria description.</td>
    </tr>
    <tr>
      <td>26</td>
      <td>?</td>
      <td>&nbsp;</td>
      <td>Mostly 16712190, but not always</td>
    </tr>
    <tr>
      <td>27</td>
      <td>Flags</td>
      <td>Integer</td>
      <td>display flags: 1: shows progress bar (other flags I don’t know)</td>
    </tr>
    <tr>
      <td>28</td>
      <td>timer_start_event</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>29</td>
      <td>timer_asset_id</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>30</td>
      <td>timer_time</td>
      <td>Integer</td>
      <td>Complete quest in %i seconds.</td>
    </tr>
    <tr>
      <td>31</td>
      <td>ui_order</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>Description of the fields</strong></p>

<p>This describes rows 3 to 9 by type (row 2). There may be more types. Unlisted fields are zero.</p>

<p>This information is retrieved from DBCStructure.h.</p>

<p><strong>KILL_CREATURE = 0</strong></p>

<p>Also used for player deaths..</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>creatureID</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>killCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>WIN_BG = 1</strong></p>

<p>There are further criterias instead just winning</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Map</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>winCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>REACH_LEVEL = 5</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>level</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>REACH_SKILL_LEVEL = 7</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>skillID</td>
      <td>iRefID</td>
      <td>SkillLine.dbc or what?</td>
    </tr>
    <tr>
      <td>5</td>
      <td>skillLevel</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_ACHIEVEMENT = 8</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Achievement</td>
      <td>iRefID</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_QUEST_COUNT = 9</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>totalQuestCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_DAILY_QUEST_DAILY = 10</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>numberOfDays</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_QUESTS_IN_ZONE = 11</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>zoneID</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>questCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>DAMAGE_DONE = 13</strong></p>

<p><strong>COMPLETE_DAILY_QUEST = 14</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>questCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_BATTLEGROUND = 15</strong></p>

<p><strong>DEATH_AT_MAP = 16</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Map</td>
      <td>iRefID</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>DEATH_IN_DUNGEON = 18</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>manLimit</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_RAID = 19</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>groupSize</td>
      <td>Integer</td>
      <td>can be 5, 10 or 25</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>KILLED_BY_CREATURE = 20</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>creatureEntry</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>FALL_WITHOUT_DYING = 24</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>fallHeight</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>DEATHS_FROM = 26</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>EnvironmentalDamage</td>
      <td>iRefID</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>COMPLETE_QUEST = 27</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>questID</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>questCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>BE_SPELL_TARGET = 28</strong></p>

<p><strong>BE_SPELL_TARGET2 = 69</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Spell</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>spellCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>CAST_SPELL = 29</strong></p>

<p><strong>CAST_SPELL2 = 110</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Spell</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>castCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>BG_OBJECTIVE_CAPTURE = 30</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unknow</td>
      <td>Integer</td>
      <td>// value 42 = capture the flag</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count(?)</td>
      <td>Integer</td>
      <td>// how many captures required</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HONORABLE_KILL_AT_AREA = 31</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Area</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>killCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>WIN_ARENA = 32</strong></p>

<p><strong>PLAY_ARENA = 33</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Map</td>
      <td>iRefID</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>LEARN_SPELL = 34</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Spell</td>
      <td>iRefID</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>OWN_ITEM = 36</strong></p>

<p><strong>WIN_RATED_ARENA = 37</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>6</td>
      <td>flag</td>
      <td>Integer</td>
      <td>4=in a row</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HIGHEST_TEAM_RATING = 38</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>teamtype</td>
      <td>Integer</td>
      <td>{2,3,5}</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>REACH_TEAM_RATING = 39</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>teamtype</td>
      <td>Integer</td>
      <td>{2,3,5}</td>
    </tr>
    <tr>
      <td>5</td>
      <td>teamrating</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>LEARN_SKILL_LEVEL = 40</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>skillID</td>
      <td>iRefID</td>
      <td>SkillLine.dbc or what?</td>
    </tr>
    <tr>
      <td>5</td>
      <td>skillLevel</td>
      <td>Integer</td>
      <td>apprentice=1, journeyman=2, expert=3, artisan=4, master=5, grand master=6</td>
    </tr>
  </tbody>
</table>

<hr>
<p><strong>USE_ITEM = 41</strong></p>

<p><strong>LOOT_ITEM = 42</strong></p>

<p><strong>EXPLORE_AREA = 43</strong></p>

<p>This areaReference is <strong>NOT</strong> the index from AreaTable.dbc. It’s from WorldMapOverlay.dbc.</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>areaReference</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>OWN_RANK = 44</strong></p>

<p>This rank is <strong>NOT</strong> the index from CharTitles.dbc</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>rank</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>BUY_BANK_SLOT = 45</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>numberOfSlots</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>GAIN_REPUTATION = 46</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Faction</td>
      <td>iRefID</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>5</td>
      <td>reputationAmount</td>
      <td>Integer</td>
      <td>Total reputation amount, so 42000 = exalted</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>GAIN_EXALTED_REPUTATION= 47</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>numberOfExaltedFactions</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>VISIT_BARBER_SHOP = 48</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>numberOfVisits</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>EQUIP_EPIC_ITEM = 49</strong></p>

<p>Where is the required itemlevel stored?</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>itemSlot</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>ROLL_NEED_ON_LOOT = 50</strong></p>

<p><strong>ROLL_GREED_ON_LOOT = 51</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>rollValue</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HK_CLASS = 52</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Class</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HK_RACE = 53</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Race</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>DO_EMOTE = 54</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Emote</td>
      <td>iRefID</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
      <td>count of emotes, always required special target or requirements</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HEALING_DONE = 55</strong></p>

<p><strong>GET_KILLING_BLOWS = 56</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>5</td>
      <td>count</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>6</td>
      <td>flag</td>
      <td>Integer</td>
      <td>3 for battleground healing</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Map</td>
      <td>iRefID</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>EQUIP_ITEM = 57</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>Item</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>itemCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>MONEY_FROM_QUEST_REWARD= 62</strong></p>

<p><strong>LOOT_MONEY = 67</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>goldInCopper</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>USE_GAMEOBJECT = 68</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>goEntry</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>useCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>SPECIAL_PVP_KILL = 70</strong></p>

<p>Are those special criteria stored in the dbc?</p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>killCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>FISH_IN_GAMEOBJECT = 72</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>goEntry</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>lootCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>LEARN_SKILLLINE_SPELLS = 75</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>SkillLine</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>spellCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>WIN_DUEL = 76</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>duelCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HIGHEST_POWER = 96</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>powerType</td>
      <td>Integer</td>
      <td>0=mana, 1=rage, 3=energy, 6=runic power</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HIGHEST_STAT = 97</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>statType</td>
      <td>Integer</td>
      <td>4=spirit, 3=int, 2=stamina, 1=agi, 0=strength</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HIGHEST_SPELLPOWER = 98</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>spellSchool</td>
      <td>iRefID</td>
      <td>SkillLine or Resistances ?</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>HIGHEST_RATING = 100</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>ratingType</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>LOOT_TYPE = 109</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
      <th><strong>Notes</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>lootType</td>
      <td>Integer</td>
      <td>3=fishing, 2=pickpocket, 4=disentchant</td>
    </tr>
    <tr>
      <td>5</td>
      <td>lootTypeCount</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>LEARN_SKILL_LINE = 112</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>SkillLine</td>
      <td>iRefID</td>
    </tr>
    <tr>
      <td>5</td>
      <td>spellCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>EARN_HONORABLE_KILL = 113</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>killCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>ACCEPTED_SUMMONS = 114</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Here comes a 1 in, because it’s a Statistic</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>ACHIVEMENTPOINTS_REACHED = 115</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>RANDOM_DUNGEON_PLAYERCOUNT = 119</strong></p>

<table>
  <thead>
    <tr>
      <th><strong>Column</strong></th>
      <th><strong>Field</strong></th>
      <th><strong>Type</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>4</td>
      <td>unused</td>
      <td>Integer</td>
    </tr>
    <tr>
      <td>5</td>
      <td>PlayerCount</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

<hr>



      </div>