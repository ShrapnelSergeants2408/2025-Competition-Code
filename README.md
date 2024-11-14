# FRC Team 2408 Shrapnel Sergeants - 2025 Competition Code
FRC 2408 main competition code for 2025

## Overview
Primary competition repository for FRC Team 2408's 2025 season robot. This codebase contains all competition-ready code used during the 2025 FRC game season. All code in this repository should be thoroughly tested and competition-ready.

## Robot Hardware
```
Drive Base:
- Swerve Drive (4 modules)
- Module Configuration:
  ├── Drive Motor: [Type TBD]
  ├── Turn Motor: [Type TBD]
  ├── Absolute Encoder: [Type TBD]
  └── Turn Encoder: [Type TBD]

Manipulator:
- [TBD based on game]

Vision:
- Cameras: [Type TBD]
- Processing: [Hardware TBD]

Control System:
- roboRIO 2.0
- REV Power Distribution Hub
- Radio: OpenMesh OM5P-AC
```

## Development Environment Setup

### Required Software
```markdown
1. WPILib 2024.1.1 or newer
2. Visual Studio Code with extensions:
   - WPILib
   - Java Extension Pack
   - Git Graph
3. Vendor Libraries:
   - REVLib
   - Phoenix6
   - PhotonVision
4. Git
```

### Initial Setup
```bash
# Clone repository
git clone https://github.com/FRCTeam2408/2025_Competition_Code.git
cd 2025_Competition_Code

# Build project
./gradlew build
```

## Project Structure
```
src/main/java/frc/robot/
├── subsystems/
│   ├── drive/          # Swerve drive subsystem
│   ├── manipulator/    # Game piece manipulation
│   └── vision/         # Vision processing
├── commands/
│   ├── drive/          # Drive commands
│   ├── manipulator/    # Manipulator commands
│   └── autonomous/     # Autonomous routines
├── constants/          # Robot constants
└── utils/              # Utility classes

src/test/java/frc/robot/  # Test files
```

## Development Workflow

### Branch Structure
```
main           # Competition-ready code only
└── develop    # Main development branch
    ├── feature/   # New features
    ├── fix/       # Bug fixes
    └── chore/     # Maintenance tasks
```

### Development Process
1. Create branch from develop:
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/your-feature
   ```

2. Write code and test:
   ```bash
   # Build and test locally
   ./gradlew build
   ./gradlew test
   
   # Test in simulation
   ./gradlew simulateJava
   ```

3. Create pull request:
   - Push changes to GitHub
   - Create PR targeting develop branch
   - Fill out PR template
   - Request reviews

### Code Reviews
All code must be reviewed before merging:
- Develop branch: 1 reviewer required
- Main branch: 2 reviewers required
- Must include mentor review for main branch

## Competition Procedures

### Pre-Competition Checklist
```markdown
1. Code Verification:
   □ All tests passing
   □ Build successful
   □ Known issues documented
   □ Autonomous modes verified
   □ Dashboard configured

2. Robot Setup:
   □ Code deployed to robot
   □ Radio configured
   □ Dashboard connected
   □ Camera streams verified
   □ Battery voltage checked

3. Backup Preparation:
   □ Code backed up to USB
   □ Configuration files saved
   □ Documentation accessible
   □ Emergency procedures reviewed
```

### Match Procedure
```markdown
1. Pre-Match:
   □ Battery voltage verified
   □ Systems check complete
   □ Autonomous mode selected
   □ Connection verified
   □ Dashboard receiving data

2. During Match:
   □ Monitor robot status
   □ Watch for error messages
   □ Note any issues

3. Post-Match:
   □ Record match data
   □ Document any issues
   □ Save log files
   □ Update issue tracking
```

## Safety Requirements

### Code Safety
```markdown
1. Motor Safety:
   □ Current limiting enabled
   □ Voltage ramping configured
   □ Position limits set
   □ Watchdog enabled

2. Operation Safety:
   □ Emergency stop tested
   □ Fail-safe modes implemented
   □ Sensor validation
   □ Power monitoring
```

### Testing Requirements
```markdown
1. New Features:
   □ Unit tests written
   □ Integration tests completed
   □ Simulation tested
   □ Practice bot verified
   □ Safety checks validated

2. Changes to Existing Code:
   □ Regression tests run
   □ Integration verified
   □ Documentation updated
   □ Safety systems checked
```

## Build and Deploy

### Build Commands
```bash
# Clean build
./gradlew clean

# Build project
./gradlew build

# Run tests
./gradlew test

# Deploy to robot
./gradlew deploy
```

### Deployment Process
```markdown
1. Practice Bot Testing:
   □ Deploy code
   □ Test all systems
   □ Verify autonomous
   □ Check fail-safes
   □ Document results

2. Competition Bot Deployment:
   □ Code review completed
   □ All tests passing
   □ Practice bot validated
   □ Mentor approval received
```

## Documentation Requirements

### Code Documentation
- All public methods must have Javadoc
- Complex logic must be commented
- Constants must be documented
- Safety features must be clearly marked

### System Documentation
- Subsystem capabilities and limits
- Autonomous routine descriptions
- Known issues and workarounds
- Configuration procedures
- Emergency procedures

## Support

### Emergency Procedures
1. Code issues during competition:
   - Access backup code from USB
   - Revert to last known good state
   - Contact available mentors
   - Document all changes

2. Robot communication issues:
   - Check radio connection
   - Verify network configuration
   - Check roboRIO connection
   - Verify dashboard status

### Contact Information
```markdown
Team Contacts:
- Team Email: [team email]
- Mentors:
  - Dan Hiebert
  - Josh Kupka
  - Stephanie
- Student Lead: Taaliyah
```

## Resources
- [Team 2408 Wiki](wiki_link)
- [Game Manual](game_manual_link)
- [WPILib Documentation](wpilib_link)
- [FIRST Robotics Competition](frc_link)
- [Chief Delphi](chiefdelphi_link)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
