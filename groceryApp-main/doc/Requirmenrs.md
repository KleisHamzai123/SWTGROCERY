# SWTgrocery Application - Requirements

## Functional Requirements

### 1. Multi-language Support
- **Requirement:** The application shall support multiple languages, allowing users to use the interface in their preferred language.  
  - **Type:** Assumption

### 2. Grocery Catalog Management
- **Item Search:**
  - Users shall be able to search the grocery catalog by item name.
  - **Type:** Interaction

- **Item Maintenance:**
  - Users shall be able to maintain grocery items in the catalog, adding or deleting one item at a time.
  - **Type:** Maintenance

- **Catalog Content:**
  - Grocery catalog shall contain an item name, item units, and item category.
  - **Type:** Data Management

- **Filtering:**
  - All items in the grocery catalog shall be filterable by category.
  - **Type:** Data Management

- **Performance:**
  - The grocery catalog should support at least 1000 concurrent items without significant degradation in performance.
  - **Type:** Scalability

- **Environmental:**
  - The grocery catalog shall prioritize sourcing products from local farmers, promoting ethical agricultural practices.
  - **Type:** Environmental

### 3. Grocery List Management
- **List Creation and Maintenance:**
  - The system shall allow users to create and manage multiple shopping lists within the grocery list.
  - **Type:** Maintenance

- **Item Inclusion:**
  - Users shall be able to add and delete items from their grocery lists.
  - **Type:** Processing Data

- **Tick Off Items:**
  - Users shall be able to tick off items in the grocery list for inclusion in the past purchase list.
  - **Type:** Interaction

- **Quantity Management:**
  - The system shall allow users to specify and change each item’s desired quantity.
  - **Type:** Processing Data, Interaction

- **Grouping and Ordering:**
  - All items on the grocery list shall be groupable by category and ordered such that already purchased items appear at the bottom while items yet to be bought are at the top.
  - **Type:** Usability, Data Management

- **Multiple Units:**
  - A grocery list shall contain the same items with different unit names.
  - **Type:** Consistency

- **Initial State:**
  - Grocery lists shall be empty at the first usage and should support at least 200 concurrent items without significant degradation in performance.
  - **Type:** Consistency, Scalability

- **Minimum Elements:**
  - A shopping grocery list shall always contain at least one element in it.
  - **Type:** Invariants

### 4. Past Purchase List Management
- **Search Capability:**
  - Users shall be able to search the past purchase list by item name and date range.
  - **Type:** Interaction, Processing Data

- **Comprehensive Browsing:**
  - Users shall have the ability to browse a comprehensive list of all past purchases, including item name, unit, quantity, date, and category.
  - **Type:** Data Management

- **Sorting:**
  - All items on the past purchase list shall be sortable alphabetically by category.
  - **Type:** Data Management

- **Import Facility:**
  - The SWTgrocery system shall offer an import facility to replace the past purchase list with new ones, ensuring the process is completed within 2 seconds.
  - **Type:** Data Integration, Performance

- **Extending Catalog:**
  - The system shall extend the grocery catalog with new items from the past purchase list.
  - **Type:** Processing Data

- **Initial State:**
  - The past purchase list shall be empty at the first usage and should support at least 1000 concurrent items without significant degradation in performance.
  - **Type:** Consistency, Scalability

### 5. Suggestions and Recommendations
- **Suggestions System:**
  - The system shall offer suggestions about grocery items and their quantities based on user behavior, tracked via the past purchase list, whenever the application is started, the grocery list changes, or past purchases are imported.
  - **Type:** Transformation

- **User Preferences:**
  - Users shall set preferences regarding the number of suggestions they want to receive.
  - **Type:** Usability

- **Acceptance and Rejection:**
  - Users shall be able to accept or decline suggestions. Upon rejection, the system shall adapt the underlying patterns used for generating suggestions.
  - **Type:** Interaction, Consistency

### 6. System Management
- **Error Handling:**
  - The application shall provide clear and user-friendly error messages to guide users in case of input errors or system failures.
  - **Type:** Interoperability

- **Scheduled Maintenance:**
  - Users should be notified in advance about scheduled maintenance activities, detailing the expected duration and services affected.
  - **Type:** Maintenance

### 7. Data Management
- **Storage:**
  - The system should store all lists in a MariaDB database.
  - **Type:** Data Management
