<div id="content">
        <h2 id="structure" class="clickable-header">Structure</h2>

<table>
  <thead>
    <tr>
      <th>Column</th>
      <th>Name</th>
      <th>Type</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>ID</td>
      <td>Int</td>
      <td>Zone Area</td>
    </tr>
    <tr>
      <td>2</td>
      <td>MapID</td>
      <td>Int</td>
      <td>Map or Continent</td>
    </tr>
    <tr>
      <td>3</td>
      <td>AreaID</td>
      <td>Int</td>
      <td>SubArea of Map</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Explore Flag</td>
      <td>Int</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>5</td>
      <td>Flags</td>
      <td>Int</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>8</td>
      <td>SoundAmbienceID</td>
      <td>Int</td>
      <td>Reference to what Ambiance to use during day and night</td>
    </tr>
    <tr>
      <td>9</td>
      <td>ZoneMusicID</td>
      <td>Int</td>
      <td>Reference to what zone music to play</td>
    </tr>
    <tr>
      <td>10</td>
      <td>ZoneIntroMusicID</td>
      <td>Int</td>
      <td>Reference to what zone intro music to play when entering area</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Area Level</td>
      <td>Int</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>12-28</td>
      <td>Area Name</td>
      <td>String</td>
      <td>&nbsp;</td>
    </tr>
    <tr>
      <td>29</td>
      <td>FactionGroupID</td>
      <td>Int</td>
      <td>Faction that owns area</td>
    </tr>
  </tbody>
</table>

<hr>

<p><strong>Description of the fields</strong></p>
<h2 id="flags" class="clickable-header">Flags</h2>

<table>
  <thead>
    <tr>
      <th>Value</th>
      <th>Name</th>
      <th>Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0x00000001</td>
      <td>AREA_FLAG_SNOW</td>
      <td>snow (only Dun Morogh, Naxxramas, Razorfen Downs and Winterspring)</td>
    </tr>
    <tr>
      <td>0x00000002</td>
      <td>AREA_FLAG_UNK1</td>
      <td>may be necropolis?</td>
    </tr>
    <tr>
      <td>0x00000004</td>
      <td>AREA_FLAG_UNK2</td>
      <td>Only used for areas on map 571 (development before)</td>
    </tr>
    <tr>
      <td>0x00000008</td>
      <td>AREA_FLAG_SLAVE_CAPITAL</td>
      <td>city and city subsones</td>
    </tr>
    <tr>
      <td>0x00000010</td>
      <td>AREA_FLAG_UNK3</td>
      <td>can’t find common meaning</td>
    </tr>
    <tr>
      <td>0x00000020</td>
      <td>AREA_FLAG_SLAVE_CAPITAL2</td>
      <td>slave capital city flag?</td>
    </tr>
    <tr>
      <td>0x00000040</td>
      <td>AREA_FLAG_ALLOW_DUELS</td>
      <td>allow to duel here</td>
    </tr>
    <tr>
      <td>0x00000080</td>
      <td>AREA_FLAG_ARENA</td>
      <td>arena, both instanced and world arenas</td>
    </tr>
    <tr>
      <td>0x00000100</td>
      <td>AREA_FLAG_CAPITAL</td>
      <td>main capital city flag</td>
    </tr>
    <tr>
      <td>0x00000200</td>
      <td>AREA_FLAG_CITY</td>
      <td>only for one zone named “City” (where it located?)</td>
    </tr>
    <tr>
      <td>0x00000400</td>
      <td>AREA_FLAG_OUTLAND</td>
      <td>expansion zones? (only Eye of the Storm not have this flag, but have 0x00004000 flag)</td>
    </tr>
    <tr>
      <td>0x00000800</td>
      <td>AREA_FLAG_SANCTUARY</td>
      <td>sanctuary area (PvP disabled)</td>
    </tr>
    <tr>
      <td>0x00001000</td>
      <td>AREA_FLAG_NEED_FLY</td>
      <td>only Netherwing Ledge, Socrethar’s Seat, Tempest Keep, The Arcatraz, The Botanica, The Mechanar, Sorrow Wing Point, Dragonspine Ridge, Netherwing Mines, Dragonmaw Base Camp, Dragonmaw Skyway</td>
    </tr>
    <tr>
      <td>0x00002000</td>
      <td>AREA_FLAG_UNUSED1</td>
      <td>not used now (no area/zones with this flag set in 3.0.3)</td>
    </tr>
    <tr>
      <td>0x00004000</td>
      <td>AREA_FLAG_OUTLAND2</td>
      <td>expansion zones? (only Circle of Blood Arena not have this flag, but have 0x00000400 flag)</td>
    </tr>
    <tr>
      <td>0x00008000</td>
      <td>AREA_FLAG_OUTDOOR_PVP</td>
      <td>pvp objective area? (Death’s Door also has this flag although it’s no pvp object area)</td>
    </tr>
    <tr>
      <td>0x00010000</td>
      <td>AREA_FLAG_ARENA_INSTANCE</td>
      <td>used by instanced arenas only</td>
    </tr>
    <tr>
      <td>0x00020000</td>
      <td>AREA_FLAG_UNUSED2</td>
      <td>not used now (no area/zones with this flag set in 3.0.3)</td>
    </tr>
    <tr>
      <td>0x00040000</td>
      <td>AREA_FLAG_CONTESTED_AREA</td>
      <td>On PvP servers these areas are considered contested, even though the zone it is contained in is a Horde/Alliance territory.</td>
    </tr>
    <tr>
      <td>0x00080000</td>
      <td>AREA_FLAG_UNK6</td>
      <td>Valgarde and Acherus: The Ebon Hold</td>
    </tr>
    <tr>
      <td>0x00100000</td>
      <td>AREA_FLAG_LOWLEVEL</td>
      <td>used for some starting areas with area_level &lt;=15</td>
    </tr>
    <tr>
      <td>0x00200000</td>
      <td>AREA_FLAG_TOWN</td>
      <td>small towns with Inn</td>
    </tr>
    <tr>
      <td>0x00400000</td>
      <td>AREA_FLAG_UNK7</td>
      <td>Warsong Hold, Acherus: The Ebon Hold, New Agamand Inn, Vengeance Landing Inn</td>
    </tr>
    <tr>
      <td>0x00800000</td>
      <td>AREA_FLAG_UNK8</td>
      <td>Westguard Inn, Acherus: The Ebon Hold, Valgarde</td>
    </tr>
    <tr>
      <td>0x01000000</td>
      <td>AREA_FLAG_WINTERGRASP</td>
      <td>Wintergrasp and it’s subzones</td>
    </tr>
    <tr>
      <td>0x02000000</td>
      <td>AREA_FLAG_INSIDE</td>
      <td>used for determinating spell related inside/outside questions in Map::IsOutdoors</td>
    </tr>
    <tr>
      <td>0x04000000</td>
      <td>AREA_FLAG_OUTSIDE</td>
      <td>used for determinating spell related inside/outside questions in Map::IsOutdoors</td>
    </tr>
    <tr>
      <td>0x08000000</td>
      <td>AREA_FLAG_WINTERGRASP_2</td>
      <td>Wintergrasp and it’s subzones</td>
    </tr>
    <tr>
      <td>0x20000000</td>
      <td>AREA_FLAG_CANNOT_FLY</td>
      <td>not allowed to fly, only used in Dalaran areas (zone 4395)</td>
    </tr>
  </tbody>
</table>

<hr>

<h2 id="content" class="clickable-header">Content</h2>

