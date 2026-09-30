# 2D Mobile Game Engine & Simulation (Android/Java)

A multi-threaded 2D arcade simulation built natively for Android using pure Java. Rather than relying on a heavy commercial framework, this project features a lightweight, custom-engineered 2D math and physics architecture tailored for real-time entity updates, precise collision detection, and procedural animation.

## Key Technical Features
* **Custom 2D Math & Collision Engine:** Implements native vector math (`Vec2D`), spatial bounds (`Circle`, `FRect`), line segments (`LineSeg`), and generic polygons (`Poly`). Uses explicit projection methodologies to resolve geometric intersections.
* **Procedural Component Animation:** Uses linear interpolation (LERP) mechanics to dynamically animate sprite components (e.g., multi-triangle jaw structures) relative to collision states.
* **Decoupled Game Loop Architecture:** Features a dedicated `GameEngineThread` to isolate rendering steps, physics loops, and user input capture from the main UI thread.
* **Particle Systems:** Includes a lightweight vector-based particle system (`Emitter.java`) handling velocity vectors and life-cycle calculations for physics-driven visual effects (`BloodSpatter`).

## Core Directory Structure
```
── app/src/main/java/com/example/me/sharks/
├── math/                  # Low-level physics & linear algebra framework
│   ├── Vec2D.java         # Native 2D vector mathematics
│   ├── Poly.java          # Custom polygon tracking and mesh primitives
│   └── CollisionFunc.java # Geometric projection & collision resolution
├── GameEngineThread.java  # Isolated loop handling timing and tick updates
├── Emitter.java           # Particle generation system for visual dynamics
├── Shark.java             # Entity with procedural LERP component manipulation
└── Fish.java              # Standard autonomous sprite agent behavior
```
