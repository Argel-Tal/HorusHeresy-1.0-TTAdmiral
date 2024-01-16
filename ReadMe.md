# HorusHeresy-1.0-TTAdmiral
## Purpose: 
__Repository for Horus Heresy 1.0 data for use with Tabletop Admiral army builder__
Supporting Heresy 1.0 given the BattleScribe repos for 1.0 are no longer being maintained, and BattleScribe is now effectively abandon-ware. 

## Implementation
Horus Heresy 1st Edition is based on the Warhammer 6th-7th Edition framework
### Alignment
- Loyalist
- Traitor
- Neutral / 3rd Party

### Factions
#### List
- Legiones Astartes
    - I: Dark Angels
    - III: Emperor's Children
    - IV: Iron Warriors
    - V: White Scars
    - VI: Space Wolves
    - VII: Imperial Fists
    - VIII: Night Lords
    - IX: Blood Angels
    - X: Iron Hands
    - XII: World Eaters
    - XIII: Ultramarines
    - XIV: Death Guard
    - XV: Thousand Sons
    - XVI: Sons of Horus
    - XVII: Word Bearers
    - XVIII: Salamanders
    - XIX: Raven Guard
    - XX: Alpha Legion

- Mechanicum
    - Taghamata
    - Legio Cybernetica
    - Ordo Reductor
    - Questoris Knights
- Crusade Imperialis
    - Solar Auxilia
    - Militia and Cults
- Other
    - Daemons of the Ruinstorm
    - Army of Dark Compliance

#### Diagram
```mermaid
mindmap
  root((FactionList))
    LegionesAstartes
        Dark Angels
        Emperor's Children
        Iron Warriors
        White Scars
        Space Wolves
        Imperial Fists
        Night Lords
        Blood Angels
        Iron Hands
        World Eaters
        Ultramarines
        Death Guard
        Thousand Sons
        Sons of Horus
        Word Bearers
        Salamanders
        Raven Guard
        Alpha Legion
    Mechanicum
        Taghamata
        Legio Cybernetica
        Ordo Reductor
        Questoris Knights
    CrusadeImperialis
        Solar Auxilia
        Militia & Cults
    Other
        Daemons of the Ruinstorm
        Army of Dark Compliance
```

### Force Orgs
- Crusade
- Allied Detachment
- Onslaught
- Leviathan
- Castelland
- Matrix of Ruin
- Army of Dark Compliance
- Strategic Raid Garrison
- Strategic Raid Raider
- Zone Mortalis Attacker
- Zone Mortalis Defender
- Zone Mortalis Combatant

### Unit Types
#### List
- Infantry
    - Boosted
        - Jump
        - Jet Pack
    - Mounted
        - Bike
        - Jetbike
        - Cavalry
    - Beast
    - Monstrous Creature
    - Artillery
- Vehicle
    - Flyer
    - Chariot
    - Walker

#### Unit Type Map
```mermaid
classDiagram
UnitContainer --|> Infantry
UnitContainer --|> Vehicle
UnitContainer : str SpecialRules(s)
UnitContainer : bool LoyalistOnly
UnitContainer : bool TraitorOnly
Infantry --|> Boosted
Infantry --|> Mounted
Infantry --|> Beast
Infantry --|> Monstrous Creature
Infantry --|> Artillery
Boosted --|> Jump
Boosted --|> Jet Pack
Mounted --|> Bike
Mounted --|> Jetbike
Mounted --|> Cavalry
Vehicle --|> Flyers
Vehicle --|> Chariots
Vehicle --|> Walkers
Infantry : int Mv
Infantry : int WS
Infantry : int BS
Infantry : int S
Infantry : int T
Infantry : int I
Infantry : int A
Infantry : int Wd
Infantry : int Ld
Infantry : int Save
Infantry : int ISave
Infantry : str Type(s)
Vehicle : int BS
Vehicle : int Front AV
Vehicle : int Side AV
Vehicle : int Rear AV
Vehicle : int Front HP
Vehicle : str Type(s)
```

## Links
### Client
- <a href="https://modular.tabletopadmiral.com/">Tabletop admiral webApp</a>
### Data files
- <a href="https://nowforwrath.github.io/data.json">Now for Wrath's MESBG datafile</a>
- <a href="https://github.com/BSData/horus-heresy-1e">Horus Heresy 1st</a>
- <a href="https://github.com/BSData/horus-heresy">Horus Heresy 2nd</a>
### Resources
- <a href="https://scoolov.github.io/wh40000rules/home-page/">Wahapedia Warhammer 40k 7th</a>

