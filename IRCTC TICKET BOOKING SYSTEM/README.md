# RDBMS-ER-DIAGRAM---ASSIGNMENT-5
IRCTC  Train Ticket Booking System - ER Diagram

This ER Diagram represents a simplified model of the **IRCTC online railway booking system** with 5 main entities:

* **Passenger**
* **Train**
* **Ticket**
* **Payment**
* **Station**

---

## Entities and Attributes

1. **Passenger**

   * Attributes: Passenger\_ID (PK), Name, Age, Gender, Phone\_Number

2. **Train**

   * Attributes: Train\_No (PK), Train\_Name, Source, Destination

3. **Station**

   * Attributes: Station\_Code (PK), Station\_Name, Location

4. **Payment**

   * Attributes: Payment\_ID (PK), Mode, Amount, Status

5. **Ticket** *(Weak Entity)*

   * Attributes: Ticket\_ID (Partial Key), PNR\_No, Journey\_Date, Status (Confirmed / RAC / Waiting)

---

## 📌 Relationships

1. **Books Ticket (Passenger – Ticket)**

   * 1 Passenger → many Tickets (1\:M)
   * **Total participation from Ticket side** → Ticket must belong to a Passenger.

2. **Ticket Confirmation in Train (Ticket – Train)**

   * Many Tickets → 1 Train (M:1)
   * **Total participation from Ticket side** → Ticket must be linked to a Train.

3. **Payment Transaction (Ticket – Payment)**

   * 1 Ticket → 1 Payment (1:1)
   * **Total participation on both sides** → A valid ticket always has a payment, and a payment exists only for a ticket.

4. **Arrives at / Leaves from (Train – Station)**

   * Many Trains ↔ Many Stations (M\:N)
   * Usually **total participation on both sides** (each train must stop at stations, each station belongs to at least one train).

---


