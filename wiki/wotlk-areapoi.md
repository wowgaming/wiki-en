<div id="content">
        <h2 id="structure">Structure</h2>

<table>
  <thead>
    <tr>
      <th>Column</th>
      <th>Field</th>
      <th>Type</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>ID</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>2</td>
      <td>importance</td>
      <td>Integer</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>3</td>
      <td>NormalIcon</td>
      <td>Integer</td>
      <td>This is getting displayed normally.</td>
    </tr>
    <tr>
      <td>4</td>
      <td>NormalIcon50%</td>
      <td>Integer</td>
      <td>Destructible building being neutral at 50%.</td>
    </tr>
    <tr>
      <td>5</td>
      <td>NormalIcon0%</td>
      <td>Integer</td>
      <td>Destroyed neutral building.</td>
    </tr>
    <tr>
      <td>6</td>
      <td>HordeIcon</td>
      <td>Integer</td>
      <td>Building at 100% captured by the horde.</td>
    </tr>
    <tr>
      <td>7</td>
      <td>HordeIcon50%</td>
      <td>Integer</td>
      <td>Destructible building being neutral at 50%.</td>
    </tr>
    <tr>
      <td>8</td>
      <td>HordeIcon0%</td>
      <td>Integer</td>
      <td>Destroyed horde building.</td>
    </tr>
    <tr>
      <td>9</td>
      <td>AllianceIcon</td>
      <td>Integer</td>
      <td>Building at 100% captured by the alliance.</td>
    </tr>
    <tr>
      <td>10</td>
      <td>AllianceIcon50%</td>
      <td>Integer</td>
      <td>Destructible building being neutral at 50%.</td>
    </tr>
    <tr>
      <td>11</td>
      <td>AllianceIcon0%</td>
      <td>Integer</td>
      <td>Destroyed alliance building.</td>
    </tr>
    <tr>
      <td>12</td>
      <td>factionID</td>
      <td>Integer</td>
      <td>This being an icon would make no sense. Walls for cities? Oo</td>
    </tr>
    <tr>
      <td>13</td>
      <td>X</td>
      <td>Float</td>
      <td>Coordinates of the POI. Global ones.</td>
    </tr>
    <tr>
      <td>14</td>
      <td>Y</td>
      <td>Float</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>15</td>
      <td>Z</td>
      <td>Float</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>16</td>
      <td>continentID</td>
      <td>iRefID</td>
      <td>And on which map that POI is.</td>
    </tr>
    <tr>
      <td>17</td>
      <td>flags</td>
      <td>Integer</td>
      <td>Flags defining, where this icon is shown. &amp;4: Zone, &amp;128: BG, &amp;512: showInBattle(mini)Map, Old: See this.</td>
    </tr>
    <tr>
      <td>18</td>
      <td>Area</td>
      <td>iRefID</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>19</td>
      <td>Name</td>
      <td>Loc</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>36</td>
      <td>Description</td>
      <td>Loc</td>
      <td>The alert triggered on the zone (World Event/PvP states mostly).</td>
    </tr>
    <tr>
      <td>53</td>
      <td>worldState</td>
      <td>Integer</td>
      <td>Most likely the value defines the icon.</td>
    </tr>
    <tr>
      <td>54</td>
      <td>worldMapLink</td>
      <td>Null</td>
      <td>(WotLK)</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>Description of the fields</strong></p>

<p><strong>Icons</strong></p>

<p>The icons are not referenced somewhere but are in the Interface\Minimap\POIICONS file which is a 256<em>256 file with 16</em>16 pixel icons.</p>

