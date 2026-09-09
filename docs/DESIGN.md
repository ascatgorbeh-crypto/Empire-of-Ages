# Empire of Ages - Game Design Document

## Overview

Empire of Ages is a massive civilization-building strategy game where players progress from a small settlement to a vast empire.

## Progression System

### Settlement Progression

```
House (1-10 population)
    ↓ (Requires 10 population, basic buildings)
Village (10-50 population)
    ↓ (Requires 50 population, market)
Town (50-200 population)
    ↓ (Requires 200 population, barracks)
City (200-500 population)
    ↓ (Requires 500 population, palace)
Metropolis (500-1000 population)
    ↓ (Requires 1000 population, advanced buildings)
Capital (1000-2000 population)
    ↓ (Requires control of 3+ territories)
Kingdom (2000-5000 population)
    ↓ (Requires control of 6+ territories, advanced army)
Empire (5000+ population, 10+ territories)
```

## Civilizations

### Achaemenid (هخامنشیان)
- **Era**: Ancient Persia
- **Strengths**: Diplomacy, Administration, Cavalry
- **Unique Unit**: Immortals (Elite Guards)
- **Special Building**: Royal Palace
- **Bonus**: +25% Diplomacy success, +15% Revenue
- **Weakness**: Slower unit training

### Parthian (اشکانیان)
- **Era**: Classical Persia
- **Strengths**: Mounted Archery, Hit-and-run tactics
- **Unique Unit**: Cataphract (Heavy Cavalry)
- **Special Building**: Horse Training Ground
- **Bonus**: +30% Horse unit speed, +20% Archer damage
- **Weakness**: Weak defense

### Sassanid (ساسانیان)
- **Era**: Late Persia
- **Strengths**: Heavy Armor, Fortifications
- **Unique Unit**: War Elephant
- **Special Building**: Siege Engineering Academy
- **Bonus**: +30% Defense, +25% Siege effectiveness
- **Weakness**: Slower units

### Greek
- **Era**: Classical Greece
- **Strengths**: Philosophy, Culture, Phalanx
- **Unique Unit**: Hoplite (Heavy Infantry)
- **Special Building**: Academy
- **Bonus**: +20% Technology research, +15% Culture
- **Weakness**: Expensive units

### Roman
- **Era**: Classical Rome
- **Strengths**: Engineering, Military discipline
- **Unique Unit**: Legionnaire
- **Special Building**: Forum
- **Bonus**: +25% Building construction, +20% Military experience
- **Weakness**: Limited cavalry

### Viking
- **Era**: Medieval Scandinavia
- **Strengths**: Naval warfare, Raiding
- **Unique Unit**: Berserker
- **Special Building**: Shipyard
- **Bonus**: +30% Naval combat, +20% Raiding rewards
- **Weakness**: Limited defense buildings

## Resources

### Primary Resources

1. **Food** 🌾
   - Production: Farms, Hunters
   - Consumption: Population (1 per person per day)
   - Uses: Population growth, Armies

2. **Wood** 🌳
   - Production: Lumber mills, Forests
   - Uses: Building construction, Weapons
   - Storage: Warehouses

3. **Stone** 🪨
   - Production: Quarries, Mountains
   - Uses: Building construction, Fortifications
   - Uses: Advanced buildings

4. **Iron** ⚙️
   - Production: Iron mines
   - Uses: Weapons, Tools, Armor
   - Rarity: Medium

5. **Gold** 💰
   - Production: Gold mines, Trade
   - Uses: Trade, Special buildings
   - Value: High

6. **Horses** 🐴
   - Production: Stables
   - Uses: Cavalry, Transportation
   - Rarity: Medium

7. **Copper** 🔶
   - Production: Copper mines
   - Uses: Weapons, Decoration
   - Rarity: Medium

## Building System

### Building Categories

#### Residential
- **Hut**: 1 population
- **House**: 2 population
- **Manor**: 4 population
- **Palace**: 8 population + administrative bonuses

#### Production
- **Farm**: +2 Food per cycle
- **Lumber Mill**: +2 Wood per cycle
- **Quarry**: +2 Stone per cycle
- **Mine**: +1 Metal per cycle (Iron/Copper/Gold)
- **Hunter's Lodge**: +1 Food per cycle

#### Commercial
- **Market**: Trading hub, +10% Trade efficiency
- **Merchant House**: +2 Trade routes
- **Bazaar**: Improved trading

