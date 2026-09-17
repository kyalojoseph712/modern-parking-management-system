# Modern Parking Management System

## 1. Project Overview
A Python-based parking management system that allows users to know parking availability before entry, records vehicles and assigned parking slots, calculates parking duration and payment on exit, and makes the slot available again.

## 2. Objectives
- Display available parking slots.
- Register vehicles entering the parking area.
- Assign an available parking slot.
- Record entry time.
- Calculate parking duration on exit.
- Calculate parking fees.
- Record completed parking transactions.
- Release the occupied slot after exit.

## 3. Technologies
- Python 3
- SQLite (database design included)
- Git/GitHub

## 4. Main Features
1. Check parking availability.
2. Vehicle entry and automatic slot allocation.
3. Vehicle exit and automatic billing.
4. Parking history.
5. Database-ready design.

## 5. Charging Rule
The example rate is KSh 100 per billable hour. A partial hour is charged as a full hour.

Example: 2 hours 20 minutes = 3 billable hours = KSh 300.

## 6. Data Structures
- Dictionary/hash table: active vehicles, allowing fast lookup by registration number.
- Dictionary/list: parking slot status.
- List: completed parking history.
- Queue: can be added for vehicles waiting when the lot is full.

## 7. Database
The SQL design contains:
- parking_lot
- parking_slot
- vehicle
- parking_transaction
- payment

See `database.sql` and `docs/database_design.md`.

## 8. Algorithms
See `algorithm.md` for the entry, exit and billing algorithms.

## 9. How to Run
Install Python 3, then run:

```bash
python parking_system.py
```

No external Python packages are required.

## 10. Sample Operation
For a parking lot with 10 slots:
- Initially available = 10.
- Vehicle KDA123A enters and receives P01.
- Available becomes 9.
- When KDA123A exits, the system calculates the duration and fee.
- P01 becomes available and available slots increase to 10.

## 11. Future Improvements
- Automatic number plate recognition (ANPR).
- Web/mobile interface.
- M-Pesa payment integration.
- Electronic entry/exit barriers.
- Real-time display board.
- User accounts and administrator dashboard.
- Multiple parking-rate categories.

## 12. Author
Student project — Modern Parking Management System.