<table>
  <thead>
    <tr>
      <th>&nbsp;</th>
      <th>+ 0</th>
      <th>+ 1</th>
      <th>+ 2</th>
      <th>+ 3</th>
      <th>+ 4</th>
      <th>+ 5</th>
      <th>+ 6</th>
      <th>+ 7</th>
      <th>+ 8</th>
      <th>+ 9</th>
      <th>+ 10</th>
      <th>+ 11</th>
      <th>+ 12</th>
      <th>+ 13</th>
      <th>+ 14</th>
      <th>+ 15</th>
      <th>&nbsp;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>none</td>
      <td>av - mine - N</td>
      <td>av - mine - H</td>
      <td>av - mine - A</td>
      <td>graveyard - N / A</td>
      <td>city</td>
      <td>tower</td>
      <td>! Flag</td>
      <td>graveyard normal</td>
      <td>tower - N / A</td>
      <td>tower - H</td>
      <td>tower - A</td>
      <td>tower - N / H</td>
      <td>graveyard - H</td>
      <td>graveyard - N / H</td>
      <td>graveyard - A</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>16</td>
      <td>ab - gold mine - N</td>
      <td>ab - gold mine - N / A</td>
      <td>ab - gold mine - A</td>
      <td>ab - gold mine - N / H</td>
      <td>ab - gold mine - H</td>
      <td>ab - lumber mill - N</td>
      <td>ab - lumber mill - N / A</td>
      <td>ab - lumber mill - A</td>
      <td>ab - lumber mill - N / H</td>
      <td>ab - lumber mill - H</td>
      <td>ab - blacksmith - N</td>
      <td>ab - blacksmith - N / A</td>
      <td>ab - blacksmith - A</td>
      <td>ab - blacksmith - N / H</td>
      <td>ab - blacksmith - H</td>
      <td>ab - farm - N</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>32</td>
      <td>ab - farm - N / A</td>
      <td>ab - farm - A</td>
      <td>ab - farm - N / H</td>
      <td>ab - farm - H</td>
      <td>ab - stables - N</td>
      <td>ab - stables - N / A</td>
      <td>ab - stables - A</td>
      <td>ab - stables - N / H</td>
      <td>ab - stables - H</td>
      <td>Naxxramas invasion</td>
      <td>sandworm</td>
      <td>flag - A</td>
      <td>flag - H</td>
      <td>flag - N</td>
      <td>medal - A</td>
      <td>medal - N / A</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>48</td>
      <td>medal - H</td>
      <td>medal - N / H</td>
      <td>tower - destr. 50% - A</td>
      <td>tower - destr. - A</td>
      <td>tower - destr. 50% - H</td>
      <td>tower - destr. - H</td>
      <td>tower - destr. 50% - N</td>
      <td>tower - destr. - N</td>
      <td>bridge? - 100% - gray</td>
      <td>bridge? - 50% - gray</td>
      <td>bridge? - 0% - gray</td>
      <td>bridge? - 100% - red</td>
      <td>bridge? - 50% - red</td>
      <td>bridge? - 0% - red</td>
      <td>bridge? - 100% - blue</td>
      <td>bridge? - 50% - blue</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>64</td>
      <td>bridge? - 0% - blue</td>
      <td>building - 100% - gray</td>
      <td>building - 50% - gray</td>
      <td>building - 0% - gray</td>
      <td>building - 100% - red</td>
      <td>building - 50% - red</td>
      <td>building - 0% - red</td>
      <td>building - 100% - blue</td>
      <td>building - 50% - blue</td>
      <td>building - 0% - blue</td>
      <td>gate - 100% - gray</td>
      <td>gate - 50% - gray</td>
      <td>gate - 0% - gray</td>
      <td>gate - 100% - red</td>
      <td>gate - 50% - red</td>
      <td>gate - 0% - red</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>80</td>
      <td>gate - 100% - blue</td>
      <td>gate - 50% - blue</td>
      <td>gate - 0% - blue</td>
      <td>wall_ho - 100% - gray</td>
      <td>wall_ho - 50% - gray</td>
      <td>wall_ho - 0% - gray</td>
      <td>wall_ho - 100% - red</td>
      <td>wall_ho - 50% - red</td>
      <td>wall_ho - 0% - red</td>
      <td>wall_ho - 100% - blue</td>
      <td>wall_ho - 50% - blue</td>
      <td>wall_ho - 0% - blue</td>
      <td>wall_vert - 100% - gray</td>
      <td>wall_vert - 50% - gray</td>
      <td>wall_vert - 0% - gray</td>
      <td>wall_vert - 100% - red</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>96</td>
      <td>wall_vert - 50% - red</td>
      <td>wall_vert - 0% - red</td>
      <td>wall_vert - 100% - blue</td>
      <td>wall_vert - 50% - blue</td>
      <td>wall_vert - 0% - blue</td>
      <td>crossed swords</td>
      <td>gate - 100% - yellow</td>
      <td>gate - 50% - yellow</td>
      <td>gate - 0% - yellow</td>
      <td>gate - 100% - violet</td>
      <td>gate - 50% - violet</td>
      <td>gate - 0% - violet</td>
      <td>gate - 100% - green</td>
      <td>gate - 50% - green</td>
      <td>gate - 0% - green</td>
      <td>0</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>112</td>
      <td>1</td>
      <td>2</td>
      <td>3</td>
      <td>4</td>
      <td>5</td>
      <td>6</td>
      <td>7</td>
      <td>8</td>
      <td>9</td>
      <td>:</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
      <td>&nbsp;</td>
    </tr>
  </tbody>
</table>

<hr>


      </div>
