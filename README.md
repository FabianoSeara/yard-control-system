# Container Yard Control System

Command-line interface (CLI) system to manage container movement and storage in a port yard: registration, search, status updates, movement between positions, and occupancy statistics.

This project was born from my practical experience in port terminals, where I have managed yard controls manually in spreadsheets. The goal here was to recreate this process as a real application, applying programming logic and databases.

## Features

- **Container registration:** number, type, client/vessel, and yard position.
- **Listing:** with filter by status.
- **Search:** by container number.
- **Status update:** (Waiting → Stored → In Transit → Loaded/Departed).
- **Movement:** between block/row/tier.
- **Statistics:** total containers, distribution by status, and occupancy per block.

## Technologies

- Python 3 (no external dependencies)
- SQLite (local database via the standard library `sqlite3` module)

## Project Structure

```text
container-yard-system/
├── main.py         # Terminal menu (user interaction)
├── operacoes.py    # Business logic (register, search, update...)
├── database.py     # SQLite connection and table creation
└── README.md

## How to Run

No dependencies to install - just Python 3.

git clone https://github.com/FabianoSeara/container-yard-system.git
cd container-yard-system
python main.py

The database (patio.db) is created automatically on the first run.

## Example Usage

==================================================
   CONTAINER YARD CONTROL SYSTEM
==================================================
1. Register new container
2. List containers
3. Search container by number
4. Update container status
5. Move container (block/row/tier)
6. Yard statistics
0. Exit
==================================================

## Next Steps

- [ ] Export reports to CVS
- [ ] Add movement history per container
- [ ] IWeb interface (Flask) as a project evolution

---

Project deloped by [Fabiano Seára](https://github.com/FabianoSeara) part of my portfólio for transitioning to a software development career.
