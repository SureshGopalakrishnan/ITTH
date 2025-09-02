# Python Assignments

This is a collection of Python assignments created as part of a course. The programs demonstrate fundamental Python concepts, including data types, conditional statements, loops, and data structures like dictionaries and lists.

---

### **1. Blood Sugar Level Categorization**

This program takes a person's blood sugar readings (Fasting or Post-Meal) and categorizes the result based on standard medical ranges.

**Functionality:**

* Accepts a blood sugar level reading and the timing of the test (Fasting or Post-Meal).
* Provides a category (Normal, Pre-Diabetic, Diabetic, or Hypoglycemia) based on the input values.
* Includes input validation to handle incorrect timing entries.

---

### **2. Simple Movie Ticket Reservation**

A basic console program for reserving movie tickets. This version uses fundamental Python concepts to manage ticket availability and booking.

**Functionality:**
* Displays a list of movies with their available tickets.
* Allows users to select a movie and request a number of tickets.
* Validates user input to ensure a movie number and a valid number of tickets are entered.
* Updates the number of available tickets after a successful booking.

**Note:** The code's comments suggest an improved approach using a dictionary to store movie data, which would make the program more scalable and maintainable.

---

### **3. Country Details Program**

This assignment includes two different methods for collecting and storing country data, demonstrating how to use dictionaries for data management.

#### **Method 1: Dictionary of Dictionaries**
This program creates a single dictionary where each country's name is the **key**. The **value** for each key is another dictionary containing the country's population, area, and capital.

**Functionality:**
* Prompts the user for the number of countries they want to enter.
* Collects the name, population, area, and capital for each country.
* Stores the data in a nested dictionary structure, preventing data from being overwritten.
* Includes robust input validation for all fields.
* Demonstrates how to iterate through the data using the `zip()` function, which pairs elements from multiple lists for structured printing.

#### **Method 2: Dictionary with Lists**
This program uses a single dictionary where each **key** represents a data category (`name`, `population`, `area`, `capital`) and the **value** is a list of all the entries for that category.

**Functionality:**
* Prompts the user for the number of countries they want to enter.
* Collects data for multiple countries.
* Appends the collected data for each country to the appropriate list.
* Includes robust input validation for all fields.
* Demonstrates how to iterate through the data using the `zip()` function, which pairs elements from multiple lists for structured printing.
