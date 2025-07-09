# Nexus King Galactic Smash Simulator

A tactical simulation for the Galactic Smash mechanic on Nexus-King Salhadaar in Manaforge: Omega.

## Getting Started

### Basic Setup
1. Open the HTML file in a web browser
2. The arena will display with radial guide markers
3. Use the control panel to configure your simulation

### Control Panel
- **Play/Pause/Reset**: Control simulation state
- **Speed Slider**: Adjust simulation speed (0.1x to 3x)
- **Checkboxes**: Toggle various modes and features

## Game Elements

### Cores (Red Circles)
- **Size**: 75px diameter (1 unit)
- **Movement**: Orbit around arena center in circular paths
- **Rotation**: Can be clockwise (CW) or counter-clockwise (CCW)
- **Expansion**: Generate outward-expanding rings every 2 seconds
- **Lifespan**: Create 15 expansion rings before stopping

#### Core Mechanics
- **0th Interval**: 2-second delay before first expansion ring
- **Expansion Rings**: 28.5px wide rings that move outward from core
- **Speed**: 75px per 5 seconds orbital movement
- **Numbering**: Cores are automatically numbered (CW1, CCW2, etc.)

### Nexus King (White Circle)
- **Size**: 37.5px diameter (half core size)
- **Function**: Defensive unit with beam weapons
- **Countdown**: 7-second preparation timer
- **Lifespan**: Disappears after 8 seconds total

#### Nexus King Timeline
1. **0-7 seconds**: Countdown display, preparation phase
2. **7 seconds**: Fires precision beams to destroy cores
3. **8 seconds**: Unit disappears from battlefield

### Guardians (Gray Circles)
- **Size**: 22.5px diameter
- **Count**: 3 guardians per Nexus King
- **Positioning**: 120° apart around NK at 37.5px distance
- **Function**: Beam weapon platforms with targeting systems

#### Guardian Targeting System
- **Blue Line**: 6px wide targeting beam (adjustable length/direction)
- **Tracker Dot**: 12px blue dot at end of targeting line
- **Beam Physics**: Fires along line direction, destroys closest intersecting core

## How to Use

### Placing Elements

#### Adding Cores
1. Ensure "Place Nexus King" is **unchecked**
2. Set rotation direction with "Clockwise Rotation" checkbox
3. Click anywhere within the arena
4. Core will appear and begin orbiting when simulation starts

#### Adding Nexus King
1. Check "Place Nexus King" checkbox
2. Click desired location in arena
3. NK appears immediately with 3 guardians
4. Click again to reposition existing NK

### Targeting System

#### Adjusting Guardian Beams
1. **Pause** the simulation
2. Check "Set Lines" checkbox
3. Drag blue tracker dots to aim guardian beams
4. Line length and angle adjust automatically
5. Uncheck "Set Lines" to resume normal placement mode

#### Targeting Tips
- Longer lines = longer range
- Point directly at core paths for best accuracy
- Each guardian operates independently
- Beams only fire forward along the line direction

### Simulation Controls

#### Running the Simulation
1. **Play**: Starts movement, countdowns, and physics
2. **Pause**: Freezes all movement (allows targeting adjustments)
3. **Reset**: Clears expansion rings, resets NK countdown (keeps placed elements)
4. **Speed**: Adjust overall simulation speed

#### Visual Aids
- **Show Markers**: Toggle radial guide lines (0°, 60°, 120°)
- **Arena boundaries**: 400px radius from center
- **Core count**: Displays total active elements

## Game Mechanics

### Combat System
- **Beam Targeting**: Guardians fire along their targeting lines
- **Core Destruction**: Beams destroy the closest core they intersect
- **Precision Strikes**: Only one core destroyed per beam
- **Range**: Unlimited beam range across entire arena

### Physics Engine
- **Orbital Mechanics**: Cores follow perfect circular paths
- **Collision Detection**: Mathematical line-circle intersection
- **Real-time Updates**: 60 FPS animation loop
- **Expansion Timing**: Precise 2-second intervals

### Strategy Elements
- **Positioning**: NK placement affects guardian coverage
- **Timing**: 7-second preparation window for targeting
- **Prediction**: Account for core movement when aiming
- **Resource Management**: Limited to one NK per simulation

## Technical Specifications

### Arena Properties
- **Size**: 800x800 pixels
- **Center**: (400, 400)
- **Active Radius**: 400px from center
- **Background**: Scalable arena image

### Performance
- **Animation**: RequestAnimationFrame for smooth 60 FPS
- **Collision Detection**: Optimized mathematical calculations
- **Memory Management**: Automatic cleanup of removed elements
- **Browser Compatibility**: Modern browsers with ES6 support

## Tips and Strategies

### Effective Core Placement
- Vary orbital distances for complex patterns
- Mix clockwise and counter-clockwise rotations
- Consider expansion ring interference
- Account for 7-second NK preparation time

### Optimal NK Positioning
- Central placement maximizes guardian coverage
- Consider core orbital paths when positioning
- Account for guardian 120° separation
- Position for maximum beam intersection opportunities

### Advanced Targeting
- Lead moving targets by predicting positions
- Use longer lines for distant cores
- Coordinate multiple guardians for area denial
- Time NK placement for maximum effectiveness

## Troubleshooting

### Common Issues
- **Elements not placing**: Check if "Set Lines" mode is active
- **Beams not firing**: Ensure 7-second countdown completes
- **Targeting not working**: Verify simulation is paused and "Set Lines" is checked
- **Performance issues**: Reduce speed multiplier or limit number of cores

### Browser Requirements
- Modern web browser with JavaScript enabled
- No additional plugins or installations required
- Responsive design works on various screen sizes

## Blog Reference
For updates and additional information, check: https://humbleguild.blogspot.com/

---

*Developed as an interactive tactical simulation for strategic gameplay and physics experimentation.*