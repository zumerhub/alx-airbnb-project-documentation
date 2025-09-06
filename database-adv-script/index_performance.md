# Index Optimization – ALX Airbnb Database Project

This task demonstrates how **indexes** can be used to improve query performance in the Airbnb database schema.

---

## 1. Indexes Created
The following indexes were added (see `database_index.sql`):

- **User Table**
  - `idx_user_email` → optimizes login and lookups by email.
- **Booking Table**
  - `idx_booking_user_id` → speeds up joins with the `User` table.
  - `idx_booking_property_id` → speeds up joins with the `Property` table.
  - `idx_booking_user_property` → improves performance when filtering by both user and property.
  - `idx_booking_date` → useful for date range searches.
- **Property Table**
  - `idx_property_location` → optimizes queries filtering/searching by location.

---

## 2. Measuring Performance

### Example Query 1 (Before Index)
```sql
EXPLAIN
SELECT *
FROM Booking
WHERE user_id = 'some-uuid';
