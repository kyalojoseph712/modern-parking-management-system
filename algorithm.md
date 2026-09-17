# Algorithms

## A. Initialization
1. Set the total number of parking slots.
2. Set the number of available slots equal to total slots.
3. Create parking-slot records.
4. Create active-vehicle and transaction records.
5. Start the system.

## B. Vehicle Entry Algorithm
1. Input vehicle registration number.
2. Check whether the registration is already active.
3. If already parked, reject the entry.
4. Check whether available slots are greater than zero.
5. If no slots are available, display `PARKING FULL`.
6. Find the first available slot.
7. Record the vehicle registration and entry time.
8. Mark the slot as occupied.
9. Decrease available slots by one.
10. Display the assigned slot and remaining availability.

## C. Vehicle Exit Algorithm
1. Input vehicle registration number.
2. Search the active-vehicle dictionary.
3. If the vehicle is not found, display an error.
4. Retrieve its parking slot and entry time.
5. Record the exit time.
6. Calculate the time difference.
7. Convert the duration into billable hours.
8. Calculate `amount = billable_hours × hourly_rate`.
9. Display the bill.
10. Record the completed transaction.
11. Mark the slot as available.
12. Increase available slots by one.
13. Remove the vehicle from active parking records.

## D. Billing Algorithm
Given duration in minutes:

`billable_hours = ceiling(duration_minutes / 60)`

Then:

`amount = billable_hours × hourly_rate`

Example:

- Duration = 170 minutes
- Billable hours = ceiling(170 / 60) = 3
- Rate = KSh 100/hour
- Amount = KSh 300

## E. High-Level Flow

START
→ Check availability
→ Vehicle arrives
→ Is a slot available?
→ No: Display FULL
→ Yes: Assign slot
→ Record vehicle and entry time
→ Vehicle exits
→ Find vehicle
→ Calculate duration
→ Calculate payment
→ Record payment
→ Free slot
→ Increment availability
→ END
