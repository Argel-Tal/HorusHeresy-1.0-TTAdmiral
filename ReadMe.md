# HorusHeresy-1.0-TTAdmiral
## Purpose: 
__Repository for Horus Heresy 1.0 data for use with Tabletop Admiral army builder__
Supporting Heresy 1.0 given the BattleScribe repos for 1.0 are no longer being maintained, and BattleScribe is now effectively abandon-ware. 

## Implementation
Horus Heresy 1st Edition is based on the Warhammer 6th-7th Edition framework

### Selecting an Army
#### Factions
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

Groupings where there is no actual faction in that field are for the purposes of the Ally Matrix, where all subfactions are treated as one entry

```json
{
    "name": "Mechanicum"
}, 
{
    "name": "Taghmata",
    "parentFaction": "Mechanicum",
}, 
{
    "name": "Ordo Reductor",
    "parentFaction": "Taghmata",
}
```

#### Force Orgs
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

#### Alignment
- Loyalist
- Traitor
- Neutral / 3rd Party

#### Process
1. Faction
0. Force Org
0. Alignment
0. Rite of War (if Legiones Astartes)

### Unit Types
#### List
- Infantry
    - Jet Pack
    - Mounted
        - Bike
        - Jetbike
        - Cavalry
    - Beast
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
Infantry --|> Jump
Infantry --|> Mounted
Infantry --|> Beast
Infantry --|> Artillery
Mounted --|> Bike
Mounted --|> Jetbike
Mounted --|> Cavalry
Infantry --|> Chariot
Vehicle --|> Chariot
Vehicle --|> Walker
Infantry : int Mv = 6
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
Walker  :   int S
Walker  :   int WS
Walker  :   int I
Walker  :   int A
Mounted :   int Mv = 12
Beast :   int Mv = 12
Jump    :   int Mv = 6/12
Artillery   :   int WS = NA
Artillery   :   int BS = NA
Artillery   :   int S = NA
Artillery   :   int I = NA
Artillery   :   int A = NA
Artillery   :   int Ld = NA
```

### Unit Implementation Plan
#### Examples
##### Angron
```json
{
    "name": "Angron - Lord of the Red Sands",
    "factions": [
        {
            "name": "World Eaters",
            "Crusade-ForceOrgSlot": "HQ"
		},
		{
		    "name": "World Eaters",
            "Crusade-ForceOrgSlot": "Lord of War"
        },
        {
            "name": "Dark Compliance",
            "Crusade-ForceOrgSlot": "Lord of War"
        }			
    ],
    "alignment": [
        {
            "name": "Traitors"
        }
    ], 
    "requiredIn": [
        "Primarch's Chosen",
    ],
    "points": 400ish,
    "movement": 6,
    "weaponSkill": 999,
    "ballisticSkill": 666,
    "strength": 444,
    "toughness": 555,
    "initative": 333,
    "attacks": 333,
    "wounds": 6,
    "leadership": 6,
    "save": 3,
    "invulnSave": 3,
    "UnitType": [
    	"Infantry"
    ],
    "options": [
    	{
    		"name": "a fake upgrade",
    		"points": 40,
    		"availableIn": [
    			"World Eaters"
    		]
    	},
    	{
    		"name": "a fake upgrade",
    		"points": 0,
    		"availableIn": [
    			"Dark Compliance"
    		],
    		"requiredIn": [
    			"Dark Compliance"
    		]
    	}
    ],
    "specialRules": [
    	"Primarch",
    	"..."
    ],
    "wargear": [
    	"Gorechild"
    ]
}
```

##### Garrow
```json
loyalistOnly        =   TRUE
HQ                  =   TRUE
Mechanicum          =   TRUE
LegionesAstartes    =   TRUE
CrusadeImperialis   =   TRUE
```

##### Leman Russ Executioner
```json
HeavySupport        =   TRUE
CrusadeImperialis   =   TRUE
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

