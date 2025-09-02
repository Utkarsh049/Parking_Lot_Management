# 🚗 Parking Lot Management System  

A **C++ console-based Parking Lot Management System** that manages vehicle parking, retrieval, billing, and a VIP membership system. It uses **file handling** to store and manage vehicle details and VIP user IDs.  

---

## 📌 Features  

- **Park a Vehicle**  
  - Supports 2-wheelers & 4-wheelers.  
  - Supports Electric & Petrol vehicles.  
  - Auto-assigns floor numbers based on vehicle type.  
  - Stores details (vehicle type, floor, number plate, entry time) in a CSV database.  

- **Retrieve a Vehicle**  
  - Fetch vehicle data using the number plate.  
  - Calculates parking fee based on duration.  
  - Applies VIP discounts (Silver/Gold/Platinum).  
  - Removes the vehicle from the database and frees the slot.  

- **VIP Membership System**  
  - Allows checking if a customer is a VIP using a UID stored in `viplist.txt`.  
  - Supports Silver (10%), Gold (15%), and Platinum (20%) discounts.  

- **Admin Functions**  
  - **View Database** (password: `galahad`).  
  - **Erase Database** (password: `lancelot`).  
  - **Update VIP UID List** (password: `merlin`).  

- **Slot Management**  
  - Tracks available slots separately for:  
    - 2-Wheeler Electric  
    - 2-Wheeler Petrol  
    - 4-Wheeler Electric  
    - 4-Wheeler Petrol  

---

## ⚙️ How It Works  

1. **User enters choice** from the main menu:  
   - Park Vehicle  
   - Retrieve Vehicle  
   - View Database (Admin)  
   - Erase Database (Admin)  
   - Update VIP UID List (Admin)  
   - Exit  

2. **When parking a vehicle:**  
   - Validates wheel type (2/4) and fuel type (Electric/Petrol).  
   - Validates number plate format: `LLDDLLDDDD` (e.g., `TN21DF9967`).  
   - Stores vehicle details in `database.csv`.  
   - Decreases slot count for the respective vehicle type.  

3. **When retrieving a vehicle:**  
   - Asks for number plate.  
   - Checks VIP status (optional).  
   - Calculates bill (with discounts if VIP).  
   - Removes vehicle record from `database.csv`.  
   - Frees slot in parking lot.  

---

