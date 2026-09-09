# Empire of Ages - Architecture

## System Overview

```
┌─────────────────────────────────────────────────────────┐
│                  GAME LOOP (Main)                        │
└─────────────────────────────────────────────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        ���                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ TimeManager  │  │  UIManager   │  │ InputManager │
└──────────────┘  └──────────────┘  └──────────────┘
        │                   │                   │
        └───────────────────┼───────────────────┘
                            │
        ┌───────────────────┼───────────────────┐
        │                   │                   │
        ▼                   ▼                   ▼
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│WorldManager  │  │PlayerManager │  │NPCManager    │
└──────────────┘  └──────────────┘  └──────────────┘
        │
        ├─ SettlementManager
        ├─ ResourceManager
        ├─ EconomyManager
        ├─ MilitaryManager
        ├─ TerritoryManager
        └─ BattleManager
```

## Core Systems

### 1. GameManager
**Responsibility**: Main game controller
- Initialization
- Game state
- Scene management
- Global updates

### 2. WorldManager
**Responsibility**: World simulation
- World generation
- Tile management
- Geography
- Environmental effects

### 3. PlayerManager
**Responsibility**: Player state
- Player data
- Civilization selection
- Player statistics
- Progress tracking

### 4. SettlementManager
**Responsibility**: Settlement operations
- Settlement creation
- Building management
- Building placement
- Settlement upgrades

### 5. ResourceManager
**Responsibility**: Resource system
- Resource tracking
- Resource production
- Resource consumption
- Inventory management

### 6. EconomyManager
**Responsibility**: Economic simulation
- Trade system
- Market prices
- Taxes
- Income/expenses

### 7. PopulationManager
**Responsibility**: Population system
- Population tracking
- Job assignments
- Population growth
- Happiness

### 8. MilitaryManager
**Responsibility**: Military operations
- Unit management
- Army organization
- Unit training
- Equipment management

### 9. BattleManager
**Responsibility**: Combat system
- Battle simulation
- Damage calculation
- Unit effects
- Victory conditions

### 10. TerritoryManager
**Responsibility**: Territory control
- Territory ownership
- Border management
- Territory expansion
- Territory claims

### 11. NPCManager
**Responsibility**: NPC simulation
- NPC spawning
- NPC behavior
- Daily routines
- AI decisions

### 12. TimeManager
**Responsibility**: Time simulation
- Day/night cycle
- Game speed
- Time events
- Timers

### 13. UIManager
**Responsibility**: User interface
- HUD management
- Panel updates
- Menu control
- Input handling

### 14. SaveManager
**Responsibility**: Data persistence
- Game saving
- Game loading
- Data serialization
- Backup management

### 15. DiplomacyManager
**Responsibility**: Player relations
- Alliance system
- Diplomacy state
- Trade agreements
- War status

## Data Flow

```
Player Input
    ↓
InputManager
    ↓
UI/Game Logic
    ↓
Specific Manager (Settlement, Military, etc.)
    ↓
World/Data Update
    ↓
UI Refresh
    ↓
Render
```

## File Organization

### Source Code (src/)
- `managers/` - Manager systems
- `world/` - World generation and management
- `settlement/` - Settlement and building systems
- `civilization/` - Civilization definitions
- `resources/` - Resource system
- `military/` - Military units and battles
- `economy/` - Economic system
- `npc/` - NPC and AI systems
- `ui/` - User interface
- `save/` - Save/load systems
- `utils/` - Utility functions

### Assets (assets/)
- `textures/` - All images
- `scenes/` - Godot scenes (.tscn)
- `audio/` - Music and sound effects
- `fonts/` - Custom fonts

### Data (data/)
- `.json` files for game configuration
- Balance data
- Civilization definitions
- World map templates

### Configuration (config/)
- Game settings
- Graphics settings
- Audio settings
- Gameplay balance

## Design Patterns

### Singleton Pattern
Managers are singletons accessible globally:
```gdscript
GameManager.instance()
WorldManager.instance()
```

### Observer Pattern
Systems listen to events:
```gdscript
EventBus.connect("resource_changed", self, "_on_resource_changed")
```

### Factory Pattern
Creating complex objects:
```gdscript
UnitFactory.create_unit("soldier", position)
```

### Component Pattern
Buildings and units have components:
```gdscript
unit.get_component("health")
unit.get_component("movement")
```

## Performance Considerations

1. **Object Pooling**: Reuse objects instead of creating/deleting
2. **LOD (Level of Detail)**: Reduce detail at distance
3. **Spatial Partitioning**: Divide world into sections
4. **Data Streaming**: Load/unload data as needed
5. **Event Aggregation**: Batch updates instead of individual
6. **Memory Management**: Careful allocation and deallocation

## Security Considerations

1. **Server Authority**: Critical game state on server
2. **Input Validation**: All player input verified
3. **Anti-Cheat**: Detect suspicious behavior
4. **Encryption**: Sensitive data encrypted
5. **Rate Limiting**: Prevent spam/abuse

## Scalability

### Mobile Optimization
- Reduce draw calls
- Optimize physics
- Memory-efficient data structures
- Async loading

### Expandability
- Modular systems
- Plugin architecture
- Data-driven design
- Configuration files

---

For more information, see other documentation files.
