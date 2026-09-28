# Mobile Shop CRUD Project

A simple command-line **CRUD** (Create, Read, Update, Delete) application built in Python to manage mobile phone inventory for a shop. Data is stored in memory using Python lists — no database or external libraries required.

## Features

1. **Add Mobile** – Add a new mobile record to the inventory
2. **Display All Mobiles** – View all mobile records in a formatted table
3. **Search Mobile** – Search for a mobile by its ID
4. **Update Mobile** – Update the details of an existing mobile
5. **Delete Mobile** – Remove a mobile record (with confirmation)
6. **Exit** – Close the application

## Data Structure

Each mobile record is stored as a list in the following format:

```python
[id, brand, model, price, quantity]
```

Example:

```python
[101, "Samsung", "Galaxy A55", 35000, 5]
```

All records are stored together in a single list:

```python
mobiles = [
    [101, "Samsung", "Galaxy A55", 35000, 5],
    [102, "Apple", "iPhone 15", 65000, 3],
    [103, "OnePlus", "Nord 4", 30000, 7]
]
```

## CRUD Mapping

| Operation | Function             | List Operation Used   |
|-----------|-----------------------|------------------------|
| Create    | `add_mobile()`         | `append()`             |
| Read      | `display_mobiles()`    | `for` loop             |
| Read/Search | `search_mobile()`   | `for` loop + condition |
| Update    | `update_mobile()`      | Modify list elements   |
| Delete    | `delete_mobile()`      | `remove()`             |

## Requirements

- Python **3.10+** (required for the `match-case` statement used in the menu)

No external packages are needed — the project only uses Python's built-in `input()` and `print()` functions.

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/mobile-shop-crud-python.git
   cd mobile-shop-crud-python
   ```

2. Run the script:
   ```bash
   python mobile_shop.py
   ```

3. Use the on-screen menu to add, view, search, update, or delete mobile records.

## Example Session

```
=============================================
 MOBILE SHOP MANAGEMENT
=============================================
1. Add Mobile
2. Display All Mobiles
3. Search Mobile
4. Update Mobile
5. Delete Mobile
6. Exit
=============================================
Enter your choice: 1

========== ADD MOBILE ==========
Enter Mobile ID: 101
Enter Brand: Samsung
Enter Model: Galaxy A55
Enter Price: 35000
Enter Quantity: 5
Mobile added successfully.
```

## Notes / Limitations

- Data is stored **in memory only** — all records are lost when the program exits (no file or database persistence).
- Mobile IDs must be unique; duplicate IDs are rejected on add.
- Intended as a beginner-friendly example of CRUD operations using core Python data structures (lists, loops, functions).

## Possible Future Improvements

- Persist data to a file (JSON/CSV) or database (SQLite) so records survive between runs
- Replace list-based records with dictionaries or a `Mobile` class for better readability
- Add input validation (e.g., non-numeric price/quantity handling)
- Add a search-by-brand or search-by-model feature