#### Military
- **Barracks**: Train soldiers (Recruits, Soldiers, Veterans)
- **Archery Range**: Train archers
- **Stable**: Train cavalry, breed horses
- **Siege Workshop**: Train siege units
- **Watchtower**: Defense +5, visibility +1
- **Fortress**: Strong defense point
- **Wall**: Defense structure

#### Infrastructure
- **Road**: Movement speed +20%
- **Bridge**: Cross rivers
- **Harbor**: Naval operations
- **Warehouse**: +5 storage for resources
- **Granary**: +10 food storage

#### Special
- **Temple**: +5% Happiness, Culture
- **Library**: +2 Technology research speed
- **Hospital**: Population health
- **University**: +3 Technology research
- **Blacksmith**: Equipment upgrades
- **Armory**: Equipment storage

## Combat System

### Unit Types

#### Infantry
- **Recruit**: Weak, trains fast
- **Soldier**: Balanced unit
- **Veteran**: Experienced, high damage
- **Elite Guard**: Best infantry

#### Archers
- **Bowman**: Basic ranged unit
- **Archer**: Improved version
- **Master Archer**: Best ranged unit

#### Cavalry
- **Horseman**: Light cavalry
- **Knight**: Medium cavalry
- **Heavy Cavalry**: Strong cavalry unit
- **Cataphract**: Armored cavalry (Parthian)

#### Siege
- **Battering Ram**: Attack buildings
- **Catapult**: Long-range siege
- **Siege Tower**: Assault fortifications
- **War Elephant**: Unique unit

### Battle Mechanics

#### Factors
- Unit count
- Unit quality
- Unit experience
- Equipment level
- Terrain (forest +20% defense, open -20% defense)
- Commander stats
- Morale
- Supply (food, weapons)

#### Battle Flow
1. Armies encounter
2. Pre-battle configuration
3. Battle simulation
4. Casualty calculation
5. Reward distribution

#### Damage Calculation
```
Damage = (UnitAttack + Equipment) × Terrain × Morale × Experience
Final Damage = Damage - (Defense × DefenseMultiplier)
```

## Economy System

### Income
- Taxation: Population × Tax Rate
- Trade: Trade routes × Resource value
- Market: Selling surplus resources
- Plunder: Raiding enemies

### Expenses
- Population: Food consumption
- Armies: Soldier maintenance
- Buildings: Maintenance costs
- Research: Technology cost
- Diplomacy: Alliance costs

### Trading
- Player to Player
- NPC Trading Posts
- Market fluctuations
- Resource value changes
- Trade routes between settlements

## Technology System

### Tech Trees
Each civilization has unique technologies:
- Agriculture improvements
- Military advancements
- Construction techniques
- Economic development
- Cultural progress

### Research
- Universities provide research
- Libraries boost research speed
- Cost in resources
- Time-based completion
- Unlock new buildings/units

## NPC System

### NPC Types
- Farmer
- Worker
- Miner
- Merchant
- Soldier
- Blacksmith
- Doctor
- Scholar

### NPC Behavior
- Wake up (Morning)
- Work shift (Day)
- Rest (Evening/Night)
- Repeat

### NPC Interaction
- Hire/Fire
- Assign jobs
- Check stats
- Trade with
- Recruit into army

## Diplomacy System

### Relationships
- Neutral (0)
- Friendly (+1 to +50)
- Allied (+50+)
- Hostile (-1 to -50)
- War (-50-)

### Actions
- Send gift
- Declare war
- Propose alliance
- Trade agreement
- Peace treaty

### Effects
- Shared vision
- Joint attacks
- Trade bonuses
- Shared buildings
- Defensive pacts

## Territory System

### Territory Control
- Settlements control surrounding territory
- Territory shown on map
- Cannot build in enemy territory
- Battle for control
- Claim new territory

### Territory Benefits
- Resource gathering
- Population limit increase
- Strategic advantage
- Trade route control

## Time System

### Day/Night Cycle
- 1 in-game day = 20 minutes real time (configurable)
- 4 cycles per in-game hour
- Visual changes (lighting, colors)
- NPC behavior changes
- Activity differences

### Seasons (Future)
- Spring: Farming, planting
- Summer: Growth, full production
- Autumn: Harvest
- Winter: Reduced production, maintenance

## Save System

### Saved Data
- Player civilization
- Settlement data
- Building list and status
- Population statistics
- Resource amounts
- Technology progress
- Relationship status
- Territory control
- Army composition
- Time/date
- Game settings

### Save Slots
- Multiple saves supported
- Auto-save feature
- Cloud save (future)

---

For implementation details, see ARCHITECTURE.md
