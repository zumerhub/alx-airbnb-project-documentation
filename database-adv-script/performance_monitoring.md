# Database Performance Monitoring and Refinement

## Objective
To monitor the performance of frequently used queries, identify bottlenecks, and refine the database schema for efficiency.

---

## Step 1: Initial Query Analysis

### Query 1: Get all bookings in 2023
```sql
EXPLAIN SELECT booking_id, start_date, end_date
FROM Booking
WHERE start_date BETWEEN '2023-01-01' AND '2023-12-31';
