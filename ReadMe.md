# HorusHeresy-1.0-TTAdmiral
## Purpose: 
__Repository for Horus Heresy 1.0 data for use with Tabletop Admiral army builder__
Supporting Heresy 1.0 given the BattleScribe repos for 1.0 are no longer being maintained, and BattleScribe is now effectively abandon-ware. 

## Implementation
Horus Heresy 1st Edition is based on the Warhammer 6th-7th Edition framework
### Factions
#### List
- Legiones Astartes
    - I: Dark Angels (The First)
    - III: Emperor's Children
    - IV: Iron Warriors
    - V: White Scars
    - VI: Space Wolves
    - VII: Imperial Fists
    - VIII: Night Lords
    - IX: Blood Angels
    - X: Iron Hands
    - XII: World Eaters (War Hounds)
    - XIII: Ultramarines
    - XIV: Death Guard (Dusk Raiders)
    - XV: Thousand Sons
    - XVI: Black Legion (Sons of Horus, Luna Wolves)
    - XVII: Word Bearers (Imperial Heralds)
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
graph TD;
    LegionesAstartes-->X;
    Mechanicum-->Taghamata;
    Mechanicum-->LegioCybernetica;
    Mechanicum-->OrdoReductor;
    Mechanicum-->QuestorisKnights;
    CrusadeImperialis-->SolarAuxilia;
    CrusadeImperialis-->Militia&Cults;
    Other-->DaemonsOfTheRuinstorm;
    Other-->ArmyOfDarkCompliance;
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
Infantry --|> Boosted
Infantry --|> Mounted
Infantry --|> Beast
Infantry --|> Boosted
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

