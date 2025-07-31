# RTS Camera System - Unreal Engine 5

A focused development project for building a robust camera system for real-time strategy games in Unreal Engine 5. This repository serves as a learning platform and progress tracker for implementing advanced camera controls and movement systems.

##  Project Focus

This project is specifically designed to explore and implement camera systems for RTS games, rather than building a complete game prototype. The focus is on:

- **Camera Movement & Controls**: Smooth, responsive camera navigation
- **Zoom Functionality**: Dynamic zoom in/out with smooth transitions
- **Input System Integration**: Modern UE5 Enhanced Input System implementation
- **Performance Optimization**: Efficient camera updates and smooth 60+ FPS performance
- **Scalable Architecture**: Building a foundation for future RTS features

##  Current Features

### Camera System
- **Smooth Movement**: Camera follows mouse at screen edges with interpolation
- **Zoom In/Out**: Dynamic zoom functionality with smooth transitions using curve assets
- **Zoom Reset**: Quick reset to default zoom level (Ctrl + key binding)
- **Boundary Constraints**: Prevents camera from going out of playable bounds

### Input System
- **Enhanced Input Actions**:
  - `IA_ZoomIn` - Digital Bool for zooming in
  - `IA_ZoomOut` - Digital Bool for zooming out
  - `IA_ZoomReset` - Digital Bool for resetting zoom (chorded with LeftCtrlModifier)
  - `LeftCtrlModifier` - Digital Bool modifier for chorded actions
- **Input Mapping**: All actions mapped through `IMC_CameraMove` context

### Technical Implementation
- **Blueprint-C++ Integration**: Core logic in C++, tweaking in Blueprints
- **Curve-Based Zoom**: Float curve asset for smooth zoom transitions (300-1350 arm length range)
- **Component Architecture**: Modular design with separate camera and movement components

##  Architecture

### Core Components
- **BP_TopDownCamera**: Main camera blueprint with zoom logic
- **BP_PawnMovementComp**: Movement component handling zoom state management
- **BP_PlayerController**: Input handling and function mapping

### Key Functions
- `SetArmLength(float ZoomAmount)` - Applies zoom using curve evaluation
- `ZoomIn()` / `ZoomOut()` - Increment/decrement zoom with Lerp transitions
- `ResetZoom()` - Reset to midpoint (0.5) of zoom curve
- `ZoomEvents()` - Centralized function for real-time camera updates

##  Controls

- **Mouse Wheel**: Zoom in/out
- **Ctrl + Reset Key**: Reset zoom to default level
- **Mouse at Screen Edges**: Camera movement (planned/implemented)

##  Development Progress

### Completed 
- Basic camera setup and movement
- Enhanced Input System integration
- Smooth zoom functionality with curve assets
- Zoom reset functionality
- Performance optimization for 60+ FPS

### In Progress 
- Camera panning system
- Boundary constraints refinement
- Camera rotation around focal points

### Planned 
- Zoom speed customization
- Dynamic zoom bounds based on map size
- Advanced camera behaviors (follow units, cinematic modes)
- Multiplayer camera synchronization

##  Technical Stack

- **Engine**: Unreal Engine 5
- **Language**: C++ with Blueprint integration
- **Input System**: Enhanced Input System
- **Rendering**: Nanite and Lumen (for future visual enhancements)

##  Learning Goals

This project serves as a learning platform for:
- UE5's C++ framework and conventions
- Blueprint-C++ integration patterns
- Game camera design principles
- Performance optimization in game engines
- Modern input system implementation
- Real-time strategy game mechanics

##  Development Log

Progress and implementation details are documented in my [Game Dev Log](https://zacstack.dev/blog), including:
- [Starting My OpenGL Learning Journey](https://your-portfolio-url.com/blog/opengl-learning-journey)
- [Developing an RTS Camera System in Unreal Engine 5](https://your-portfolio-url.com/blog/unreal-engine-rts-camera)
- [Implementing Smooth Camera Zoom in Unreal Engine 5](https://your-portfolio-url.com/blog/camera-zoom-implementation)

##  Future Vision

While this project focuses on camera systems, it's designed as the foundation for a larger RTS game development journey. Future phases may include:
- Unit selection and movement systems
- Basic AI for units
- Resource management
- Multiplayer foundation
- Full RTS gameplay mechanics

##  License

This project is for educational and portfolio purposes. Feel free to use concepts and implementations for your own learning.

---

*This is a focused development project - not a complete game, but a stepping stone in my journey to build robust RTS game systems.*

