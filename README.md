# MentorshipProjekt

A medieval village simulation game built with **Unreal Engine 5.7**, featuring family management, economic systems, skill progression, and NPC interactions in a richly detailed medieval setting.

## 📋 Table of Contents

- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Building the Project](#building-the-project)
- [Project Structure](#project-structure)
- [Gameplay Overview](#gameplay-overview)
- [Architecture](#architecture)
- [Support & Documentation](#support--documentation)
- [Contributing](#contributing)
- [Team](#team)

## About the Project

MentorshipProjekt is an immersive medieval village simulation experience where players manage family members, develop their skills, and navigate economic challenges. The game combines strategic family management with real-time interactions in a living medieval community filled with NPCs, workstations, and environmental storytelling.

### Why This Project?

This project demonstrates:
- **Complex Systems Design**: Economy, reputation, skill progression, and time management systems working in tandem
- **Advanced Gameplay Architecture**: NPC AI, interaction systems, and real-time simulation
- **Production-Quality Assets**: Medieval environments, characters, and interactive objects
- **Scalable C++ Architecture**: Modular subsystems for extensible gameplay features

## Key Features

✨ **Family Management System**
- Create and manage family members with unique attributes
- Progress through skill trees and unlock new abilities
- Track family reputation and economic status

💰 **Economy & Progression**
- Dynamic gold and expense system
- Reputation tracking affecting gameplay
- Income generation through work shifts and customer interactions

🏘️ **Medieval Village Environment**
- Detailed medieval locations including taverns, markets, and residential areas
- Interactive workstations for various professions (kitchen, carpentry, etc.)
- Day-night cycle with work shifts and schedules

👥 **NPC Interaction System**
- Customer interactions and trading mechanics
- Family member AI with behavioral patterns
- Context-sensitive interaction menus

🎮 **Skill & Progression System**
- Multiple skill types with progression tracking
- Gameplay tag-based skill identification
- Real-time skill development feedback

🎨 **Rich Visual Presentation**
- Professional-grade medieval assets and environments
- Advanced rendering with ray-tracing support
- Optimized performance with Oodle compression

## Getting Started

### Prerequisites

- **Unreal Engine 5.7** (or later compatible version)
- **Visual Studio 2022** (for C++ development)
- **Git** (for version control)
- **Minimum System Requirements**:
  - OS: Windows 10/11
  - CPU: 6-core processor or better
  - RAM: 16 GB
  - GPU: RTX 2080 or equivalent (for ray-tracing features)
  - Disk Space: ~100 GB for full installation with assets

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Ubisoft-Mentorship-Projekt/MentorshipProjekt.git
   cd MentorshipProjekt
   ```

2. **Download Unreal Engine 5.7**:
   - Visit the [Epic Games Launcher](https://www.epicgames.com/download)
   - Install Unreal Engine 5.7
   - Associate it with this project

3. **Generate Visual Studio project files**:
   ```bash
   # Right-click MentorshipProjekt.uproject
   Generate Visual Studio project files
   ```

4. **Open the project**:
   - Double-click `MentorshipProjekt.uproject`
   - The editor will compile shaders and load the project (first load may take 5-10 minutes)

### Building the Project

**From Visual Studio**:
```bash
# Open MentorshipProjekt.sln
# Select Win64 | Development configuration
# Build > Build Solution (Ctrl+Shift+B)
```

**From Unreal Editor**:
- Tools > Compile
- Tools > Refresh Visual Studio Project

**Packaging for Distribution**:
```
File > Package Project > Windows (64-bit)
```

## Project Structure

```
MentorshipProjekt/
├── Source/                          # C++ source code
│   ├── MentorshipProjekt/          # Main game module
│   │   ├── Player/                 # Player character and controller systems
│   │   ├── NPCs/                   # NPC systems (customers, family members, AI)
│   │   ├── InteractionSystem/      # Object interaction and menus
│   │   ├── Areas/                  # Location-based systems
│   │   ├── GameTime/               # Day-night cycles and shifts
│   │   ├── Menu/                   # UI and menu systems
│   │   ├── Purchasables/           # Item and trading systems
│   │   ├── Tags/                   # Gameplay tag definitions
│   │   └── Public/                 # Public headers (subsystems, data assets)
│   ├── MentorshipProjekt.Target.cs  # Build target configuration
│   └── MentorshipProjektEditor.Target.cs
├── Content/                         # Game assets
│   ├── Data/                        # Data assets (recipes, skills, customer profiles)
│   ├── Areas/                       # Location blueprints (tavern, kitchen, etc.)
│   ├── NPCs/                        # Character blueprints and assets
│   ├── Player/                      # Player character and UI
│   ├── UI/                          # User interface widgets
│   ├── Interactables/              # Interactive object blueprints
│   ├── AdvancedVillagePack/        # Third-party village assets
│   ├── Fantastic_Village_Pack/     # Additional village pack assets
│   ├── Medieval_House/              # Medieval architecture assets
│   └── MainLevel.umap              # Primary gameplay level
├── Config/                          # Engine configuration
├── Binaries/                        # Compiled executables
└── MentorshipProjekt.uproject      # Project configuration
```

## Gameplay Overview

### Core Loop

1. **Planning**: Assign family members to work shifts and locations
2. **Execution**: Navigate the village in real-time, manage customer interactions
3. **Progression**: Earn gold and reputation, develop family skills
4. **Economy**: Balance income and expenses to sustain your family

### Key Systems

**Family Economy Subsystem** (`FamilyEconomySubsystem`)
- Tracks family gold reserves and expenses
- Manages reputation changes and milestones
- Broadcasts economy state changes to UI

**Skill Progression** (`SkillProgress`, `SkillDataAsset`)
- Gameplay tag-based skill identification
- Experience tracking and level progression
- Skill data assets define progression curves

**NPC Management** (`NPCManagerSubsystem`, `NPCCharacter`)
- Spawns and manages NPC behavior
- Handles customer interactions and transactions
- Family member attribute and skill tracking

**Interaction System** (`InteractableBase`, `InteractionWidget`)
- Context-sensitive interaction prompts
- Menu-based interaction flows
- Widget-based UI for player selections

## Architecture

### Core Subsystems

- **FamilyEconomySubsystem**: Manages family finances and reputation
- **GameTimeSubsystem**: Handles day-night cycles and shift scheduling
- **NPCManagerSubsystem**: Controls NPC spawning and behavior
- **MyAssetManager**: Custom asset management and loading

### Input System

The project uses the **Enhanced Input System**:
- Configurable input actions and mappings
- Separate context handling for different gameplay modes
- Support for multiple input devices

### Networking & Scalability

- Single-player focused gameplay
- Optimized for Windows (DirectX 12)
- Ray-tracing enabled with virtual shadow mapping
- Substrate-based material system for advanced rendering

## Support & Documentation

### Getting Help

- **Code Documentation**: Review [Source](Source/) folder headers and comments
- **Blueprint Reference**: Explore Content assets and their Blueprint implementations
- **Configuration**: Check [Config/](Config/) for engine and game settings
- **Issue Tracking**: Open issues on GitHub for bugs and feature requests

### Project Links

- **Unreal Engine 5.7 Documentation**: https://docs.unrealengine.com/5.7/
- **Enhanced Input System Guide**: https://docs.unrealengine.com/5.7/en-US/enhanced-input-user-guide-in-unreal-engine/
- **Blueprint Visual Scripting**: https://docs.unrealengine.com/5.7/en-US/BlueprintAPI/

## Contributing

We welcome contributions from developers interested in:
- Expanding gameplay systems
- Optimizing performance
- Adding new features and content
- Improving code quality and architecture

### Contribution Guidelines

1. **Fork the repository** and create a feature branch
2. **Follow C++ and Blueprint conventions** consistent with the codebase
3. **Test your changes** in the editor before submitting
4. **Submit pull requests** with clear descriptions of changes

For detailed contribution instructions, see [CONTRIBUTING.md](CONTRIBUTING.md)

### Development Workflow

```bash
# Create feature branch
git checkout -b feature/your-feature-name

# Make changes and commit
git commit -m "feat: add your feature description"

# Push and create pull request
git push origin feature/your-feature-name
```

## Team

**MentorshipProjekt** is developed as part of the **Ubisoft Mentorship Program**, combining industry experience with emerging talent to create engaging interactive entertainment.

---

**Project Status**: Active Development  
**Latest Version**: 1.0  
**Engine**: Unreal Engine 5.7  
**License**: See LICENSE file

Built with ❤️ for simulation game enthusiasts and aspiring game developers.