<table>
  <thead>
    <tr>
      <th>Field Nb</th>
      <th>Name</th>
      <th>MapID</th>
      <th>AreaID</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>Dun Morogh</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2</td>
      <td>Longshore</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>3</td>
      <td>Badlands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4</td>
      <td>Blasted Lands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>7</td>
      <td>Blackwater Cove</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>8</td>
      <td>Swamp of Sorrows</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>9</td>
      <td>Northshire Valley</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>10</td>
      <td>Duskwood</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>11</td>
      <td>Wetlands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>12</td>
      <td>Elwynn Forest</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>13</td>
      <td>The World Tree</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>14</td>
      <td>Durotar</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>15</td>
      <td>Dustwallow Marsh</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>16</td>
      <td>Azshara</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>17</td>
      <td>The Barrens</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>18</td>
      <td>Crystal Lake</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>19</td>
      <td>Zul’Gurub</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>20</td>
      <td>Moonbrook</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>21</td>
      <td>Kul Tiras</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>22</td>
      <td>Programmer Isle</td>
      <td>451</td>
      <td>0</td>
    </tr>
    <tr>
      <td>23</td>
      <td>Northshire River</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>24</td>
      <td>Northshire Abbey</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>25</td>
      <td>Blackrock Mountain</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>26</td>
      <td>Lighthouse</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>28</td>
      <td>Western Plaguelands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>30</td>
      <td>Nine</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>32</td>
      <td>The Cemetary</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>33</td>
      <td>Stranglethorn Vale</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>34</td>
      <td>Echo Ridge Mine</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>35</td>
      <td>Booty Bay</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>36</td>
      <td>Alterac Mountains</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>37</td>
      <td>Lake Nazferiti</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>38</td>
      <td>Loch Modan</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>40</td>
      <td>Westfall</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>41</td>
      <td>Deadwind Pass</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>42</td>
      <td>Darkshire</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>43</td>
      <td>Wild Shore</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>44</td>
      <td>Redridge Mountains</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>45</td>
      <td>Arathi Highlands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>46</td>
      <td>Burning Steppes</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>47</td>
      <td>The Hinterlands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>49</td>
      <td>Dead Man’s Hole</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>51</td>
      <td>Searing Gorge</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>53</td>
      <td>Thieves Camp</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>54</td>
      <td>Jasperlode Mine</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>55</td>
      <td>Valley of Heroes UNUSED</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>56</td>
      <td>Heroes’ Vigil</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>57</td>
      <td>Fargodeep Mine</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>59</td>
      <td>Northshire Vineyards</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>60</td>
      <td>Forest’s Edge</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>61</td>
      <td>Thunder Falls</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>62</td>
      <td>Brackwell Pumpkin Patch</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>63</td>
      <td>The Stonefield Farm</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>64</td>
      <td>The Maclure Vineyards</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>65</td>
      <td>Dragonblight</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>66</td>
      <td>Zul’Drak</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>67</td>
      <td>The Storm Peaks</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>68</td>
      <td>Lake Everstill</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>69</td>
      <td>Lakeshire</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>70</td>
      <td>Stonewatch</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>71</td>
      <td>Stonewatch Falls</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>72</td>
      <td>The Dark Portal</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>73</td>
      <td>The Tainted Scar</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>74</td>
      <td>Pool of Tears</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>75</td>
      <td>Stonard</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>76</td>
      <td>Fallow Sanctuary</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>77</td>
      <td>Anvilmar</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>80</td>
      <td>Stormwind Mountains</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>81</td>
      <td>Jeff NE Quadrant Changed</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>82</td>
      <td>Jeff NW Quadrant</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>83</td>
      <td>Jeff SE Quadrant</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>84</td>
      <td>Jeff SW Quadrant</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>85</td>
      <td>Tirisfal Glades</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>86</td>
      <td>Stone Cairn Lake</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>87</td>
      <td>Goldshire</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>88</td>
      <td>Eastvale Logging Camp</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>89</td>
      <td>Mirror Lake Orchard</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>91</td>
      <td>Tower of Azora</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>92</td>
      <td>Mirror Lake</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>93</td>
      <td>Vul’Gol Ogre Mound</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>94</td>
      <td>Raven Hill</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>95</td>
      <td>Redridge Canyons</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>96</td>
      <td>Tower of Ilgalar</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>97</td>
      <td>Alther’s Mill</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>98</td>
      <td>Rethban Caverns</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>99</td>
      <td>Rebel Camp</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>100</td>
      <td>Nesingwary’s Expedition</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>101</td>
      <td>Kurzen’s Compound</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>102</td>
      <td>Ruins of Zul’Kunda</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>103</td>
      <td>Ruins of Zul’Mamwe</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>104</td>
      <td>The Vile Reef</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>105</td>
      <td>Mosh’Ogg Ogre Mound</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>106</td>
      <td>The Stockpile</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>107</td>
      <td>Saldean’s Farm</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>108</td>
      <td>Sentinel Hill</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>109</td>
      <td>Furlbrow’s Pumpkin Farm</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>111</td>
      <td>Jangolode Mine</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>113</td>
      <td>Gold Coast Quarry</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>115</td>
      <td>Westfall Lighthouse</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>116</td>
      <td>Misty Valley</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>117</td>
      <td>Grom’gol Base Camp</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>118</td>
      <td>Whelgar’s Excavation Site</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>120</td>
      <td>Westbrook Garrison</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>121</td>
      <td>Tranquil Gardens Cemetery</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>122</td>
      <td>Zuuldaia Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>123</td>
      <td>Bal’lal Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>125</td>
      <td>Kal’ai Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>126</td>
      <td>Tkashi Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>127</td>
      <td>Balia’mah Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>128</td>
      <td>Ziata’jai Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>129</td>
      <td>Mizjah Ruins</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>130</td>
      <td>Silverpine Forest</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>131</td>
      <td>Kharanos</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>132</td>
      <td>Coldridge Valley</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>133</td>
      <td>Gnomeregan</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>134</td>
      <td>Gol’Bolar Quarry</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>135</td>
      <td>Frostmane Hold</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>136</td>
      <td>The Grizzled Den</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>137</td>
      <td>Brewnall Village</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>138</td>
      <td>Misty Pine Refuge</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>139</td>
      <td>Eastern Plaguelands</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>141</td>
      <td>Teldrassil</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>142</td>
      <td>Ironband’s Excavation Site</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>143</td>
      <td>Mo’grosh Stronghold</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>144</td>
      <td>Thelsamar</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>145</td>
      <td>Algaz Gate</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>146</td>
      <td>Stonewrought Dam</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>147</td>
      <td>The Farstrider Lodge</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>148</td>
      <td>Darkshore</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>149</td>
      <td>Silver Stream Mine</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>150</td>
      <td>Menethil Harbor</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>151</td>
      <td>Designer Island</td>
      <td>451</td>
      <td>0</td>
    </tr>
    <tr>
      <td>152</td>
      <td>The Bulwark</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>153</td>
      <td>Ruins of Lordaeron</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>154</td>
      <td>Deathknell</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>155</td>
      <td>Night Web’s Hollow</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>156</td>
      <td>Solliden Farmstead</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>157</td>
      <td>Agamand Mills</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>158</td>
      <td>Agamand Family Crypt</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>159</td>
      <td>Brill</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>160</td>
      <td>Whispering Gardens</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>161</td>
      <td>Terrace of Repose</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>162</td>
      <td>Brightwater Lake</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>163</td>
      <td>Gunther’s Retreat</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>164</td>
      <td>Garren’s Haunt</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>165</td>
      <td>Balnir Farmstead</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>166</td>
      <td>Cold Hearth Manor</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>167</td>
      <td>Crusader Outpost</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>168</td>
      <td>The North Coast</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>169</td>
      <td>Whispering Shore</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>170</td>
      <td>Lordamere Lake</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>172</td>
      <td>Fenris Isle</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>173</td>
      <td>Faol’s Rest</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>186</td>
      <td>Dolanaar</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>187</td>
      <td>Darnassus UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>188</td>
      <td>Shadowglen</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>189</td>
      <td>Steelgrill’s Depot</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>190</td>
      <td>Hearthglen</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>192</td>
      <td>Northridge Lumber Camp</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>193</td>
      <td>Ruins of Andorhal</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>195</td>
      <td>School of Necromancy</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>196</td>
      <td>Uther’s Tomb</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>197</td>
      <td>Sorrow Hill</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>198</td>
      <td>The Weeping Cave</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>199</td>
      <td>Felstone Field</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>200</td>
      <td>Dalson’s Tears</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>201</td>
      <td>Gahrron’s Withering</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>202</td>
      <td>The Writhing Haunt</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>203</td>
      <td>Mardenholde Keep</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>204</td>
      <td>Pyrewood Village</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>205</td>
      <td>Dun Modr</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>206</td>
      <td>Utgarde Keep</td>
      <td>574</td>
      <td>0</td>
    </tr>
    <tr>
      <td>207</td>
      <td>The Great Sea</td>
      <td>36</td>
      <td>0</td>
    </tr>
    <tr>
      <td>208</td>
      <td>Unused Ironcladcove</td>
      <td>36</td>
      <td>0</td>
    </tr>
    <tr>
      <td>209</td>
      <td>Shadowfang Keep</td>
      <td>33</td>
      <td>0</td>
    </tr>
    <tr>
      <td>210</td>
      <td>Icecrown</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>211</td>
      <td>Iceflow Lake</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>212</td>
      <td>Helm’s Bed Lake</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>213</td>
      <td>Deep Elem Mine</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>214</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>215</td>
      <td>Mulgore</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>219</td>
      <td>Alexston Farmstead</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>220</td>
      <td>Red Cloud Mesa</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>221</td>
      <td>Camp Narache</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>222</td>
      <td>Bloodhoof Village</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>223</td>
      <td>Stonebull Lake</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>224</td>
      <td>Ravaged Caravan</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>225</td>
      <td>Red Rocks</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>226</td>
      <td>The Skittering Dark</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>227</td>
      <td>Valgan’s Field</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>228</td>
      <td>The Sepulcher</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>229</td>
      <td>Olsen’s Farthing</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>230</td>
      <td>The Greymane Wall</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>231</td>
      <td>Beren’s Peril</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>232</td>
      <td>The Dawning Isles</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>233</td>
      <td>Ambermill</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>235</td>
      <td>Fenris Keep</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>236</td>
      <td>Shadowfang Keep</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>237</td>
      <td>The Decrepit Ferry</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>238</td>
      <td>Malden’s Orchard</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>239</td>
      <td>The Ivar Patch</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>240</td>
      <td>The Dead Field</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>241</td>
      <td>The Rotting Orchard</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>242</td>
      <td>Brightwood Grove</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>243</td>
      <td>Forlorn Rowe</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>244</td>
      <td>The Whipple Estate</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>245</td>
      <td>The Yorgen Farmstead</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>246</td>
      <td>The Cauldron</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>247</td>
      <td>Grimesilt Dig Site</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>249</td>
      <td>Dreadmaul Rock</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>250</td>
      <td>Ruins of Thaurissan</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>251</td>
      <td>Flame Crest</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>252</td>
      <td>Blackrock Stronghold</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>253</td>
      <td>The Pillar of Ash</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>254</td>
      <td>Blackrock Mountain</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>255</td>
      <td>Altar of Storms</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>256</td>
      <td>Aldrassil</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>257</td>
      <td>Shadowthread Cave</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>258</td>
      <td>Fel Rock</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>259</td>
      <td>Lake Al’Ameth</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>260</td>
      <td>Starbreeze Village</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>261</td>
      <td>Gnarlpine Hold</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>262</td>
      <td>Ban’ethil Barrow Den</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>263</td>
      <td>The Cleft</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>264</td>
      <td>The Oracle Glade</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>265</td>
      <td>Wellspring River</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>266</td>
      <td>Wellspring Lake</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>267</td>
      <td>Hillsbrad Foothills</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>268</td>
      <td>Azshara Crater</td>
      <td>37</td>
      <td>0</td>
    </tr>
    <tr>
      <td>269</td>
      <td>Dun Algaz</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>271</td>
      <td>Southshore</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>272</td>
      <td>Tarren Mill</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>275</td>
      <td>Durnholde Keep</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>276</td>
      <td>UNUSED Stonewrought Pass</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>277</td>
      <td>The Foothill Caverns</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>278</td>
      <td>Lordamere Internment Camp</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>279</td>
      <td>Dalaran Crater</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>280</td>
      <td>Strahnbrad</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>281</td>
      <td>Ruins of Alterac</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>282</td>
      <td>Crushridge Hold</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>283</td>
      <td>Slaughter Hollow</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>284</td>
      <td>The Uplands</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>285</td>
      <td>Southpoint Tower</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>286</td>
      <td>Hillsbrad Fields</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>287</td>
      <td>Hillsbrad</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>288</td>
      <td>Azurelode Mine</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>289</td>
      <td>Nethander Stead</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>290</td>
      <td>Dun Garok</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>293</td>
      <td>Thoradin’s Wall</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>294</td>
      <td>Eastern Strand</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>295</td>
      <td>Western Strand</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>296</td>
      <td>South Seas UNUSED</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>297</td>
      <td>Jaguero Isle</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>298</td>
      <td>Baradin Bay</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>299</td>
      <td>Menethil Bay</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>300</td>
      <td>Misty Reed Strand</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>301</td>
      <td>The Savage Coast</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>302</td>
      <td>The Crystal Shore</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>303</td>
      <td>Shell Beach</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>305</td>
      <td>North Tide’s Run</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>306</td>
      <td>South Tide’s Run</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>307</td>
      <td>The Overlook Cliffs</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>308</td>
      <td>The Forbidding Sea</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>309</td>
      <td>Ironbeard’s Tomb</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>310</td>
      <td>Crystalvein Mine</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>311</td>
      <td>Ruins of Aboraz</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>312</td>
      <td>Janeiro’s Point</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>313</td>
      <td>Northfold Manor</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>314</td>
      <td>Go’Shek Farm</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>315</td>
      <td>Dabyrie’s Farmstead</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>316</td>
      <td>Boulderfist Hall</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>317</td>
      <td>Witherbark Village</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>318</td>
      <td>Drywhisker Gorge</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>320</td>
      <td>Refuge Pointe</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>321</td>
      <td>Hammerfall</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>322</td>
      <td>Blackwater Shipwrecks</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>323</td>
      <td>O’Breen’s Camp</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>324</td>
      <td>Stromgarde Keep</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>325</td>
      <td>The Tower of Arathor</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>326</td>
      <td>The Sanctum</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>327</td>
      <td>Faldir’s Cove</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>328</td>
      <td>The Drowned Reef</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>330</td>
      <td>Thandol Span</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>331</td>
      <td>Ashenvale</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>332</td>
      <td>The Great Sea</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>333</td>
      <td>Circle of East Binding</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>334</td>
      <td>Circle of West Binding</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>335</td>
      <td>Circle of Inner Binding</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>336</td>
      <td>Circle of Outer Binding</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>337</td>
      <td>Apocryphan’s Rest</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>338</td>
      <td>Angor Fortress</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>339</td>
      <td>Lethlor Ravine</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>340</td>
      <td>Kargath</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>341</td>
      <td>Camp Kosh</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>342</td>
      <td>Camp Boff</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>343</td>
      <td>Camp Wurg</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>344</td>
      <td>Camp Cagg</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>345</td>
      <td>Agmond’s End</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>346</td>
      <td>Hammertoe’s Digsite</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>347</td>
      <td>Dustbelch Grotto</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>348</td>
      <td>Aerie Peak</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>349</td>
      <td>Wildhammer Keep</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>350</td>
      <td>Quel’Danil Lodge</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>351</td>
      <td>Skulk Rock</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>352</td>
      <td>Zun’watha</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>353</td>
      <td>Shadra’Alor</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>354</td>
      <td>Jintha’Alor</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>355</td>
      <td>The Altar of Zul</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>356</td>
      <td>Seradane</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>357</td>
      <td>Feralas</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>358</td>
      <td>Brambleblade Ravine</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>359</td>
      <td>Bael Modan</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>360</td>
      <td>The Venture Co. Mine</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>361</td>
      <td>Felwood</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>362</td>
      <td>Razor Hill</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>363</td>
      <td>Valley of Trials</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>364</td>
      <td>The Den</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>365</td>
      <td>Burning Blade Coven</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>366</td>
      <td>Kolkar Crag</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>367</td>
      <td>Sen’jin Village</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>368</td>
      <td>Echo Isles</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>369</td>
      <td>Thunder Ridge</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>370</td>
      <td>Drygulch Ravine</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>371</td>
      <td>Dustwind Cave</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>372</td>
      <td>Tiragarde Keep</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>373</td>
      <td>Scuttle Coast</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>374</td>
      <td>Bladefist Bay</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>375</td>
      <td>Deadeye Shore</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>377</td>
      <td>Southfury River</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>378</td>
      <td>Camp Taurajo</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>379</td>
      <td>Far Watch Post</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>380</td>
      <td>The Crossroads</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>381</td>
      <td>Boulder Lode Mine</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>382</td>
      <td>The Sludge Fen</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>383</td>
      <td>The Dry Hills</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>384</td>
      <td>Dreadmist Peak</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>385</td>
      <td>Northwatch Hold</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>386</td>
      <td>The Forgotten Pools</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>387</td>
      <td>Lushwater Oasis</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>388</td>
      <td>The Stagnant Oasis</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>390</td>
      <td>Field of Giants</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>391</td>
      <td>The Merchant Coast</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>392</td>
      <td>Ratchet</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>393</td>
      <td>Darkspear Strand</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>394</td>
      <td>Grizzly Hills</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>395</td>
      <td>Grizzlemaw</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>396</td>
      <td>Winterhoof Water Well</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>397</td>
      <td>Thunderhorn Water Well</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>398</td>
      <td>Wildmane Water Well</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>399</td>
      <td>Skyline Ridge</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>400</td>
      <td>Thousand Needles</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>401</td>
      <td>The Tidus Stair</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>403</td>
      <td>Shady Rest Inn</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>404</td>
      <td>Bael’dun Digsite</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>405</td>
      <td>Desolace</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>406</td>
      <td>Stonetalon Mountains</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>407</td>
      <td>Orgrimmar UNUSED</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>408</td>
      <td>Gillijim’s Isle</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>409</td>
      <td>Island of Doctor Lapidis</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>410</td>
      <td>Razorwind Canyon</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>411</td>
      <td>Bathran’s Haunt</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>412</td>
      <td>The Ruins of Ordil’Aran</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>413</td>
      <td>Maestra’s Post</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>414</td>
      <td>The Zoram Strand</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>415</td>
      <td>Astranaar</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>416</td>
      <td>The Shrine of Aessina</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>417</td>
      <td>Fire Scar Shrine</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>418</td>
      <td>The Ruins of Stardust</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>419</td>
      <td>The Howling Vale</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>420</td>
      <td>Silverwind Refuge</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>421</td>
      <td>Mystral Lake</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>422</td>
      <td>Fallen Sky Lake</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>424</td>
      <td>Iris Lake</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>425</td>
      <td>Moonwell</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>426</td>
      <td>Raynewood Retreat</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>427</td>
      <td>The Shady Nook</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>428</td>
      <td>Night Run</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>429</td>
      <td>Xavian</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>430</td>
      <td>Satyrnaar</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>431</td>
      <td>Splintertree Post</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>432</td>
      <td>The Dor’Danil Barrow Den</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>433</td>
      <td>Falfarren River</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>434</td>
      <td>Felfire Hill</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>435</td>
      <td>Demon Fall Canyon</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>436</td>
      <td>Demon Fall Ridge</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>437</td>
      <td>Warsong Lumber Camp</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>438</td>
      <td>Bough Shadow</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>439</td>
      <td>The Shimmering Flats</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>440</td>
      <td>Tanaris</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>441</td>
      <td>Lake Falathim</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>442</td>
      <td>Auberdine</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>443</td>
      <td>Ruins of Mathystra</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>444</td>
      <td>Tower of Althalaxx</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>445</td>
      <td>Cliffspring Falls</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>446</td>
      <td>Bashal’Aran</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>447</td>
      <td>Ameth’Aran</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>448</td>
      <td>Grove of the Ancients</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>449</td>
      <td>The Master’s Glaive</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>450</td>
      <td>Remtravel’s Excavation</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>452</td>
      <td>Mist’s Edge</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>453</td>
      <td>The Long Wash</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>454</td>
      <td>Wildbend River</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>455</td>
      <td>Blackwood Den</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>456</td>
      <td>Cliffspring River</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>457</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>458</td>
      <td>Gold Road</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>459</td>
      <td>Scarlet Watch Post</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>460</td>
      <td>Sun Rock Retreat</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>461</td>
      <td>Windshear Crag</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>463</td>
      <td>Cragpool Lake</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>464</td>
      <td>Mirkfallon Lake</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>465</td>
      <td>The Charred Vale</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>466</td>
      <td>Valley of the Bloodfuries</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>467</td>
      <td>Stonetalon Peak</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>468</td>
      <td>The Talon Den</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>469</td>
      <td>Greatwood Vale</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>470</td>
      <td>Thunder Bluff UNUSED</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>471</td>
      <td>Brave Wind Mesa</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>472</td>
      <td>Fire Stone Mesa</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>473</td>
      <td>Mantle Rock</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>474</td>
      <td>Hunter Rise UNUSED</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>475</td>
      <td>Spirit RiseUNUSED</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>476</td>
      <td>Elder RiseUNUSED</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>477</td>
      <td>Ruins of Jubuwal</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>478</td>
      <td>Pools of Arlithrien</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>479</td>
      <td>The Rustmaul Dig Site</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>480</td>
      <td>Camp E’thok</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>481</td>
      <td>Splithoof Crag</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>482</td>
      <td>Highperch</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>483</td>
      <td>The Screeching Canyon</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>484</td>
      <td>Freewind Post</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>485</td>
      <td>The Great Lift</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>486</td>
      <td>Galak Hold</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>487</td>
      <td>Roguefeather Den</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>488</td>
      <td>The Weathered Nook</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>489</td>
      <td>Thalanaar</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>490</td>
      <td>Un’Goro Crater</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>491</td>
      <td>Razorfen Kraul</td>
      <td>47</td>
      <td>0</td>
    </tr>
    <tr>
      <td>492</td>
      <td>Raven Hill Cemetery</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>493</td>
      <td>Moonglade</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>495</td>
      <td>Howling Fjord</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>496</td>
      <td>Brackenwall Village</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>497</td>
      <td>Swamplight Manor</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>498</td>
      <td>Bloodfen Burrow</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>499</td>
      <td>Darkmist Cavern</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>500</td>
      <td>Moggle Point</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>501</td>
      <td>Beezil’s Wreck</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>502</td>
      <td>Witch Hill</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>503</td>
      <td>Sentry Point</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>504</td>
      <td>North Point Tower</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>505</td>
      <td>West Point Tower</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>506</td>
      <td>Lost Point</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>507</td>
      <td>Bluefen</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>508</td>
      <td>Stonemaul Ruins</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>509</td>
      <td>The Den of Flame</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>510</td>
      <td>The Dragonmurk</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>511</td>
      <td>Wyrmbog</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>512</td>
      <td>Blackhoof Village</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>513</td>
      <td>Theramore Isle</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>514</td>
      <td>Foothold Citadel</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>515</td>
      <td>Ironclad Prison</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>516</td>
      <td>Dustwallow Bay</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>517</td>
      <td>Tidefury Cove</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>518</td>
      <td>Dreadmurk Shore</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>536</td>
      <td>Addle’s Stead</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>537</td>
      <td>Fire Plume Ridge</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>538</td>
      <td>Lakkari Tar Pits</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>539</td>
      <td>Terror Run</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>540</td>
      <td>The Slithering Scar</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>541</td>
      <td>Marshal’s Refuge</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>542</td>
      <td>Fungal Rock</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>543</td>
      <td>Golakka Hot Springs</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>556</td>
      <td>The Loch</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>576</td>
      <td>Beggar’s Haunt</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>596</td>
      <td>Kodo Graveyard</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>597</td>
      <td>Ghost Walker Post</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>598</td>
      <td>Sar’theris Strand</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>599</td>
      <td>Thunder Axe Fortress</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>600</td>
      <td>Bolgan’s Hole</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>602</td>
      <td>Mannoroc Coven</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>603</td>
      <td>Sargeron</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>604</td>
      <td>Magram Village</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>606</td>
      <td>Gelkis Village</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>607</td>
      <td>Valley of Spears</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>608</td>
      <td>Nijel’s Point</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>609</td>
      <td>Kolkar Village</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>616</td>
      <td>Hyjal</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>618</td>
      <td>Winterspring</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>636</td>
      <td>Blackwolf River</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>637</td>
      <td>Kodo Rock</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>638</td>
      <td>Hidden Path</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>639</td>
      <td>Spirit Rock</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>640</td>
      <td>Shrine of the Dormant Flame</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>656</td>
      <td>Lake Elune’ara</td>
      <td>1</td>
      <td>493</td>
    </tr>
    <tr>
      <td>657</td>
      <td>The Harborage</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>676</td>
      <td>Outland</td>
      <td>150</td>
      <td>0</td>
    </tr>
    <tr>
      <td>696</td>
      <td>Craftsmen’s Terrace UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>697</td>
      <td>Tradesmen’s Terrace UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>698</td>
      <td>The Temple Gardens UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>699</td>
      <td>Temple of Elune UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>700</td>
      <td>Cenarion Enclave UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>701</td>
      <td>Warrior’s Terrace UNUSED</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>702</td>
      <td>Rut’theran Village</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>716</td>
      <td>Ironband’s Compound</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>717</td>
      <td>The Stockade</td>
      <td>34</td>
      <td>0</td>
    </tr>
    <tr>
      <td>718</td>
      <td>Wailing Caverns</td>
      <td>43</td>
      <td>0</td>
    </tr>
    <tr>
      <td>719</td>
      <td>Blackfathom Deeps</td>
      <td>48</td>
      <td>0</td>
    </tr>
    <tr>
      <td>720</td>
      <td>Fray Island</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>721</td>
      <td>Gnomeregan</td>
      <td>90</td>
      <td>0</td>
    </tr>
    <tr>
      <td>722</td>
      <td>Razorfen Downs</td>
      <td>129</td>
      <td>0</td>
    </tr>
    <tr>
      <td>736</td>
      <td>Ban’ethil Hollow</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>796</td>
      <td>Scarlet Monastery</td>
      <td>189</td>
      <td>0</td>
    </tr>
    <tr>
      <td>797</td>
      <td>Jerod’s Landing</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>798</td>
      <td>Ridgepoint Tower</td>
      <td>0</td>
      <td>12</td>
    </tr>
    <tr>
      <td>799</td>
      <td>The Darkened Bank</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>800</td>
      <td>Coldridge Pass</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>801</td>
      <td>Chill Breeze Valley</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>802</td>
      <td>Shimmer Ridge</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>803</td>
      <td>Amberstill Ranch</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>804</td>
      <td>The Tundrid Hills</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>805</td>
      <td>South Gate Pass</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>806</td>
      <td>South Gate Outpost</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>807</td>
      <td>North Gate Pass</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>808</td>
      <td>North Gate Outpost</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>809</td>
      <td>Gates of Ironforge</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>810</td>
      <td>Stillwater Pond</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>811</td>
      <td>Nightmare Vale</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>812</td>
      <td>Venomweb Vale</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>813</td>
      <td>The Bulwark</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>814</td>
      <td>Southfury River</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>815</td>
      <td>Southfury River</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>816</td>
      <td>Razormane Grounds</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>817</td>
      <td>Skull Rock</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>818</td>
      <td>Palemane Rock</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>819</td>
      <td>Windfury Ridge</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>820</td>
      <td>The Golden Plains</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>821</td>
      <td>The Rolling Plains</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>836</td>
      <td>Dun Algaz</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>837</td>
      <td>Dun Algaz</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>838</td>
      <td>North Gate Pass</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>839</td>
      <td>South Gate Pass</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>856</td>
      <td>Twilight Grove</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>876</td>
      <td>GM Island</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>877</td>
      <td>Delete ME</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>878</td>
      <td>Southfury River</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>879</td>
      <td>Southfury River</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>880</td>
      <td>Thandol Span</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>881</td>
      <td>Thandol Span</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>896</td>
      <td>Purgation Isle</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>916</td>
      <td>The Jansen Stead</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>917</td>
      <td>The Dead Acre</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>918</td>
      <td>The Molsen Farm</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>919</td>
      <td>Stendel’s Pond</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>920</td>
      <td>The Dagger Hills</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>921</td>
      <td>Demont’s Place</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>922</td>
      <td>The Dust Plains</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>923</td>
      <td>Stonesplinter Valley</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>924</td>
      <td>Valley of Kings</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>925</td>
      <td>Algaz Station</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>926</td>
      <td>Bucklebree Farm</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>927</td>
      <td>The Shining Strand</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>928</td>
      <td>North Tide’s Hollow</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>936</td>
      <td>Grizzlepaw Ridge</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>956</td>
      <td>The Verdant Fields</td>
      <td>169</td>
      <td>0</td>
    </tr>
    <tr>
      <td>976</td>
      <td>Gadgetzan</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>977</td>
      <td>Steamwheedle Port</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>978</td>
      <td>Zul’Farrak</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>979</td>
      <td>Sandsorrow Watch</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>980</td>
      <td>Thistleshrub Valley</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>981</td>
      <td>The Gaping Chasm</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>982</td>
      <td>The Noxious Lair</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>983</td>
      <td>Dunemaul Compound</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>984</td>
      <td>Eastmoon Ruins</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>985</td>
      <td>Waterspring Field</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>986</td>
      <td>Zalashji’s Den</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>987</td>
      <td>Land’s End Beach</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>988</td>
      <td>Wavestrider Beach</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>989</td>
      <td>Uldum</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>990</td>
      <td>Valley of the Watchers</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>991</td>
      <td>Gunstan’s Post</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>992</td>
      <td>Southmoon Ruins</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>996</td>
      <td>Render’s Camp</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>997</td>
      <td>Render’s Valley</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>998</td>
      <td>Render’s Rock</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>999</td>
      <td>Stonewatch Tower</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>1000</td>
      <td>Galardell Valley</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>1001</td>
      <td>Lakeridge Highway</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>1002</td>
      <td>Three Corners</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>1016</td>
      <td>Direforge Hill</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1017</td>
      <td>Raptor Ridge</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1018</td>
      <td>Black Channel Marsh</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1019</td>
      <td>The Green Belt</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>1020</td>
      <td>Mosshide Fen</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1021</td>
      <td>Thelgen Rock</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1022</td>
      <td>Bluegill Marsh</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1023</td>
      <td>Saltspray Glen</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1024</td>
      <td>Sundown Marsh</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1025</td>
      <td>The Green Belt</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1036</td>
      <td>Angerfang Encampment</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1037</td>
      <td>Grim Batol</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1038</td>
      <td>Dragonmaw Gates</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1039</td>
      <td>The Lost Fleet</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>1056</td>
      <td>Darrow Hill</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>1057</td>
      <td>Thoradin’s Wall</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>1076</td>
      <td>Webwinder Path</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>1097</td>
      <td>The Hushed Bank</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>1098</td>
      <td>Manor Mistmantle</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>1099</td>
      <td>Camp Mojache</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1100</td>
      <td>Grimtotem Compound</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1101</td>
      <td>The Writhing Deep</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1102</td>
      <td>Wildwind Lake</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1103</td>
      <td>Gordunni Outpost</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1104</td>
      <td>Mok’Gordun</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1105</td>
      <td>Feral Scar Vale</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1106</td>
      <td>Frayfeather Highlands</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1107</td>
      <td>Idlewind Lake</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1108</td>
      <td>The Forgotten Coast</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1109</td>
      <td>East Pillar</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1110</td>
      <td>West Pillar</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1111</td>
      <td>Dream Bough</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1112</td>
      <td>Jademir Lake</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1113</td>
      <td>Oneiros</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1114</td>
      <td>Ruins of Ravenwind</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1115</td>
      <td>Rage Scar Hold</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1116</td>
      <td>Feathermoon Stronghold</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1117</td>
      <td>Ruins of Solarsal</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1118</td>
      <td>Lower Wilds UNUSED</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1119</td>
      <td>The Twin Colossals</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1120</td>
      <td>Sardor Isle</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1121</td>
      <td>Isle of Dread</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1136</td>
      <td>High Wilderness</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1137</td>
      <td>Lower Wilds</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>1156</td>
      <td>Southern Barrens</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1157</td>
      <td>Southern Gold Road</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1176</td>
      <td>Zul’Farrak</td>
      <td>209</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1196</td>
      <td>Utgarde Pinnacle</td>
      <td>575</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1216</td>
      <td>Timbermaw Hold</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1217</td>
      <td>Vanndir Encampment</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1218</td>
      <td>TESTAzshara</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1219</td>
      <td>Legash Encampment</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1220</td>
      <td>Thalassian Base Camp</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1221</td>
      <td>Ruins of Eldarath</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1222</td>
      <td>Hetaera’s Clutch</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1223</td>
      <td>Temple of Zin-Malor</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1224</td>
      <td>Bear’s Head</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1225</td>
      <td>Ursolan</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1226</td>
      <td>Temple of Arkkoran</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1227</td>
      <td>Bay of Storms</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1228</td>
      <td>The Shattered Strand</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1229</td>
      <td>Tower of Eldara</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1230</td>
      <td>Jagged Reef</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1231</td>
      <td>Southridge Beach</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1232</td>
      <td>Ravencrest Monument</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1233</td>
      <td>Forlorn Ridge</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1234</td>
      <td>Lake Mennar</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1235</td>
      <td>Shadowsong Shrine</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1236</td>
      <td>Haldarr Encampment</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1237</td>
      <td>Valormok</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1256</td>
      <td>The Ruined Reaches</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>1276</td>
      <td>The Talondeep Path</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>1277</td>
      <td>The Talondeep Path</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>1296</td>
      <td>Rocktusk Farm</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>1297</td>
      <td>Jaggedswine Farm</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>1316</td>
      <td>Razorfen Downs</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1336</td>
      <td>Lost Rigger Cove</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>1337</td>
      <td>Uldaman</td>
      <td>70</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1338</td>
      <td>Lordamere Lake</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>1339</td>
      <td>Lordamere Lake</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1357</td>
      <td>Gallows’ Corner</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1377</td>
      <td>Silithus</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1397</td>
      <td>Emerald Forest</td>
      <td>169</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1417</td>
      <td>Sunken Temple</td>
      <td>109</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1437</td>
      <td>Dreadmaul Hold</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1438</td>
      <td>Nethergarde Keep</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1439</td>
      <td>Dreadmaul Post</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1440</td>
      <td>Serpent’s Coil</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1441</td>
      <td>Altar of Storms</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1442</td>
      <td>Firewatch Ridge</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1443</td>
      <td>The Slag Pit</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1444</td>
      <td>The Sea of Cinders</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1445</td>
      <td>Blackrock Mountain</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1446</td>
      <td>Thorium Point</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1457</td>
      <td>Garrison Armory</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>1477</td>
      <td>The Temple of Atal’Hakkar</td>
      <td>109</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1497</td>
      <td>Undercity</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1517</td>
      <td>Uldaman</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1518</td>
      <td>Not Used Deadmines</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>1519</td>
      <td>Stormwind City</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1537</td>
      <td>Ironforge</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1557</td>
      <td>Splithoof Hold</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>1577</td>
      <td>The Cape of Stranglethorn</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1578</td>
      <td>Southern Savage Coast</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1579</td>
      <td>Unused The Deadmines 002</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1580</td>
      <td>Unused Ironclad Cove 003</td>
      <td>0</td>
      <td>1579</td>
    </tr>
    <tr>
      <td>1581</td>
      <td>The Deadmines</td>
      <td>36</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1582</td>
      <td>Ironclad Cove</td>
      <td>36</td>
      <td>1581</td>
    </tr>
    <tr>
      <td>1583</td>
      <td>Blackrock Spire</td>
      <td>229</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1584</td>
      <td>Blackrock Depths</td>
      <td>230</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1597</td>
      <td>Raptor Grounds UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1598</td>
      <td>Grol’dom Farm UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1599</td>
      <td>Mor’shan Base Camp</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1600</td>
      <td>Honor’s Stand UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1601</td>
      <td>Blackthorn Ridge UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1602</td>
      <td>Bramblescar UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1603</td>
      <td>Agama’gor UNUSED</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1617</td>
      <td>Valley of Heroes</td>
      <td>0</td>
      <td>1519</td>
    </tr>
    <tr>
      <td>1637</td>
      <td>Orgrimmar</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1638</td>
      <td>Thunder Bluff</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1639</td>
      <td>Elder Rise</td>
      <td>1</td>
      <td>1638</td>
    </tr>
    <tr>
      <td>1640</td>
      <td>Spirit Rise</td>
      <td>1</td>
      <td>1638</td>
    </tr>
    <tr>
      <td>1641</td>
      <td>Hunter Rise</td>
      <td>1</td>
      <td>1638</td>
    </tr>
    <tr>
      <td>1657</td>
      <td>Darnassus</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1658</td>
      <td>Cenarion Enclave</td>
      <td>1</td>
      <td>1657</td>
    </tr>
    <tr>
      <td>1659</td>
      <td>Craftsmen’s Terrace</td>
      <td>1</td>
      <td>1657</td>
    </tr>
    <tr>
      <td>1660</td>
      <td>Warrior’s Terrace</td>
      <td>1</td>
      <td>1657</td>
    </tr>
    <tr>
      <td>1661</td>
      <td>The Temple Gardens</td>
      <td>1</td>
      <td>1657</td>
    </tr>
    <tr>
      <td>1662</td>
      <td>Tradesmen’s Terrace</td>
      <td>1</td>
      <td>1657</td>
    </tr>
    <tr>
      <td>1677</td>
      <td>Gavin’s Naze</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1678</td>
      <td>Sofera’s Naze</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1679</td>
      <td>Corrahn’s Dagger</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1680</td>
      <td>The Headland</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1681</td>
      <td>Misty Shore</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1682</td>
      <td>Dandred’s Fold</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1683</td>
      <td>Growless Cave</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1684</td>
      <td>Chillwind Point</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>1697</td>
      <td>Raptor Grounds</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1698</td>
      <td>Bramblescar</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1699</td>
      <td>Thorn Hill</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1700</td>
      <td>Agama’gor</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1701</td>
      <td>Blackthorn Ridge</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1702</td>
      <td>Honor’s Stand</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1703</td>
      <td>The Mor’shan Rampart</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1704</td>
      <td>Grol’dom Farm</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1717</td>
      <td>Razorfen Kraul</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1718</td>
      <td>The Great Lift</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>1737</td>
      <td>Mistvale Valley</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1738</td>
      <td>Nek’mani Wellspring</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1739</td>
      <td>Bloodsail Compound</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1740</td>
      <td>Venture Co. Base Camp</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1741</td>
      <td>Gurubashi Arena</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1742</td>
      <td>Spirit Den</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1757</td>
      <td>The Crimson Veil</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1758</td>
      <td>The Riptide</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1759</td>
      <td>The Damsel’s Luck</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1760</td>
      <td>Venture Co. Operations Center</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>1761</td>
      <td>Deadwood Village</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1762</td>
      <td>Felpaw Village</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1763</td>
      <td>Jaedenar</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1764</td>
      <td>Bloodvenom River</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1765</td>
      <td>Bloodvenom Falls</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1766</td>
      <td>Shatter Scar Vale</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1767</td>
      <td>Irontree Woods</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1768</td>
      <td>Irontree Cavern</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1769</td>
      <td>Timbermaw Hold</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1770</td>
      <td>Shadow Hold</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1771</td>
      <td>Shrine of the Deceiver</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1777</td>
      <td>Itharius’s Cave</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1778</td>
      <td>Sorrowmurk</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1779</td>
      <td>Draenil’dur Village</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1780</td>
      <td>Splinterspear Junction</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1797</td>
      <td>Stagalbog</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1798</td>
      <td>The Shifting Mire</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1817</td>
      <td>Stagalbog Cave</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1837</td>
      <td>Witherbark Caverns</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>1857</td>
      <td>Thoradin’s Wall</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>1858</td>
      <td>Boulder’gor</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>1877</td>
      <td>Valley of Fangs</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1878</td>
      <td>The Dustbowl</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1879</td>
      <td>Mirage Flats</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1880</td>
      <td>Featherbeard’s Hovel</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1881</td>
      <td>Shindigger’s Camp</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1882</td>
      <td>Plaguemist Ravine</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1883</td>
      <td>Valorwind Lake</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1884</td>
      <td>Agol’watha</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1885</td>
      <td>Hiri’watha</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1886</td>
      <td>The Creeping Ruin</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1887</td>
      <td>Bogen’s Ledge</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1897</td>
      <td>The Maker’s Terrace</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1898</td>
      <td>Dustwind Gulch</td>
      <td>0</td>
      <td>3</td>
    </tr>
    <tr>
      <td>1917</td>
      <td>Shaol’watha</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>1937</td>
      <td>Noonshade Ruins</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>1938</td>
      <td>Broken Pillar</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>1939</td>
      <td>Abyssal Sands</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>1940</td>
      <td>Southbreak Shore</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>1941</td>
      <td>Caverns of Time</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1942</td>
      <td>The Marshlands</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>1943</td>
      <td>Ironstone Plateau</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>1957</td>
      <td>Blackchar Cave</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1958</td>
      <td>Tanner Camp</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1959</td>
      <td>Dustfire Valley</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>1977</td>
      <td>Zul’Gurub</td>
      <td>309</td>
      <td>0</td>
    </tr>
    <tr>
      <td>1978</td>
      <td>Misty Reed Post</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>1997</td>
      <td>Bloodvenom Post</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>1998</td>
      <td>Talonbranch Glade</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2017</td>
      <td>Stratholme</td>
      <td>329</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2037</td>
      <td>Quel’thalas</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2057</td>
      <td>Scholomance</td>
      <td>289</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2077</td>
      <td>Twilight Vale</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>2078</td>
      <td>Twilight Shore</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>2079</td>
      <td>Alcaz Island</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>2097</td>
      <td>Darkcloud Pinnacle</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2098</td>
      <td>Dawning Wood Catacombs</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>2099</td>
      <td>Stonewatch Keep</td>
      <td>0</td>
      <td>44</td>
    </tr>
    <tr>
      <td>2100</td>
      <td>Maraudon</td>
      <td>349</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2101</td>
      <td>Stoutlager Inn</td>
      <td>0</td>
      <td>38</td>
    </tr>
    <tr>
      <td>2102</td>
      <td>Thunderbrew Distillery</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <td>2103</td>
      <td>Menethil Keep</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>2104</td>
      <td>Deepwater Tavern</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>2117</td>
      <td>Shadow Grave</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>2118</td>
      <td>Brill Town Hall</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>2119</td>
      <td>Gallows’ End Tavern</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>2137</td>
      <td>The Pools of VisionUNUSED</td>
      <td>1</td>
      <td>215</td>
    </tr>
    <tr>
      <td>2138</td>
      <td>Dreadmist Den</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>2157</td>
      <td>Bael’dun Keep</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>2158</td>
      <td>Emberstrife’s Den</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>2159</td>
      <td>Onyxia’s Lair</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2160</td>
      <td>Windshear Mine</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2161</td>
      <td>Roland’s Doom</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <td>2177</td>
      <td>Battle Ring</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>2197</td>
      <td>The Pools of Vision</td>
      <td>1</td>
      <td>1638</td>
    </tr>
    <tr>
      <td>2198</td>
      <td>Shadowbreak Ravine</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2217</td>
      <td>Broken Spear Village</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2237</td>
      <td>Whitereach Post</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2238</td>
      <td>Gornia</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2239</td>
      <td>Zane’s Eye Crater</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2240</td>
      <td>Mirage Raceway</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2241</td>
      <td>Frostsaber Rock</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2242</td>
      <td>The Hidden Grove</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2243</td>
      <td>Timbermaw Post</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2244</td>
      <td>Winterfall Village</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2245</td>
      <td>Mazthoril</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2246</td>
      <td>Frostfire Hot Springs</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2247</td>
      <td>Ice Thistle Hills</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2248</td>
      <td>Dun Mandarr</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2249</td>
      <td>Frostwhisper Gorge</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2250</td>
      <td>Owl Wing Thicket</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2251</td>
      <td>Lake Kel’Theril</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2252</td>
      <td>The Ruins of Kel’Theril</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2253</td>
      <td>Starfall Village</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2254</td>
      <td>Ban’Thallow Barrow Den</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2255</td>
      <td>Everlook</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2256</td>
      <td>Darkwhisper Gorge</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>2257</td>
      <td>Deeprun Tram</td>
      <td>369</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2258</td>
      <td>The Fungal Vale</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2259</td>
      <td>UNUSEDThe Marris Stead</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2260</td>
      <td>The Marris Stead</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2261</td>
      <td>The Undercroft</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2262</td>
      <td>Darrowshire</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2263</td>
      <td>Crown Guard Tower</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2264</td>
      <td>Corin’s Crossing</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2265</td>
      <td>Scarlet Base Camp</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2266</td>
      <td>Tyr’s Hand</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2267</td>
      <td>The Scarlet Basilica</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2268</td>
      <td>Light’s Hope Chapel</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2269</td>
      <td>Browman Mill</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2270</td>
      <td>The Noxious Glade</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2271</td>
      <td>Eastwall Tower</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2272</td>
      <td>Northdale</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2273</td>
      <td>Zul’Mashar</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2274</td>
      <td>Mazra’Alor</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2275</td>
      <td>Northpass Tower</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2276</td>
      <td>Quel’Lithien Lodge</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2277</td>
      <td>Plaguewood</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2278</td>
      <td>Scourgehold</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2279</td>
      <td>Stratholme</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2280</td>
      <td>DO NOT USE</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2297</td>
      <td>Darrowmere Lake</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>2298</td>
      <td>Caer Darrow</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>2299</td>
      <td>Darrowmere Lake</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2300</td>
      <td>Caverns of Time</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>2301</td>
      <td>Thistlefur Village</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2302</td>
      <td>The Quagmire</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>2303</td>
      <td>Windbreak Canyon</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>2317</td>
      <td>South Seas</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>2318</td>
      <td>The Great Sea</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>2319</td>
      <td>The Great Sea</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>2320</td>
      <td>The Great Sea</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>2321</td>
      <td>The Great Sea</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>2322</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>141</td>
    </tr>
    <tr>
      <td>2323</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2324</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2325</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2326</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>148</td>
    </tr>
    <tr>
      <td>2337</td>
      <td>Razor Hill Barracks</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>2338</td>
      <td>South Seas</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>2339</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>2357</td>
      <td>Bloodtooth Camp</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2358</td>
      <td>Forest Song</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2359</td>
      <td>Greenpaw Village</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2360</td>
      <td>Silverwing Outpost</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2361</td>
      <td>Nighthaven</td>
      <td>1</td>
      <td>493</td>
    </tr>
    <tr>
      <td>2362</td>
      <td>Shrine of Remulos</td>
      <td>1</td>
      <td>493</td>
    </tr>
    <tr>
      <td>2363</td>
      <td>Stormrage Barrow Dens</td>
      <td>1</td>
      <td>493</td>
    </tr>
    <tr>
      <td>2364</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>2365</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>2366</td>
      <td>The Black Morass</td>
      <td>269</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2367</td>
      <td>Old Hillsbrad Foothills</td>
      <td>560</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2368</td>
      <td>Tarren Mill</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2369</td>
      <td>Southshore</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2370</td>
      <td>Durnholde Keep</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2371</td>
      <td>Dun Garok</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2372</td>
      <td>Hillsbrad Fields</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2373</td>
      <td>Eastern Strand</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2374</td>
      <td>Nethander Stead</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2375</td>
      <td>Darrow Hill</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2376</td>
      <td>Southpoint Tower</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2377</td>
      <td>Thoradin’s Wall</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2378</td>
      <td>Western Strand</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2379</td>
      <td>Azurelode Mine</td>
      <td>560</td>
      <td>2367</td>
    </tr>
    <tr>
      <td>2397</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>2398</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>130</td>
    </tr>
    <tr>
      <td>2399</td>
      <td>The Great Sea</td>
      <td>0</td>
      <td>85</td>
    </tr>
    <tr>
      <td>2400</td>
      <td>The Forbidding Sea</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>2401</td>
      <td>The Forbidding Sea</td>
      <td>0</td>
      <td>45</td>
    </tr>
    <tr>
      <td>2402</td>
      <td>The Forbidding Sea</td>
      <td>0</td>
      <td>11</td>
    </tr>
    <tr>
      <td>2403</td>
      <td>The Forbidding Sea</td>
      <td>0</td>
      <td>8</td>
    </tr>
    <tr>
      <td>2404</td>
      <td>Tethris Aran</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2405</td>
      <td>Ethel Rethor</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2406</td>
      <td>Ranazjar Isle</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2407</td>
      <td>Kormek’s Hut</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2408</td>
      <td>Shadowprey Village</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2417</td>
      <td>Blackrock Pass</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>2418</td>
      <td>Morgan’s Vigil</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>2419</td>
      <td>Slither Rock</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>2420</td>
      <td>Terror Wing Path</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>2421</td>
      <td>Draco’dar</td>
      <td>0</td>
      <td>46</td>
    </tr>
    <tr>
      <td>2437</td>
      <td>Ragefire Chasm</td>
      <td>389</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2457</td>
      <td>Nightsong Woods</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2477</td>
      <td>The Veiled Sea</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2478</td>
      <td>Morlos’Aran</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2479</td>
      <td>Emerald Sanctuary</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2480</td>
      <td>Jadefire Glen</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2481</td>
      <td>Ruins of Constellas</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2497</td>
      <td>Bitter Reaches</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>2517</td>
      <td>Rise of the Defiler</td>
      <td>0</td>
      <td>4</td>
    </tr>
    <tr>
      <td>2518</td>
      <td>Lariss Pavilion</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2519</td>
      <td>Woodpaw Hills</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2520</td>
      <td>Woodpaw Den</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2521</td>
      <td>Verdantis River</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2522</td>
      <td>Ruins of Isildien</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2537</td>
      <td>Grimtotem Post</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2538</td>
      <td>Camp Aparaje</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2539</td>
      <td>Malaka’jin</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2540</td>
      <td>Boulderslide Ravine</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2541</td>
      <td>Sishir Canyon</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>2557</td>
      <td>Dire Maul</td>
      <td>429</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2558</td>
      <td>Deadwind Ravine</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2559</td>
      <td>Diamondhead River</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2560</td>
      <td>Ariden’s Camp</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2561</td>
      <td>The Vice</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2562</td>
      <td>Karazhan</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2563</td>
      <td>Morgan’s Plot</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2577</td>
      <td>Dire Maul</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>2597</td>
      <td>Alterac Valley</td>
      <td>30</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2617</td>
      <td>Scrabblescrew’s Camp</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2618</td>
      <td>Jadefire Run</td>
      <td>1</td>
      <td>361</td>
    </tr>
    <tr>
      <td>2619</td>
      <td>Thondroril River</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2620</td>
      <td>Thondroril River</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>2621</td>
      <td>Lake Mereldar</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2622</td>
      <td>Pestilent Scar</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2623</td>
      <td>The Infectis Scar</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2624</td>
      <td>Blackwood Lake</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2625</td>
      <td>Eastwall Gate</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2626</td>
      <td>Terrorweb Tunnel</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2627</td>
      <td>Terrordale</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>2637</td>
      <td>Kargathia Keep</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2657</td>
      <td>Valley of Bones</td>
      <td>1</td>
      <td>405</td>
    </tr>
    <tr>
      <td>2677</td>
      <td>Blackwing Lair</td>
      <td>469</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2697</td>
      <td>Deadman’s Crossing</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2717</td>
      <td>Molten Core</td>
      <td>409</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2737</td>
      <td>The Scarab Wall</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2738</td>
      <td>Southwind Village</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2739</td>
      <td>Twilight Base Camp</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2740</td>
      <td>The Crystal Vale</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2741</td>
      <td>The Scarab Dais</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2742</td>
      <td>Hive’Ashi</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2743</td>
      <td>Hive’Zora</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2744</td>
      <td>Hive’Regal</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>2757</td>
      <td>Shrine of the Fallen Warrior</td>
      <td>1</td>
      <td>17</td>
    </tr>
    <tr>
      <td>2777</td>
      <td>UNUSED Alterac Valley</td>
      <td>0</td>
      <td>267</td>
    </tr>
    <tr>
      <td>2797</td>
      <td>Blackfathom Deeps</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2817</td>
      <td>Crystalsong Forest</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2837</td>
      <td>The Master’s Cellar</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2838</td>
      <td>Stonewrought Pass</td>
      <td>0</td>
      <td>51</td>
    </tr>
    <tr>
      <td>2839</td>
      <td>Alterac Valley</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>2857</td>
      <td>The Rumble Cage</td>
      <td>1</td>
      <td>440</td>
    </tr>
    <tr>
      <td>2877</td>
      <td>Chunk Test</td>
      <td>451</td>
      <td>22</td>
    </tr>
    <tr>
      <td>2897</td>
      <td>Zoram’gar Outpost</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>2917</td>
      <td>Hall of Legends</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2918</td>
      <td>Champions’ Hall</td>
      <td>449</td>
      <td>0</td>
    </tr>
    <tr>
      <td>2937</td>
      <td>Grosh’gok Compound</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2938</td>
      <td>Sleeping Gorge</td>
      <td>0</td>
      <td>41</td>
    </tr>
    <tr>
      <td>2957</td>
      <td>Irondeep Mine</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2958</td>
      <td>Stonehearth Outpost</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2959</td>
      <td>Dun Baldar</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2960</td>
      <td>Icewing Pass</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2961</td>
      <td>Frostwolf Village</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2962</td>
      <td>Tower Point</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2963</td>
      <td>Coldtooth Mine</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2964</td>
      <td>Winterax Hold</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2977</td>
      <td>Iceblood Garrison</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2978</td>
      <td>Frostwolf Keep</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>2979</td>
      <td>Tor’kren Farm</td>
      <td>1</td>
      <td>14</td>
    </tr>
    <tr>
      <td>3017</td>
      <td>Frost Dagger Pass</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3037</td>
      <td>Ironstone Camp</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>3038</td>
      <td>Weazel’s Crater</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>3039</td>
      <td>Tahonda Ruins</td>
      <td>1</td>
      <td>400</td>
    </tr>
    <tr>
      <td>3057</td>
      <td>Field of Strife</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3058</td>
      <td>Icewing Cavern</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3077</td>
      <td>Valor’s Rest</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3097</td>
      <td>The Swarming Pillar</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3098</td>
      <td>Twilight Post</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3099</td>
      <td>Twilight Outpost</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3100</td>
      <td>Ravaged Twilight Camp</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3117</td>
      <td>Shalzaru’s Lair</td>
      <td>1</td>
      <td>357</td>
    </tr>
    <tr>
      <td>3137</td>
      <td>Talrendis Point</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>3138</td>
      <td>Rethress Sanctum</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>3139</td>
      <td>Moon Horror Den</td>
      <td>1</td>
      <td>618</td>
    </tr>
    <tr>
      <td>3140</td>
      <td>Scalebeard’s Cave</td>
      <td>1</td>
      <td>16</td>
    </tr>
    <tr>
      <td>3157</td>
      <td>Boulderslide Cavern</td>
      <td>1</td>
      <td>406</td>
    </tr>
    <tr>
      <td>3177</td>
      <td>Warsong Labor Camp</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>3197</td>
      <td>Chillwind Camp</td>
      <td>0</td>
      <td>28</td>
    </tr>
    <tr>
      <td>3217</td>
      <td>The Maul</td>
      <td>429</td>
      <td>2557</td>
    </tr>
    <tr>
      <td>3237</td>
      <td>The Maul UNUSED</td>
      <td>429</td>
      <td>2557</td>
    </tr>
    <tr>
      <td>3257</td>
      <td>Bones of Grakkarond</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3277</td>
      <td>Warsong Gulch</td>
      <td>489</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3297</td>
      <td>Frostwolf Graveyard</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3298</td>
      <td>Frostwolf Pass</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3299</td>
      <td>Dun Baldar Pass</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3300</td>
      <td>Iceblood Graveyard</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3301</td>
      <td>Snowfall Graveyard</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3302</td>
      <td>Stonehearth Graveyard</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3303</td>
      <td>Stormpike Graveyard</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3304</td>
      <td>Icewing Bunker</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3305</td>
      <td>Stonehearth Bunker</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3306</td>
      <td>Wildpaw Ridge</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3317</td>
      <td>Revantusk Village</td>
      <td>0</td>
      <td>47</td>
    </tr>
    <tr>
      <td>3318</td>
      <td>Rock of Durotan</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3319</td>
      <td>Silverwing Grove</td>
      <td>1</td>
      <td>331</td>
    </tr>
    <tr>
      <td>3320</td>
      <td>Warsong Lumber Mill</td>
      <td>489</td>
      <td>3277</td>
    </tr>
    <tr>
      <td>3321</td>
      <td>Silverwing Hold</td>
      <td>489</td>
      <td>3277</td>
    </tr>
    <tr>
      <td>3337</td>
      <td>Wildpaw Cavern</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3338</td>
      <td>The Veiled Cleft</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>3357</td>
      <td>Yojamba Isle</td>
      <td>0</td>
      <td>33</td>
    </tr>
    <tr>
      <td>3358</td>
      <td>Arathi Basin</td>
      <td>529</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3377</td>
      <td>The Coil</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3378</td>
      <td>Altar of Hir’eek</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3379</td>
      <td>Shadra’zaar</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3380</td>
      <td>Hakkari Grounds</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3381</td>
      <td>Naze of Shirvallah</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3382</td>
      <td>Temple of Bethekk</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3383</td>
      <td>The Bloodfire Pit</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3384</td>
      <td>Altar of the Blood God</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3397</td>
      <td>Zanza’s Rise</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3398</td>
      <td>Edge of Madness</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3417</td>
      <td>Trollbane Hall</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3418</td>
      <td>Defiler’s Den</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3419</td>
      <td>Pagle’s Pointe</td>
      <td>309</td>
      <td>1977</td>
    </tr>
    <tr>
      <td>3420</td>
      <td>Farm</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3421</td>
      <td>Blacksmith</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3422</td>
      <td>Lumber Mill</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3423</td>
      <td>Gold Mine</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3424</td>
      <td>Stables</td>
      <td>529</td>
      <td>3358</td>
    </tr>
    <tr>
      <td>3425</td>
      <td>Cenarion Hold</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3426</td>
      <td>Staghelm Point</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3427</td>
      <td>Bronzebeard Encampment</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3428</td>
      <td>Ahn’Qiraj</td>
      <td>531</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3429</td>
      <td>Ruins of Ahn’Qiraj</td>
      <td>509</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3430</td>
      <td>Eversong Woods</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3431</td>
      <td>Sunstrider Isle</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3432</td>
      <td>Shrine of Dath’Remar</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3433</td>
      <td>Ghostlands</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3434</td>
      <td>Scarab Terrace</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3435</td>
      <td>General’s Terrace</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3436</td>
      <td>The Reservoir</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3437</td>
      <td>The Hatchery</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3438</td>
      <td>The Comb</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3439</td>
      <td>Watchers’ Terrace</td>
      <td>531</td>
      <td>3428</td>
    </tr>
    <tr>
      <td>3440</td>
      <td>Scarab Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3441</td>
      <td>General’s Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3442</td>
      <td>The Reservoir</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3443</td>
      <td>The Hatchery</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3444</td>
      <td>The Comb</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3445</td>
      <td>Watchers’ Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3446</td>
      <td>Twilight’s Run</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3447</td>
      <td>Ortell’s Hideout</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3448</td>
      <td>Scarab Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3449</td>
      <td>General’s Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3450</td>
      <td>The Reservoir</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3451</td>
      <td>The Hatchery</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3452</td>
      <td>The Comb</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3453</td>
      <td>Watchers’ Terrace</td>
      <td>509</td>
      <td>3429</td>
    </tr>
    <tr>
      <td>3454</td>
      <td>Ruins of Ahn’Qiraj</td>
      <td>1</td>
      <td>1377</td>
    </tr>
    <tr>
      <td>3455</td>
      <td>The North Sea</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3456</td>
      <td>Naxxramas</td>
      <td>533</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3457</td>
      <td>Karazhan</td>
      <td>532</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3459</td>
      <td>City</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3460</td>
      <td>Golden Strand</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3461</td>
      <td>Sunsail Anchorage</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3462</td>
      <td>Fairbreeze Village</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3463</td>
      <td>Magisters Gate</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3464</td>
      <td>Farstrider Retreat</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3465</td>
      <td>North Sanctum</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3466</td>
      <td>West Sanctum</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3467</td>
      <td>East Sanctum</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3468</td>
      <td>Saltheril’s Haven</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3469</td>
      <td>Thuron’s Livery</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3470</td>
      <td>Stillwhisper Pond</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3471</td>
      <td>The Living Wood</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3472</td>
      <td>Azurebreeze Coast</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3473</td>
      <td>Lake Elrendar</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3474</td>
      <td>The Scorched Grove</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3475</td>
      <td>Zeb’Watha</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3476</td>
      <td>Tor’Watha</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3477</td>
      <td>Azjol-Nerub</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3478</td>
      <td>Gates of Ahn’Qiraj</td>
      <td>1</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3479</td>
      <td>The Veiled Sea</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3480</td>
      <td>Duskwither Grounds</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3481</td>
      <td>Duskwither Spire</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3482</td>
      <td>The Dead Scar</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3483</td>
      <td>Hellfire Peninsula</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3484</td>
      <td>The Sunspire</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3485</td>
      <td>Falthrien Academy</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3486</td>
      <td>Ravenholdt Manor</td>
      <td>0</td>
      <td>36</td>
    </tr>
    <tr>
      <td>3487</td>
      <td>Silvermoon City</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3488</td>
      <td>Tranquillien</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3489</td>
      <td>Suncrown Village</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3490</td>
      <td>Goldenmist Village</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3491</td>
      <td>Windrunner Village</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3492</td>
      <td>Windrunner Spire</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3493</td>
      <td>Sanctum of the Sun</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3494</td>
      <td>Sanctum of the Moon</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3495</td>
      <td>Dawnstar Spire</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3496</td>
      <td>Farstrider Enclave</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3497</td>
      <td>An’daroth</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3498</td>
      <td>An’telas</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3499</td>
      <td>An’owyn</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3500</td>
      <td>Deatholme</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3501</td>
      <td>Bleeding Ziggurat</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3502</td>
      <td>Howling Ziggurat</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3503</td>
      <td>Shalandis Isle</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3504</td>
      <td>Toryl Estate</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3505</td>
      <td>Underlight Mines</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3506</td>
      <td>Andilien Estate</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3507</td>
      <td>Hatchet Hills</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3508</td>
      <td>Amani Pass</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3509</td>
      <td>Sungraze Peak</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3510</td>
      <td>Amani Catacombs</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3511</td>
      <td>Tower of the Damned</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3512</td>
      <td>Zeb’Sora</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3513</td>
      <td>Lake Elrendar</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3514</td>
      <td>The Dead Scar</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3515</td>
      <td>Elrendar River</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3516</td>
      <td>Zeb’Tela</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3517</td>
      <td>Zeb’Nowa</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3518</td>
      <td>Nagrand</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3519</td>
      <td>Terokkar Forest</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3520</td>
      <td>Shadowmoon Valley</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3521</td>
      <td>Zangarmarsh</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3522</td>
      <td>Blade’s Edge Mountains</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3523</td>
      <td>Netherstorm</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3524</td>
      <td>Azuremyst Isle</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3525</td>
      <td>Bloodmyst Isle</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3526</td>
      <td>Ammen Vale</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3527</td>
      <td>Crash Site</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3528</td>
      <td>Silverline Lake</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3529</td>
      <td>Nestlewood Thicket</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3530</td>
      <td>Shadow Ridge</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3531</td>
      <td>Skulking Row</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3532</td>
      <td>Dawning Lane</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3533</td>
      <td>Ruins of Silvermoon</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3534</td>
      <td>Feth’s Way</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3535</td>
      <td>Hellfire Citadel</td>
      <td>540</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3536</td>
      <td>Thrallmar</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3537</td>
      <td>Borean Tundra</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3538</td>
      <td>Honor Hold</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3539</td>
      <td>The Stair of Destiny</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3540</td>
      <td>Twisting Nether</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3541</td>
      <td>Forge Camp: Mageddon</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3542</td>
      <td>The Path of Glory</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3543</td>
      <td>The Great Fissure</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3544</td>
      <td>Plain of Shards</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3545</td>
      <td>Hellfire Citadel</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3546</td>
      <td>Expedition Armory</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3547</td>
      <td>Throne of Kil’jaeden</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3548</td>
      <td>Forge Camp: Rage</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3549</td>
      <td>Invasion Point: Annihilator</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3550</td>
      <td>Borune Ruins</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3551</td>
      <td>Ruins of Sha’naar</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3552</td>
      <td>Temple of Telhamat</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3553</td>
      <td>Pools of Aggonar</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3554</td>
      <td>Falcon Watch</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3555</td>
      <td>Mag’har Post</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3556</td>
      <td>Den of Haal’esh</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3557</td>
      <td>The Exodar</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3558</td>
      <td>Elrendar Falls</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3559</td>
      <td>Nestlewood Hills</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3560</td>
      <td>Ammen Fields</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3561</td>
      <td>The Sacred Grove</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3562</td>
      <td>Hellfire Ramparts</td>
      <td>543</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3563</td>
      <td>Hellfire Citadel</td>
      <td>543</td>
      <td>3562</td>
    </tr>
    <tr>
      <td>3564</td>
      <td>Emberglade</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3565</td>
      <td>Cenarion Refuge</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3566</td>
      <td>Moonwing Den</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3567</td>
      <td>Pod Cluster</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3568</td>
      <td>Pod Wreckage</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3569</td>
      <td>Tides’ Hollow</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3570</td>
      <td>Wrathscale Point</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3571</td>
      <td>Bristlelimb Village</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3572</td>
      <td>Stillpine Hold</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3573</td>
      <td>Odesyus’ Landing</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3574</td>
      <td>Valaar’s Berth</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3575</td>
      <td>Silting Shore</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3576</td>
      <td>Azure Watch</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3577</td>
      <td>Geezle’s Camp</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3578</td>
      <td>Menagerie Wreckage</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3579</td>
      <td>Traitor’s Cove</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3580</td>
      <td>Wildwind Peak</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3581</td>
      <td>Wildwind Path</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3582</td>
      <td>Zeth’Gor</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3583</td>
      <td>Beryl Coast</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3584</td>
      <td>Blood Watch</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3585</td>
      <td>Bladewood</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3586</td>
      <td>The Vector Coil</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3587</td>
      <td>The Warp Piston</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3588</td>
      <td>The Cryo-Core</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3589</td>
      <td>The Crimson Reach</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3590</td>
      <td>Wrathscale Lair</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3591</td>
      <td>Ruins of Loreth’Aran</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3592</td>
      <td>Nazzivian</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3593</td>
      <td>Axxarien</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3594</td>
      <td>Blacksilt Shore</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3595</td>
      <td>The Foul Pool</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3596</td>
      <td>The Hidden Reef</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3597</td>
      <td>Amberweb Pass</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3598</td>
      <td>Wyrmscar Island</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3599</td>
      <td>Talon Stand</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3600</td>
      <td>Bristlelimb Enclave</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3601</td>
      <td>Ragefeather Ridge</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3602</td>
      <td>Kessel’s Crossing</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3603</td>
      <td>Tel’athion’s Camp</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3604</td>
      <td>The Bloodcursed Reef</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3605</td>
      <td>Hyjal Past</td>
      <td>560</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3606</td>
      <td>Hyjal Summit</td>
      <td>534</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3607</td>
      <td>Serpentshrine Cavern</td>
      <td>548</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3608</td>
      <td>Vindicator’s Rest</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3609</td>
      <td>Unused3</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3610</td>
      <td>Burning Blade Ruins</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3611</td>
      <td>Clan Watch</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3612</td>
      <td>Bloodcurse Isle</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3613</td>
      <td>Garadar</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3614</td>
      <td>Skysong Lake</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3615</td>
      <td>Throne of the Elements</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3616</td>
      <td>Laughing Skull Ruins</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3617</td>
      <td>Warmaul Hill</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3618</td>
      <td>Gruul’s Lair</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3619</td>
      <td>Auren Ridge</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3620</td>
      <td>Auren Falls</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3621</td>
      <td>Lake Sunspring</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3622</td>
      <td>Sunspring Post</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3623</td>
      <td>Aeris Landing</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3624</td>
      <td>Forge Camp: Fear</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3625</td>
      <td>Forge Camp: Hate</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3626</td>
      <td>Telaar</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3627</td>
      <td>Northwind Cleft</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3628</td>
      <td>Halaa</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3629</td>
      <td>Southwind Cleft</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3630</td>
      <td>Oshu’gun</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3631</td>
      <td>Spirit Fields</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3632</td>
      <td>Shamanar</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3633</td>
      <td>Ancestral Grounds</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3634</td>
      <td>Windyreed Village</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3635</td>
      <td>Unused2</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3636</td>
      <td>Elemental Plateau</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3637</td>
      <td>Kil’sorrow Fortress</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3638</td>
      <td>The Ring of Trials</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3639</td>
      <td>Silvermyst Isle</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3640</td>
      <td>Daggerfen Village</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3641</td>
      <td>Umbrafen Village</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3642</td>
      <td>Feralfen Village</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3643</td>
      <td>Bloodscale Enclave</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3644</td>
      <td>Telredor</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3645</td>
      <td>Zabra’jin</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3646</td>
      <td>Quagg Ridge</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3647</td>
      <td>The Spawning Glen</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3648</td>
      <td>The Dead Mire</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3649</td>
      <td>Sporeggar</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3650</td>
      <td>Ango’rosh Grounds</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3651</td>
      <td>Ango’rosh Stronghold</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3652</td>
      <td>Funggor Cavern</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3653</td>
      <td>Serpent Lake</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3654</td>
      <td>The Drain</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3655</td>
      <td>Umbrafen Lake</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3656</td>
      <td>Marshlight Lake</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3657</td>
      <td>Portal Clearing</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3658</td>
      <td>Sporewind Lake</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3659</td>
      <td>The Lagoon</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3660</td>
      <td>Blades’ Run</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3661</td>
      <td>Blade Tooth Canyon</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3662</td>
      <td>Commons Hall</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3663</td>
      <td>Derelict Manor</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3664</td>
      <td>Huntress of the Sun</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3665</td>
      <td>Falconwing Square</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3666</td>
      <td>Halaani Basin</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3667</td>
      <td>Hewn Bog</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3668</td>
      <td>Boha’mu Ruins</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3669</td>
      <td>The Stadium</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3670</td>
      <td>The Overlook</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3671</td>
      <td>Broken Hill</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3672</td>
      <td>Mag’hari Procession</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3673</td>
      <td>Nesingwary Safari</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3674</td>
      <td>Cenarion Thicket</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3675</td>
      <td>Tuurem</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3676</td>
      <td>Veil Shienor</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3677</td>
      <td>Veil Skith</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3678</td>
      <td>Veil Shalas</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3679</td>
      <td>Skettis</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3680</td>
      <td>Blackwind Valley</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3681</td>
      <td>Firewing Point</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3682</td>
      <td>Grangol’var Village</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3683</td>
      <td>Stonebreaker Hold</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3684</td>
      <td>Allerian Stronghold</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3685</td>
      <td>Bonechewer Ruins</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3686</td>
      <td>Veil Lithic</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3687</td>
      <td>Olembas</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3688</td>
      <td>Auchindoun</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3689</td>
      <td>Veil Reskk</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3690</td>
      <td>Blackwind Lake</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3691</td>
      <td>Lake Ere’Noru</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3692</td>
      <td>Lake Jorune</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3693</td>
      <td>Skethyl Mountains</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3694</td>
      <td>Misty Ridge</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3695</td>
      <td>The Broken Hills</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3696</td>
      <td>The Barrier Hills</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3697</td>
      <td>The Bone Wastes</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3698</td>
      <td>Nagrand Arena</td>
      <td>559</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3699</td>
      <td>Laughing Skull Courtyard</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3700</td>
      <td>The Ring of Blood</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3701</td>
      <td>Arena Floor</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3702</td>
      <td>Blade’s Edge Arena</td>
      <td>562</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3703</td>
      <td>Shattrath City</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3704</td>
      <td>The Shepherd’s Gate</td>
      <td>530</td>
      <td>3487</td>
    </tr>
    <tr>
      <td>3705</td>
      <td>Telaari Basin</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3706</td>
      <td>The Dark Portal</td>
      <td>269</td>
      <td>2366</td>
    </tr>
    <tr>
      <td>3707</td>
      <td>Alliance Base</td>
      <td>534</td>
      <td>3606</td>
    </tr>
    <tr>
      <td>3708</td>
      <td>Horde Encampment</td>
      <td>534</td>
      <td>3606</td>
    </tr>
    <tr>
      <td>3709</td>
      <td>Night Elf Village</td>
      <td>534</td>
      <td>3606</td>
    </tr>
    <tr>
      <td>3710</td>
      <td>Nordrassil</td>
      <td>534</td>
      <td>3606</td>
    </tr>
    <tr>
      <td>3711</td>
      <td>Sholazar Basin</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3712</td>
      <td>Area 52</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3713</td>
      <td>The Blood Furnace</td>
      <td>542</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3714</td>
      <td>The Shattered Halls</td>
      <td>540</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3715</td>
      <td>The Steamvault</td>
      <td>545</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3716</td>
      <td>The Underbog</td>
      <td>546</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3717</td>
      <td>The Slave Pens</td>
      <td>547</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3718</td>
      <td>Swamprat Post</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3719</td>
      <td>Bleeding Hollow Ruins</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3720</td>
      <td>Twin Spire Ruins</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3721</td>
      <td>The Crumbling Waste</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3722</td>
      <td>Manaforge Ara</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3723</td>
      <td>Arklon Ruins</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3724</td>
      <td>Cosmowrench</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3725</td>
      <td>Ruins of Enkaat</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3726</td>
      <td>Manaforge B’naar</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3727</td>
      <td>The Scrap Field</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3728</td>
      <td>The Vortex Fields</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3729</td>
      <td>The Heap</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3730</td>
      <td>Manaforge Coruu</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3731</td>
      <td>The Tempest Rift</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3732</td>
      <td>Kirin’Var Village</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3733</td>
      <td>The Violet Tower</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3734</td>
      <td>Manaforge Duro</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3735</td>
      <td>Voidwind Plateau</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3736</td>
      <td>Manaforge Ultris</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3737</td>
      <td>Celestial Ridge</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3738</td>
      <td>The Stormspire</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3739</td>
      <td>Forge Base: Oblivion</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3740</td>
      <td>Forge Base: Gehenna</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3741</td>
      <td>Ruins of Farahlon</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3742</td>
      <td>Socrethar’s Seat</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3743</td>
      <td>Legion Hold</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3744</td>
      <td>Shadowmoon Village</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3745</td>
      <td>Wildhammer Stronghold</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3746</td>
      <td>The Hand of Gul’dan</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3747</td>
      <td>The Fel Pits</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3748</td>
      <td>The Deathforge</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3749</td>
      <td>Coilskar Cistern</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3750</td>
      <td>Coilskar Point</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3751</td>
      <td>Sunfire Point</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3752</td>
      <td>Illidari Point</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3753</td>
      <td>Ruins of Baa’ri</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3754</td>
      <td>Altar of Sha’tar</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3755</td>
      <td>The Stair of Doom</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3756</td>
      <td>Ruins of Karabor</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3757</td>
      <td>Ata’mal Terrace</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3758</td>
      <td>Netherwing Fields</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3759</td>
      <td>Netherwing Ledge</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3760</td>
      <td>The Barrier Hills</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3761</td>
      <td>The High Path</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3762</td>
      <td>Windyreed Pass</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3763</td>
      <td>Zangar Ridge</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3764</td>
      <td>The Twilight Ridge</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3765</td>
      <td>Razorthorn Trail</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3766</td>
      <td>Orebor Harborage</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3767</td>
      <td>Blades’ Run</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3768</td>
      <td>Jagged Ridge</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3769</td>
      <td>Thunderlord Stronghold</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3770</td>
      <td>Blade Tooth Canyon</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3771</td>
      <td>The Living Grove</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3772</td>
      <td>Sylvanaar</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3773</td>
      <td>Bladespire Hold</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3774</td>
      <td>Gruul’s Lair</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3775</td>
      <td>Circle of Blood</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3776</td>
      <td>Bloodmaul Outpost</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3777</td>
      <td>Bloodmaul Camp</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3778</td>
      <td>Draenethyst Mine</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3779</td>
      <td>Trogma’s Claim</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3780</td>
      <td>Blackwing Coven</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3781</td>
      <td>Grishnath</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3782</td>
      <td>Veil Lashh</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3783</td>
      <td>Veil Vekh</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3784</td>
      <td>Forge Camp: Terror</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3785</td>
      <td>Forge Camp: Wrath</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3786</td>
      <td>Ogri’la</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3787</td>
      <td>Forge Camp: Anger</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3788</td>
      <td>The Low Path</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3789</td>
      <td>Shadow Labyrinth</td>
      <td>555</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3790</td>
      <td>Auchenai Crypts</td>
      <td>558</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3791</td>
      <td>Sethekk Halls</td>
      <td>556</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3792</td>
      <td>Mana-Tombs</td>
      <td>557</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3793</td>
      <td>Felspark Ravine</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3794</td>
      <td>Valley of Bones</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3795</td>
      <td>Sha’naari Wastes</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3796</td>
      <td>The Warp Fields</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3797</td>
      <td>Fallen Sky Ridge</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3798</td>
      <td>Haal’eshi Gorge</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3799</td>
      <td>Stonewall Canyon</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3800</td>
      <td>Thornfang Hill</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3801</td>
      <td>Mag’har Grounds</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3802</td>
      <td>Void Ridge</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3803</td>
      <td>The Abyssal Shelf</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3804</td>
      <td>The Legion Front</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3805</td>
      <td>Zul’Aman</td>
      <td>568</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3806</td>
      <td>Supply Caravan</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3807</td>
      <td>Reaver’s Fall</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3808</td>
      <td>Cenarion Post</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3809</td>
      <td>Southern Rampart</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3810</td>
      <td>Northern Rampart</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3811</td>
      <td>Gor’gaz Outpost</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3812</td>
      <td>Spinebreaker Post</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3813</td>
      <td>The Path of Anguish</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3814</td>
      <td>East Supply Caravan</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3815</td>
      <td>Expedition Point</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3816</td>
      <td>Zeppelin Crash</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3817</td>
      <td>Testing</td>
      <td>13</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3818</td>
      <td>Bloodscale Grounds</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3819</td>
      <td>Darkcrest Enclave</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3820</td>
      <td>Eye of the Storm</td>
      <td>566</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3821</td>
      <td>Warden’s Cage</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3822</td>
      <td>Eclipse Point</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3823</td>
      <td>Isle of Tribulations</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3824</td>
      <td>Bloodmaul Ravine</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3825</td>
      <td>Dragons’ End</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3826</td>
      <td>Daggermaw Canyon</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3827</td>
      <td>Vekhaar Stand</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3828</td>
      <td>Ruuan Weald</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3829</td>
      <td>Veil Ruuan</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3830</td>
      <td>Raven’s Wood</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3831</td>
      <td>Death’s Door</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3832</td>
      <td>Vortex Pinnacle</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3833</td>
      <td>Razor Ridge</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3834</td>
      <td>Ridge of Madness</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3835</td>
      <td>Dustquill Ravine</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3836</td>
      <td>Magtheridon’s Lair</td>
      <td>544</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3837</td>
      <td>Sunfury Hold</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3838</td>
      <td>Spinebreaker Mountains</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3839</td>
      <td>Abandoned Armory</td>
      <td>530</td>
      <td>3518</td>
    </tr>
    <tr>
      <td>3840</td>
      <td>The Black Temple</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3841</td>
      <td>Darkcrest Shore</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3842</td>
      <td>Tempest Keep</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3844</td>
      <td>Mok’Nathal Village</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3845</td>
      <td>Tempest Keep</td>
      <td>550</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3846</td>
      <td>The Arcatraz</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3847</td>
      <td>The Botanica</td>
      <td>553</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3848</td>
      <td>The Arcatraz</td>
      <td>552</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3849</td>
      <td>The Mechanar</td>
      <td>554</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3850</td>
      <td>Netherstone</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3851</td>
      <td>Midrealm Post</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3852</td>
      <td>Tuluman’s Landing</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3854</td>
      <td>Protectorate Watch Post</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3855</td>
      <td>Circle of Blood Arena</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3856</td>
      <td>Elrendar Crossing</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3857</td>
      <td>Ammen Ford</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3858</td>
      <td>Razorthorn Shelf</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3859</td>
      <td>Silmyr Lake</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3860</td>
      <td>Raastok Glade</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3861</td>
      <td>Thalassian Pass</td>
      <td>530</td>
      <td>3433</td>
    </tr>
    <tr>
      <td>3862</td>
      <td>Churning Gulch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3863</td>
      <td>Broken Wilds</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3864</td>
      <td>Bash’ir Landing</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3865</td>
      <td>Crystal Spine</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3866</td>
      <td>Skald</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3867</td>
      <td>Bladed Gulch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3868</td>
      <td>Gyro-Plank Bridge</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3869</td>
      <td>Mage Tower</td>
      <td>566</td>
      <td>3820</td>
    </tr>
    <tr>
      <td>3870</td>
      <td>Blood Elf Tower</td>
      <td>566</td>
      <td>3820</td>
    </tr>
    <tr>
      <td>3871</td>
      <td>Draenei Ruins</td>
      <td>566</td>
      <td>3820</td>
    </tr>
    <tr>
      <td>3872</td>
      <td>Fel Reaver Ruins</td>
      <td>566</td>
      <td>3820</td>
    </tr>
    <tr>
      <td>3873</td>
      <td>The Proving Grounds</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3874</td>
      <td>Eco-Dome Farfield</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3875</td>
      <td>Eco-Dome Skyperch</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3876</td>
      <td>Eco-Dome Sutheron</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3877</td>
      <td>Eco-Dome Midrealm</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3878</td>
      <td>Ethereum Staging Grounds</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3879</td>
      <td>Chapel Yard</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3880</td>
      <td>Access Shaft Zeon</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3881</td>
      <td>Trelleum Mine</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3882</td>
      <td>Invasion Point: Destroyer</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3883</td>
      <td>Camp of Boom</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3884</td>
      <td>Spinebreaker Pass</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3885</td>
      <td>Netherweb Ridge</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3886</td>
      <td>Derelict Caravan</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3887</td>
      <td>Refugee Caravan</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3888</td>
      <td>Shadow Tomb</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3889</td>
      <td>Veil Rhaze</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3890</td>
      <td>Tomb of Lights</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3891</td>
      <td>Carrion Hill</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3892</td>
      <td>Writhing Mound</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3893</td>
      <td>Ring of Observance</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3894</td>
      <td>Auchenai Grounds</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3895</td>
      <td>Cenarion Watchpost</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3896</td>
      <td>Aldor Rise</td>
      <td>530</td>
      <td>3703</td>
    </tr>
    <tr>
      <td>3897</td>
      <td>Terrace of Light</td>
      <td>530</td>
      <td>3703</td>
    </tr>
    <tr>
      <td>3898</td>
      <td>Scryer’s Tier</td>
      <td>530</td>
      <td>3703</td>
    </tr>
    <tr>
      <td>3899</td>
      <td>Lower City</td>
      <td>530</td>
      <td>3703</td>
    </tr>
    <tr>
      <td>3900</td>
      <td>Invasion Point: Overlord</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3901</td>
      <td>Allerian Post</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3902</td>
      <td>Stonebreaker Camp</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3903</td>
      <td>Boulder’mok</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3904</td>
      <td>Cursed Hollow</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3905</td>
      <td>Coilfang Reservoir</td>
      <td>530</td>
      <td>3521</td>
    </tr>
    <tr>
      <td>3906</td>
      <td>The Bloodwash</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3907</td>
      <td>Veridian Point</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3908</td>
      <td>Middenvale</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3909</td>
      <td>The Lost Fold</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3910</td>
      <td>Mystwood</td>
      <td>530</td>
      <td>3525</td>
    </tr>
    <tr>
      <td>3911</td>
      <td>Tranquil Shore</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3912</td>
      <td>Goldenbough Pass</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3913</td>
      <td>Runestone Falithas</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3914</td>
      <td>Runestone Shan’dor</td>
      <td>530</td>
      <td>3430</td>
    </tr>
    <tr>
      <td>3915</td>
      <td>Fairbridge Strand</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3916</td>
      <td>Moongraze Woods</td>
      <td>530</td>
      <td>3524</td>
    </tr>
    <tr>
      <td>3917</td>
      <td>Auchindoun</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3918</td>
      <td>Toshley’s Station</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3919</td>
      <td>Singing Ridge</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3920</td>
      <td>Shatter Point</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3921</td>
      <td>Arklonis Ridge</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3922</td>
      <td>Bladespire Outpost</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3923</td>
      <td>Gruul’s Lair</td>
      <td>565</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3924</td>
      <td>Northmaul Tower</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3925</td>
      <td>Southmaul Tower</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3926</td>
      <td>Shattered Plains</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3927</td>
      <td>Oronok’s Farm</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3928</td>
      <td>The Altar of Damnation</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3929</td>
      <td>The Path of Conquest</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3930</td>
      <td>Eclipsion Fields</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3931</td>
      <td>Bladespire Grounds</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3932</td>
      <td>Sketh’lon Base Camp</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3933</td>
      <td>Sketh’lon Wreckage</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3934</td>
      <td>Town Square</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3935</td>
      <td>Wizard Row</td>
      <td>530</td>
      <td>3523</td>
    </tr>
    <tr>
      <td>3936</td>
      <td>Deathforge Tower</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3937</td>
      <td>Slag Watch</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3938</td>
      <td>Sanctum of the Stars</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3939</td>
      <td>Dragonmaw Fortress</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3940</td>
      <td>The Fetid Pool</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3941</td>
      <td>Test</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3942</td>
      <td>Razaan’s Landing</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3943</td>
      <td>Invasion Point: Cataclysm</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3944</td>
      <td>The Altar of Shadows</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3945</td>
      <td>Netherwing Pass</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3946</td>
      <td>Wayne’s Refuge</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3947</td>
      <td>The Scalding Pools</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3948</td>
      <td>Brian and Pat Test</td>
      <td>451</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3949</td>
      <td>Magma Fields</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3950</td>
      <td>Crimson Watch</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3951</td>
      <td>Evergrove</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3952</td>
      <td>Wyrmskull Bridge</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3953</td>
      <td>Scalewing Shelf</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3954</td>
      <td>Wyrmskull Tunnel</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3955</td>
      <td>Hellfire Basin</td>
      <td>530</td>
      <td>3483</td>
    </tr>
    <tr>
      <td>3956</td>
      <td>The Shadow Stair</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3957</td>
      <td>Sha’tari Outpost</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3958</td>
      <td>Sha’tari Base Camp</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3959</td>
      <td>Black Temple</td>
      <td>564</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3960</td>
      <td>Soulgrinder’s Barrow</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3961</td>
      <td>Sorrow Wing Point</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3962</td>
      <td>Vim’gol’s Circle</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3963</td>
      <td>Dragonspine Ridge</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3964</td>
      <td>Skyguard Outpost</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3965</td>
      <td>Netherwing Mines</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3966</td>
      <td>Dragonmaw Base Camp</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3967</td>
      <td>Dragonmaw Skyway</td>
      <td>530</td>
      <td>3520</td>
    </tr>
    <tr>
      <td>3968</td>
      <td>Ruins of Lordaeron</td>
      <td>572</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3969</td>
      <td>Rivendark’s Perch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3970</td>
      <td>Obsidia’s Perch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3971</td>
      <td>Insidion’s Perch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3972</td>
      <td>Furywing’s Perch</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>3973</td>
      <td>Blackwind Landing</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3974</td>
      <td>Veil Harr’ik</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3975</td>
      <td>Terokk’s Rest</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3976</td>
      <td>Veil Ala’rak</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3977</td>
      <td>Upper Veil Shil’ak</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3978</td>
      <td>Lower Veil Shil’ak</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>3979</td>
      <td>The Frozen Sea</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>3980</td>
      <td>Daggercap Bay</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3981</td>
      <td>Valgarde</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3982</td>
      <td>Wyrmskull Village</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3983</td>
      <td>Utgarde Keep</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3984</td>
      <td>Nifflevar</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3985</td>
      <td>Falls of Ymiron</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3986</td>
      <td>Echo Reach</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3987</td>
      <td>The Isle of Spears</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3988</td>
      <td>Kamagua</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3989</td>
      <td>Garvan’s Reef</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3990</td>
      <td>Scalawag Point</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3991</td>
      <td>New Agamand</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3992</td>
      <td>The Ancient Lift</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3993</td>
      <td>Westguard Turret</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3994</td>
      <td>Halgrind</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3995</td>
      <td>The Laughing Stand</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3996</td>
      <td>Baelgun’s Excavation Site</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3997</td>
      <td>Explorers’ League Outpost</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3998</td>
      <td>Westguard Keep</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>3999</td>
      <td>Steel Gate</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4000</td>
      <td>Vengeance Landing</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4001</td>
      <td>Baleheim</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4002</td>
      <td>Skorn</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4003</td>
      <td>Fort Wildervar</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4004</td>
      <td>Vileprey Village</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4005</td>
      <td>Ivald’s Ruin</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4006</td>
      <td>Gjalerbron</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4007</td>
      <td>Tomb of the Lost Kings</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4008</td>
      <td>Shartuul’s Transporter</td>
      <td>530</td>
      <td>3522</td>
    </tr>
    <tr>
      <td>4009</td>
      <td>Illidari Training Grounds</td>
      <td>564</td>
      <td>3959</td>
    </tr>
    <tr>
      <td>4010</td>
      <td>Mudsprocket</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>4018</td>
      <td>Camp Winterhoof</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4019</td>
      <td>Development Land</td>
      <td>451</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4020</td>
      <td>Mightstone Quarry</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4021</td>
      <td>Bloodspore Plains</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4022</td>
      <td>Gammoth</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4023</td>
      <td>Amber Ledge</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4024</td>
      <td>Coldarra</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4025</td>
      <td>The Westrift</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4026</td>
      <td>The Transitus Stair</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4027</td>
      <td>Coast of Echoes</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4028</td>
      <td>Riplash Strand</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4029</td>
      <td>Riplash Ruins</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4030</td>
      <td>Coast of Idols</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4031</td>
      <td>Pal’ea</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4032</td>
      <td>Valiance Keep</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4033</td>
      <td>Winterfin Village</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4034</td>
      <td>The Borean Wall</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4035</td>
      <td>The Geyser Fields</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4036</td>
      <td>Fizzcrank Pumping Station</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4037</td>
      <td>Taunka’le Village</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4038</td>
      <td>Magnamoth Caverns</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4039</td>
      <td>Coldrock Quarry</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4040</td>
      <td>Njord’s Breath Bay</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4041</td>
      <td>Kaskala</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4042</td>
      <td>Transborea</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4043</td>
      <td>The Flood Plains</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4046</td>
      <td>Direhorn Post</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>4047</td>
      <td>Nat’s Landing</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>4048</td>
      <td>Ember Clutch</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4049</td>
      <td>Tabetha’s Farm</td>
      <td>1</td>
      <td>15</td>
    </tr>
    <tr>
      <td>4050</td>
      <td>Derelict Strand</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4051</td>
      <td>The Frozen Glade</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4052</td>
      <td>The Vibrant Glade</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4053</td>
      <td>The Twisted Glade</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4054</td>
      <td>Rivenwood</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4055</td>
      <td>Caldemere Lake</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4056</td>
      <td>Utgarde Catacombs</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4057</td>
      <td>Shield Hill</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4058</td>
      <td>Lake Cauldros</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4059</td>
      <td>Cauldros Isle</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4060</td>
      <td>Bleeding Vale</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4061</td>
      <td>Giants’ Run</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4062</td>
      <td>Apothecary Camp</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4063</td>
      <td>Ember Spear Tower</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4064</td>
      <td>Shattered Straits</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4065</td>
      <td>Gjalerhorn</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4066</td>
      <td>Frostblade Peak</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4067</td>
      <td>Plaguewood Tower</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>4068</td>
      <td>West Spear Tower</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4069</td>
      <td>North Spear Tower</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4070</td>
      <td>Chillmere Coast</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4071</td>
      <td>Whisper Gulch</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4072</td>
      <td>Sub zone</td>
      <td>451</td>
      <td>151</td>
    </tr>
    <tr>
      <td>4073</td>
      <td>Winter’s Terrace</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4074</td>
      <td>The Waking Halls</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4075</td>
      <td>Sunwell Plateau</td>
      <td>580</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4076</td>
      <td>Reuse Me 7</td>
      <td>598</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4077</td>
      <td>Sorlof’s Strand</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4078</td>
      <td>Razorthorn Rise</td>
      <td>530</td>
      <td>3519</td>
    </tr>
    <tr>
      <td>4079</td>
      <td>Frostblade Pass</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4080</td>
      <td>Isle of Quel’Danas</td>
      <td>530</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4081</td>
      <td>The Dawnchaser</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4082</td>
      <td>The Sin’loren</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4083</td>
      <td>Silvermoon’s Pride</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4084</td>
      <td>The Bloodoath</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4085</td>
      <td>Shattered Sun Staging Area</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4086</td>
      <td>Sun’s Reach Sanctum</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4087</td>
      <td>Sun’s Reach Harbor</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4088</td>
      <td>Sun’s Reach Armory</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4089</td>
      <td>Dawnstar Village</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4090</td>
      <td>The Dawning Square</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4091</td>
      <td>Greengill Coast</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4092</td>
      <td>The Dead Scar</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4093</td>
      <td>The Sun Forge</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4094</td>
      <td>Sunwell Plateau</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4095</td>
      <td>Magisters’ Terrace</td>
      <td>530</td>
      <td>4080</td>
    </tr>
    <tr>
      <td>4096</td>
      <td>Clayt?Ân’s WoWEdit Land</td>
      <td>451</td>
      <td>4019</td>
    </tr>
    <tr>
      <td>4097</td>
      <td>Winterfin Caverns</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4098</td>
      <td>Glimmer Bay</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4099</td>
      <td>Winterfin Retreat</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4100</td>
      <td>The Culling of Stratholme</td>
      <td>595</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4101</td>
      <td>Sands of Nasam</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4102</td>
      <td>Krom’s Landing</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4103</td>
      <td>Nasam’s Talon</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4104</td>
      <td>Echo Cove</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4105</td>
      <td>Beryl Point</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4106</td>
      <td>Garrosh’s Landing</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4107</td>
      <td>Warsong Jetty</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4108</td>
      <td>Fizzcrank Airstrip</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4109</td>
      <td>Lake Kum’uya</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4110</td>
      <td>Farshire Fields</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4111</td>
      <td>Farshire</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4112</td>
      <td>Farshire Lighthouse</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4113</td>
      <td>Unu’pe</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4114</td>
      <td>Death’s Stand</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4115</td>
      <td>The Abandoned Reach</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4116</td>
      <td>Scalding Pools</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4117</td>
      <td>Steam Springs</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4118</td>
      <td>Talramas</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4119</td>
      <td>Festering Pools</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4120</td>
      <td>The Nexus</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4121</td>
      <td>Transitus Shield</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4122</td>
      <td>Bor’gorok Outpost</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4123</td>
      <td>Magmoth</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4124</td>
      <td>The Dens of Dying</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4125</td>
      <td>Temple City of En’kilah</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4126</td>
      <td>The Wailing Ziggurat</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4127</td>
      <td>Steeljaw’s Caravan</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4128</td>
      <td>Naxxanar</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4129</td>
      <td>Warsong Hold</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4130</td>
      <td>Plains of Nasam</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4131</td>
      <td>Magisters’ Terrace</td>
      <td>585</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4132</td>
      <td>Ruins of Eldra’nath</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4133</td>
      <td>Charred Rise</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4134</td>
      <td>Blistering Pool</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4135</td>
      <td>Spire of Blood</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4136</td>
      <td>Spire of Decay</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4137</td>
      <td>Spire of Pain</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4138</td>
      <td>Frozen Reach</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4139</td>
      <td>Parhelion Plaza</td>
      <td>580</td>
      <td>4075</td>
    </tr>
    <tr>
      <td>4140</td>
      <td>The Dead Scar</td>
      <td>580</td>
      <td>4075</td>
    </tr>
    <tr>
      <td>4141</td>
      <td>Torp’s Farm</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4142</td>
      <td>Warsong Granary</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4143</td>
      <td>Warsong Slaughterhouse</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4144</td>
      <td>Warsong Farms Outpost</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4145</td>
      <td>West Point Station</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4146</td>
      <td>North Point Station</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4147</td>
      <td>Mid Point Station</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4148</td>
      <td>South Point Station</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4149</td>
      <td>D.E.H.T.A. Encampment</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4150</td>
      <td>Kaw’s Roost</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4151</td>
      <td>Westwind Refugee Camp</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4152</td>
      <td>Moa’ki Harbor</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4153</td>
      <td>Indu’le Village</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4154</td>
      <td>Snowfall Glade</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4155</td>
      <td>The Half Shell</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4156</td>
      <td>Surge Needle</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4157</td>
      <td>Moonrest Gardens</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4158</td>
      <td>Stars’ Rest</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4159</td>
      <td>Westfall Brigade Encampment</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4160</td>
      <td>Lothalor Woodlands</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4161</td>
      <td>Wyrmrest Temple</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4162</td>
      <td>Icemist Falls</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4163</td>
      <td>Icemist Village</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4164</td>
      <td>The Pit of Narjun</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4165</td>
      <td>Agmar’s Hammer</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4166</td>
      <td>Lake Indu’le</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4167</td>
      <td>Obsidian Dragonshrine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4168</td>
      <td>Ruby Dragonshrine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4169</td>
      <td>Fordragon Hold</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4170</td>
      <td>Kor’kron Vanguard</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4171</td>
      <td>The Court of Skulls</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4172</td>
      <td>Angrathar the Wrathgate</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4173</td>
      <td>Galakrond’s Rest</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4174</td>
      <td>The Wicked Coil</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4175</td>
      <td>Bronze Dragonshrine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4176</td>
      <td>The Mirror of Dawn</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4177</td>
      <td>Wintergarde Keep</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4178</td>
      <td>Wintergarde Mine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4179</td>
      <td>Emerald Dragonshrine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4180</td>
      <td>New Hearthglen</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4181</td>
      <td>Crusader’s Landing</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4182</td>
      <td>Sinner’s Folly</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4183</td>
      <td>Azure Dragonshrine</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4184</td>
      <td>Path of the Titans</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4185</td>
      <td>The Forgotten Shore</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4186</td>
      <td>Venomspite</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4187</td>
      <td>The Crystal Vice</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4188</td>
      <td>The Carrion Fields</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4189</td>
      <td>Onslaught Base Camp</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4190</td>
      <td>Thorson’s Post</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4191</td>
      <td>Light’s Trust</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4192</td>
      <td>Frostmourne Cavern</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4193</td>
      <td>Scarlet Point</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4194</td>
      <td>Jintha’kalar</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4195</td>
      <td>Ice Heart Cavern</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4196</td>
      <td>Drak’Tharon Keep</td>
      <td>600</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4197</td>
      <td>Wintergrasp</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4198</td>
      <td>Kili’ua’s Atoll</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4199</td>
      <td>Silverbrook</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4200</td>
      <td>Vordrassil’s Heart</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4201</td>
      <td>Vordrassil’s Tears</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4202</td>
      <td>Vordrassil’s Tears</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4203</td>
      <td>Vordrassil’s Limb</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4204</td>
      <td>Amberpine Lodge</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4205</td>
      <td>Solstice Village</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4206</td>
      <td>Conquest Hold</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4207</td>
      <td>Voldrune</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4208</td>
      <td>Granite Springs</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4209</td>
      <td>Zeb’Halak</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4210</td>
      <td>Drak’Tharon Keep</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4211</td>
      <td>Camp Oneqwah</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4212</td>
      <td>Eastwind Shore</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4213</td>
      <td>The Broken Bluffs</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4214</td>
      <td>Boulder Hills</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4215</td>
      <td>Rage Fang Shrine</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4216</td>
      <td>Drakil’jin Ruins</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4217</td>
      <td>Blackriver Logging Camp</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4218</td>
      <td>Heart’s Blood Shrine</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4219</td>
      <td>Hollowstone Mine</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4220</td>
      <td>Dun Argol</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4221</td>
      <td>Thor Modan</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4222</td>
      <td>Blue Sky Logging Grounds</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4223</td>
      <td>Maw of Neltharion</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4224</td>
      <td>The Briny Pinnacle</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4225</td>
      <td>Glittering Strand</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4226</td>
      <td>Iskaal</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4227</td>
      <td>Dragon’s Fall</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4228</td>
      <td>The Oculus</td>
      <td>578</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4229</td>
      <td>Prospector’s Point</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4230</td>
      <td>Coldwind Heights</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4231</td>
      <td>Redwood Trading Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4232</td>
      <td>Vengeance Pass</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4233</td>
      <td>Dawn’s Reach</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4234</td>
      <td>Naxxramas</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4235</td>
      <td>Heartwood Trading Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4236</td>
      <td>Evergreen Trading Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4237</td>
      <td>Spruce Point Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4238</td>
      <td>White Pine Trading Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4239</td>
      <td>Aspen Grove Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4240</td>
      <td>Forest’s Edge Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4241</td>
      <td>Eldritch Heights</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4242</td>
      <td>Venture Bay</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4243</td>
      <td>Wintergarde Crypt</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4244</td>
      <td>Bloodmoon Isle</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4245</td>
      <td>Shadowfang Tower</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4246</td>
      <td>Wintergarde Mausoleum</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4247</td>
      <td>Duskhowl Den</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4248</td>
      <td>The Conquest Pit</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4249</td>
      <td>The Path of Iron</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4250</td>
      <td>Ruins of Tethys</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4251</td>
      <td>Silverbrook Hills</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4252</td>
      <td>The Broken Bluffs</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4253</td>
      <td>7th Legion Front</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4254</td>
      <td>The Dragon Wastes</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4255</td>
      <td>Ruins of Drak’Zin</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4256</td>
      <td>Drak’Mar Lake</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4257</td>
      <td>Dragonspine Tributary</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4258</td>
      <td>The North Sea</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4259</td>
      <td>Drak’ural</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4260</td>
      <td>Thorvald’s Camp</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4261</td>
      <td>Ghostblade Post</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4262</td>
      <td>Ashwood Post</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4263</td>
      <td>Lydell’s Ambush</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4264</td>
      <td>Halls of Stone</td>
      <td>599</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4265</td>
      <td>The Nexus</td>
      <td>576</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4266</td>
      <td>Harkor’s Camp</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4267</td>
      <td>Vordrassil Pass</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4268</td>
      <td>Ruuna’s Camp</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4269</td>
      <td>Shrine of Scales</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4270</td>
      <td>Drak’atal Passage</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4271</td>
      <td>Utgarde Pinnacle</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4272</td>
      <td>Halls of Lightning</td>
      <td>602</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4273</td>
      <td>Ulduar</td>
      <td>603</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4275</td>
      <td>The Argent Stand</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4276</td>
      <td>Altar of Sseratus</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4277</td>
      <td>Azjol-Nerub</td>
      <td>601</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4278</td>
      <td>Drak’Sotra Fields</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4279</td>
      <td>Drak’Sotra</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4280</td>
      <td>Drak’Agal</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4281</td>
      <td>Acherus: The Ebon Hold</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>4282</td>
      <td>The Avalanche</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4283</td>
      <td>The Lost Lands</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4284</td>
      <td>Nesingwary Base Camp</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4285</td>
      <td>The Seabreach Flow</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4286</td>
      <td>The Bones of Nozronn</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4287</td>
      <td>Kartak’s Hold</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4288</td>
      <td>Sparktouched Haven</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4289</td>
      <td>The Path of the Lifewarden</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4290</td>
      <td>River’s Heart</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4291</td>
      <td>Rainspeaker Canopy</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4292</td>
      <td>Frenzyheart Hill</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4293</td>
      <td>Wildgrowth Mangal</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4294</td>
      <td>Heb’Valok</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4295</td>
      <td>The Sundered Shard</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4296</td>
      <td>The Lifeblood Pillar</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4297</td>
      <td>Mosswalker Village</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4298</td>
      <td>Plaguelands: The Scarlet Enclave</td>
      <td>609</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4299</td>
      <td>Kolramas</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4300</td>
      <td>Waygate</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4302</td>
      <td>The Skyreach Pillar</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4303</td>
      <td>Hardknuckle Clearing</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4304</td>
      <td>Sapphire Hive</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4306</td>
      <td>Mistwhisper Refuge</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4307</td>
      <td>The Glimmering Pillar</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4308</td>
      <td>Spearborn Encampment</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4309</td>
      <td>Drak’Tharon Keep</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4310</td>
      <td>Zeramas</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4311</td>
      <td>Reliquary of Agony</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4312</td>
      <td>Ebon Watch</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4313</td>
      <td>Thrym’s End</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4314</td>
      <td>Voltarus</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4315</td>
      <td>Reliquary of Pain</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4316</td>
      <td>Rageclaw Den</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4317</td>
      <td>Light’s Breach</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4318</td>
      <td>Pools of Zha’Jin</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4319</td>
      <td>Zim’Abwa</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4320</td>
      <td>Amphitheater of Anguish</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4321</td>
      <td>Altar of Rhunok</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4322</td>
      <td>Altar of Har’koa</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4323</td>
      <td>Zim’Torga</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4324</td>
      <td>Pools of Jin’Alai</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4325</td>
      <td>Altar of Quetz’lun</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4326</td>
      <td>Heb’Drakkar</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4327</td>
      <td>Drak’Mabwa</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4328</td>
      <td>Zim’Rhuk</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4329</td>
      <td>Altar of Mam’toth</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4342</td>
      <td>Acherus: The Ebon Hold</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4343</td>
      <td>New Avalon</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4344</td>
      <td>New Avalon Fields</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4345</td>
      <td>New Avalon Orchard</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4346</td>
      <td>New Avalon Town Hall</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4347</td>
      <td>Havenshire</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4348</td>
      <td>Havenshire Farms</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4349</td>
      <td>Havenshire Lumber Mill</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4350</td>
      <td>Havenshire Stables</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4351</td>
      <td>Scarlet Hold</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4352</td>
      <td>Chapel of the Crimson Flame</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4353</td>
      <td>Light’s Point Tower</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4354</td>
      <td>Light’s Point</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4355</td>
      <td>Crypt of Remembrance</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4356</td>
      <td>Death’s Breach</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4357</td>
      <td>The Noxious Glade</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4358</td>
      <td>Tyr’s Hand</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4359</td>
      <td>King’s Harbor</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4360</td>
      <td>Scarlet Overlook</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4361</td>
      <td>Light’s Hope Chapel</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4362</td>
      <td>Sinner’s Folly</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4363</td>
      <td>Pestilent Scar</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4364</td>
      <td>Browman Mill</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4365</td>
      <td>Havenshire Mine</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4366</td>
      <td>Ursoc’s Den</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4367</td>
      <td>The Blight Line</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4368</td>
      <td>The Bonefields</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4369</td>
      <td>Dorian’s Outpost</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4371</td>
      <td>Mam’toth Crater</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4372</td>
      <td>Zol’Maz Stronghold</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4373</td>
      <td>Zol’Heb</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4374</td>
      <td>Rageclaw Lake</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4375</td>
      <td>Gundrak</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4376</td>
      <td>The Savage Thicket</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4377</td>
      <td>New Avalon Forge</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4378</td>
      <td>Dalaran Arena</td>
      <td>617</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4379</td>
      <td>Valgarde</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4380</td>
      <td>Westguard Inn</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4381</td>
      <td>Waygate</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>4382</td>
      <td>The Shaper’s Terrace</td>
      <td>1</td>
      <td>490</td>
    </tr>
    <tr>
      <td>4383</td>
      <td>Lakeside Landing</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4384</td>
      <td>Strand of the Ancients</td>
      <td>607</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4385</td>
      <td>Bittertide Lake</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4386</td>
      <td>Rainspeaker Rapids</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4387</td>
      <td>Frenzyheart River</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4388</td>
      <td>Wintergrasp River</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4389</td>
      <td>The Suntouched Pillar</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4390</td>
      <td>Frigid Breach</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4391</td>
      <td>Swindlegrin’s Dig</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4392</td>
      <td>The Stormwright’s Shelf</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4393</td>
      <td>Death’s Hand Encampment</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4394</td>
      <td>Scarlet Tavern</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4395</td>
      <td>Dalaran</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4396</td>
      <td>Nozzlerust Post</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4399</td>
      <td>Farshire Mine</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4400</td>
      <td>The Mosslight Pillar</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4401</td>
      <td>Saragosa’s Landing</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4402</td>
      <td>Vengeance Lift</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4403</td>
      <td>Balejar Watch</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4404</td>
      <td>New Agamand Inn</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4405</td>
      <td>Passage of Lost Fiends</td>
      <td>601</td>
      <td>4277</td>
    </tr>
    <tr>
      <td>4406</td>
      <td>The Ring of Valor</td>
      <td>618</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4407</td>
      <td>Hall of the Frostwolf</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>4408</td>
      <td>Hall of the Stormpike</td>
      <td>30</td>
      <td>2597</td>
    </tr>
    <tr>
      <td>4411</td>
      <td>Stormwind Harbor</td>
      <td>0</td>
      <td>1519</td>
    </tr>
    <tr>
      <td>4412</td>
      <td>The Makers’ Overlook</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4413</td>
      <td>The Makers’ Perch</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4414</td>
      <td>Scarlet Tower</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4415</td>
      <td>The Violet Hold</td>
      <td>608</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4416</td>
      <td>Gundrak</td>
      <td>604</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4417</td>
      <td>Onslaught Harbor</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4418</td>
      <td>K3</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4419</td>
      <td>Snowblind Hills</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4420</td>
      <td>Snowblind Terrace</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4421</td>
      <td>Garm</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4422</td>
      <td>Brunnhildar Village</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4423</td>
      <td>Sifreldar Village</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4424</td>
      <td>Valkyrion</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4425</td>
      <td>The Forlorn Mine</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4426</td>
      <td>Bor’s Breath River</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4427</td>
      <td>Argent Vanguard</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4428</td>
      <td>Frosthold</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4429</td>
      <td>Grom’arsh Crash-Site</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4430</td>
      <td>Temple of Storms</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4431</td>
      <td>Engine of the Makers</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4432</td>
      <td>The Foot Steppes</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4433</td>
      <td>Dragonspine Peaks</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4434</td>
      <td>Nidavelir</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4435</td>
      <td>Narvir’s Cradle</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4436</td>
      <td>Snowdrift Plains</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4437</td>
      <td>Valley of Ancient Winters</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4438</td>
      <td>Dun Niffelem</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4439</td>
      <td>Frostfield Lake</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4440</td>
      <td>Thunderfall</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4441</td>
      <td>Camp Tunka’lo</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4442</td>
      <td>Brann’s Base-Camp</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4443</td>
      <td>Gate of Echoes</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4444</td>
      <td>Plain of Echoes</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4445</td>
      <td>Ulduar</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4446</td>
      <td>Terrace of the Makers</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4447</td>
      <td>Gate of Lightning</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4448</td>
      <td>Path of the Titans</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4449</td>
      <td>Uldis</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4450</td>
      <td>Loken’s Bargain</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4451</td>
      <td>Bor’s Fall</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4452</td>
      <td>Bor’s Breath</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4453</td>
      <td>Rohemdal Pass</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4454</td>
      <td>The Storm Foundry</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4455</td>
      <td>Hibernal Cavern</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4456</td>
      <td>Voldrune Dwelling</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4457</td>
      <td>Torseg’s Rest</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4458</td>
      <td>Sparksocket Minefield</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4459</td>
      <td>Ricket’s Folly</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4460</td>
      <td>Garm’s Bane</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4461</td>
      <td>Garm’s Rise</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4462</td>
      <td>Crystalweb Cavern</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4463</td>
      <td>Temple of Life</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4464</td>
      <td>Temple of Order</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4465</td>
      <td>Temple of Winter</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4466</td>
      <td>Temple of Invention</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4467</td>
      <td>Death’s Rise</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4468</td>
      <td>The Dead Fields</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4469</td>
      <td>Dargath’s Demise</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4470</td>
      <td>The Hidden Hollow</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4471</td>
      <td>Bernau’s Happy Fun Land</td>
      <td>451</td>
      <td>4019</td>
    </tr>
    <tr>
      <td>4472</td>
      <td>Frostgrip’s Hollow</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4473</td>
      <td>The Frigid Tomb</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4474</td>
      <td>Twin Shores</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4475</td>
      <td>Zim’bo’s Hideout</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4476</td>
      <td>Abandoned Camp</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4477</td>
      <td>The Shadow Vault</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4478</td>
      <td>Coldwind Pass</td>
      <td>571</td>
      <td>65</td>
    </tr>
    <tr>
      <td>4479</td>
      <td>Winter’s Breath Lake</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4480</td>
      <td>The Forgotten Overlook</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4481</td>
      <td>Jintha’kalar Passage</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4482</td>
      <td>Arriga Footbridge</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4483</td>
      <td>The Lost Passage</td>
      <td>571</td>
      <td>3711</td>
    </tr>
    <tr>
      <td>4484</td>
      <td>Bouldercrag’s Refuge</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4485</td>
      <td>The Inventor’s Library</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4486</td>
      <td>The Frozen Mine</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4487</td>
      <td>Frostfloe Deep</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4488</td>
      <td>The Howling Hollow</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4489</td>
      <td>Crusader Forward Camp</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4490</td>
      <td>Stormcrest</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4491</td>
      <td>Bonesnap’s Camp</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4492</td>
      <td>Ufrang’s Hall</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4493</td>
      <td>The Obsidian Sanctum</td>
      <td>615</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4494</td>
      <td>Ahn’kahet: The Old Kingdom</td>
      <td>619</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4495</td>
      <td>Fjorn’s Anvil</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4496</td>
      <td>Jotunheim</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4497</td>
      <td>Savage Ledge</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4498</td>
      <td>Halls of the Ancestors</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4499</td>
      <td>The Blighted Pool</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4500</td>
      <td>The Eye of Eternity</td>
      <td>616</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4501</td>
      <td>The Argent Vanguard</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4502</td>
      <td>Mimir’s Workshop</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4503</td>
      <td>Ironwall Dam</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4504</td>
      <td>Valley of Echoes</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4505</td>
      <td>The Breach</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4506</td>
      <td>Scourgeholme</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4507</td>
      <td>The Broken Front</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4508</td>
      <td>Mord’rethar: The Death Gate</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4509</td>
      <td>The Bombardment</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4510</td>
      <td>Aldur’thar: The Desolation Gate</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4511</td>
      <td>The Skybreaker</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4512</td>
      <td>Orgrim’s Hammer</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4513</td>
      <td>Ymirheim</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4514</td>
      <td>Saronite Mines</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4515</td>
      <td>The Conflagration</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4516</td>
      <td>Ironwall Rampart</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4517</td>
      <td>Weeping Quarry</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4518</td>
      <td>Corp’rethar: The Horror Gate</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4519</td>
      <td>The Court of Bones</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4520</td>
      <td>Malykriss: The Vile Hold</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4521</td>
      <td>Cathedral of Darkness</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4522</td>
      <td>Icecrown Citadel</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4523</td>
      <td>Icecrown Glacier</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4524</td>
      <td>Valhalas</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4525</td>
      <td>The Underhalls</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4526</td>
      <td>Njorndar Village</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4527</td>
      <td>Balargarde Fortress</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4528</td>
      <td>Kul’galar Keep</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4529</td>
      <td>The Crimson Cathedral</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4530</td>
      <td>Sanctum of Reanimation</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4531</td>
      <td>The Fleshwerks</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4532</td>
      <td>Vengeance Landing Inn</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4533</td>
      <td>Sindragosa’s Fall</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4534</td>
      <td>Wildervar Mine</td>
      <td>571</td>
      <td>495</td>
    </tr>
    <tr>
      <td>4535</td>
      <td>The Pit of the Fang</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4536</td>
      <td>Frosthowl Cavern</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4537</td>
      <td>The Valley of Lost Hope</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4538</td>
      <td>The Sunken Ring</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4539</td>
      <td>The Broken Temple</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4540</td>
      <td>The Valley of Fallen Heroes</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4541</td>
      <td>Vanguard Infirmary</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4542</td>
      <td>Hall of the Shaper</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4543</td>
      <td>Temple of Wisdom</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4544</td>
      <td>Death’s Breach</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>4545</td>
      <td>Abandoned Mine</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>4546</td>
      <td>Ruins of the Scarlet Enclave</td>
      <td>0</td>
      <td>139</td>
    </tr>
    <tr>
      <td>4547</td>
      <td>Halls of Stone</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4548</td>
      <td>Halls of Lightning</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4549</td>
      <td>The Great Tree</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4550</td>
      <td>The Mirror of Twilight</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4551</td>
      <td>The Twilight Rivulet</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4552</td>
      <td>The Decrepit Flow</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4553</td>
      <td>Forlorn Woods</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4554</td>
      <td>Ruins of Shandaral</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4555</td>
      <td>The Azure Front</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4556</td>
      <td>Violet Stand</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4557</td>
      <td>The Unbound Thicket</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4558</td>
      <td>Sunreaver’s Command</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4559</td>
      <td>Windrunner’s Overlook</td>
      <td>571</td>
      <td>2817</td>
    </tr>
    <tr>
      <td>4560</td>
      <td>The Underbelly</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4564</td>
      <td>Krasus’ Landing</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4567</td>
      <td>The Violet Hold</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4568</td>
      <td>The Eventide</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4569</td>
      <td>Sewer Exit Pipe</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4570</td>
      <td>Circle of Wills</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4571</td>
      <td>Silverwing Flag Room</td>
      <td>489</td>
      <td>3277</td>
    </tr>
    <tr>
      <td>4572</td>
      <td>Warsong Flag Room</td>
      <td>489</td>
      <td>3277</td>
    </tr>
    <tr>
      <td>4575</td>
      <td>Wintergrasp Fortress</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4576</td>
      <td>Central Bridge</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4577</td>
      <td>Eastern Bridge</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4578</td>
      <td>Western Bridge</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4579</td>
      <td>Dubra’Jin</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4580</td>
      <td>Crusaders’ Pinnacle</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4581</td>
      <td>Flamewatch Tower</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4582</td>
      <td>Winter’s Edge Tower</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4583</td>
      <td>Shadowsight Tower</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4584</td>
      <td>The Cauldron of Flames</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4585</td>
      <td>Glacial Falls</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4586</td>
      <td>Windy Bluffs</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4587</td>
      <td>The Forest of Shadows</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4588</td>
      <td>Blackwatch</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4589</td>
      <td>The Chilled Quagmire</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4590</td>
      <td>The Steppe of Life</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4591</td>
      <td>Silent Vigil</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4592</td>
      <td>Gimorak’s Den</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4593</td>
      <td>The Pit of Fiends</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4594</td>
      <td>Battlescar Spire</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4595</td>
      <td>Hall of Horrors</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4596</td>
      <td>The Circle of Suffering</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4597</td>
      <td>Rise of Suffering</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4598</td>
      <td>Krasus’ Landing</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4599</td>
      <td>Sewer Exit Pipe</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4601</td>
      <td>Dalaran Island</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4602</td>
      <td>Force Interior</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4603</td>
      <td>Vault of Archavon</td>
      <td>624</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4604</td>
      <td>Gate of the Red Sun</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4605</td>
      <td>Gate of the Blue Sapphire</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4606</td>
      <td>Gate of the Green Emerald</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4607</td>
      <td>Gate of the Purple Amethyst</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4608</td>
      <td>Gate of the Yellow Moon</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4609</td>
      <td>Courtyard of the Ancients</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4610</td>
      <td>Landing Beach</td>
      <td>607</td>
      <td>4384</td>
    </tr>
    <tr>
      <td>4611</td>
      <td>Westspark Workshop</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4612</td>
      <td>Eastspark Workshop</td>
      <td>571</td>
      <td>4197</td>
    </tr>
    <tr>
      <td>4613</td>
      <td>Dalaran City</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4614</td>
      <td>The Violet Citadel Spire</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4615</td>
      <td>Naz’anak: The Forgotten Depths</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4616</td>
      <td>Sunreaver’s Sanctuary</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4617</td>
      <td>Elevator</td>
      <td>0</td>
      <td>1497</td>
    </tr>
    <tr>
      <td>4618</td>
      <td>Antonidas Memorial</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4619</td>
      <td>The Violet Citadel</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4620</td>
      <td>Magus Commerce Exchange</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4621</td>
      <td>UNUSED</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4622</td>
      <td>First Legion Forward Camp</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4623</td>
      <td>Hall of the Conquered Kings</td>
      <td>619</td>
      <td>4494</td>
    </tr>
    <tr>
      <td>4624</td>
      <td>Befouled Terrace</td>
      <td>619</td>
      <td>4494</td>
    </tr>
    <tr>
      <td>4625</td>
      <td>The Desecrated Altar</td>
      <td>619</td>
      <td>4494</td>
    </tr>
    <tr>
      <td>4626</td>
      <td>Shimmering Bog</td>
      <td>619</td>
      <td>4494</td>
    </tr>
    <tr>
      <td>4627</td>
      <td>Fallen Temple of Ahn’kahet</td>
      <td>619</td>
      <td>4494</td>
    </tr>
    <tr>
      <td>4628</td>
      <td>Halls of Binding</td>
      <td>229</td>
      <td>1583</td>
    </tr>
    <tr>
      <td>4629</td>
      <td>Winter’s Heart</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4630</td>
      <td>The North Sea</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4631</td>
      <td>The Broodmother’s Nest</td>
      <td>571</td>
      <td>67</td>
    </tr>
    <tr>
      <td>4632</td>
      <td>Dalaran Floating Rocks</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4633</td>
      <td>Raptor Pens</td>
      <td>600</td>
      <td>4196</td>
    </tr>
    <tr>
      <td>4635</td>
      <td>Drak’Tharon Keep</td>
      <td>571</td>
      <td>66</td>
    </tr>
    <tr>
      <td>4636</td>
      <td>The Noxious Pass</td>
      <td>609</td>
      <td>4298</td>
    </tr>
    <tr>
      <td>4637</td>
      <td>Vargoth’s Retreat</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4638</td>
      <td>Violet Citadel Balcony</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4639</td>
      <td>Band of Variance</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4640</td>
      <td>Band of Acceleration</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4641</td>
      <td>Band of Transmutation</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4642</td>
      <td>Band of Alignment</td>
      <td>571</td>
      <td>3537</td>
    </tr>
    <tr>
      <td>4646</td>
      <td>Ashwood Lake</td>
      <td>571</td>
      <td>394</td>
    </tr>
    <tr>
      <td>4650</td>
      <td>Iron Concourse</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4652</td>
      <td>Formation Grounds</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4653</td>
      <td>Razorscale’s Aerie</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4654</td>
      <td>The Colossal Forge</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4655</td>
      <td>The Scrapyard</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4656</td>
      <td>The Conservatory of Life</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4657</td>
      <td>The Archivum</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4658</td>
      <td>Argent Tournament Grounds</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4665</td>
      <td>Expedition Base Camp</td>
      <td>603</td>
      <td>4273</td>
    </tr>
    <tr>
      <td>4666</td>
      <td>Sunreaver Pavilion</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4667</td>
      <td>Silver Covenant Pavilion</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4668</td>
      <td>The Cooper Residence</td>
      <td>0</td>
      <td>40</td>
    </tr>
    <tr>
      <td>4669</td>
      <td>The Ring of Champions</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4670</td>
      <td>The Aspirants’ Ring</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4671</td>
      <td>The Argent Valiants’ Ring</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4672</td>
      <td>The Alliance Valiants’ Ring</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4673</td>
      <td>The Horde Valiants’ Ring</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4674</td>
      <td>Argent Pavilion</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4676</td>
      <td>Sunreaver Pavilion</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4677</td>
      <td>Silver Covenant Pavilion</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4679</td>
      <td>The Forlorn Cavern</td>
      <td>0</td>
      <td>1537</td>
    </tr>
    <tr>
      <td>4688</td>
      <td>claytonio test area</td>
      <td>451</td>
      <td>151</td>
    </tr>
    <tr>
      <td>4692</td>
      <td>Quel’Delar’s Rest</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4710</td>
      <td>Isle of Conquest</td>
      <td>628</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4722</td>
      <td>Trial of the Crusader</td>
      <td>649</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4723</td>
      <td>Trial of the Champion</td>
      <td>650</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4739</td>
      <td>Runeweaver Square</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4740</td>
      <td>The Silver Enclave</td>
      <td>571</td>
      <td>4395</td>
    </tr>
    <tr>
      <td>4741</td>
      <td>Isle of Conquest No Man’s Land</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4742</td>
      <td>Hrothgar’s Landing</td>
      <td>571</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4743</td>
      <td>Deathspeaker’s Watch</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4747</td>
      <td>Workshop</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4748</td>
      <td>Quarry</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4749</td>
      <td>Docks</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4750</td>
      <td>Hangar</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4751</td>
      <td>Refinery</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4752</td>
      <td>Horde Keep</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4753</td>
      <td>Alliance Keep</td>
      <td>628</td>
      <td>4710</td>
    </tr>
    <tr>
      <td>4760</td>
      <td>The Sea Reaver’s Run</td>
      <td>571</td>
      <td>4742</td>
    </tr>
    <tr>
      <td>4763</td>
      <td>Transport: Alliance Gunship</td>
      <td>641</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4764</td>
      <td>Transport: Horde Gunship</td>
      <td>642</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4769</td>
      <td>Hrothgar’s Landing</td>
      <td>571</td>
      <td>4742</td>
    </tr>
    <tr>
      <td>4809</td>
      <td>The Forge of Souls</td>
      <td>632</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4812</td>
      <td>Icecrown Citadel</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4813</td>
      <td>Pit of Saron</td>
      <td>658</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4820</td>
      <td>Halls of Reflection</td>
      <td>668</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4832</td>
      <td>Transport: Alliance Gunship (IGB)</td>
      <td>672</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4833</td>
      <td>Transport: Horde Gunship (IGB)</td>
      <td>673</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4859</td>
      <td>The Frozen Throne</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4862</td>
      <td>The Frozen Halls</td>
      <td>571</td>
      <td>210</td>
    </tr>
    <tr>
      <td>4889</td>
      <td>The Frost Queen’s Lair</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4890</td>
      <td>Putricide’s Laboratory of Alchemical Horrors and Fun</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4891</td>
      <td>The Sanctum of Blood</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4892</td>
      <td>The Crimson Hall</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4893</td>
      <td>The Frost Queen’s Lair</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4894</td>
      <td>Putricide’s Laboratory of Alchemical Horrors and Fun</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4895</td>
      <td>The Crimson Hall</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4896</td>
      <td>The Frozen Throne</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4897</td>
      <td>The Sanctum of Blood</td>
      <td>631</td>
      <td>0</td>
    </tr>
    <tr>
      <td>4898</td>
      <td>Frostmourne</td>
      <td>631</td>
      <td>4896</td>
    </tr>
    <tr>
      <td>4904</td>
      <td>The Dark Approach</td>
      <td>658</td>
      <td>4813</td>
    </tr>
    <tr>
      <td>4905</td>
      <td>Scourgelord’s Command</td>
      <td>658</td>
      <td>4813</td>
    </tr>
    <tr>
      <td>4906</td>
      <td>The Shadow Throne</td>
      <td>668</td>
      <td>4820</td>
    </tr>
    <tr>
      <td>4908</td>
      <td>The Hidden Passage</td>
      <td>668</td>
      <td>4820</td>
    </tr>
    <tr>
      <td>4910</td>
      <td>Frostmourne</td>
      <td>631</td>
      <td>4812</td>
    </tr>
    <tr>
      <td>4987</td>
      <td>The Ruby Sanctum</td>
      <td>724</td>
      <td>0</td>
    </tr>
  </tbody>
</table>


      </div>
