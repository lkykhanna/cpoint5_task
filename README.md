# cpoint5_task
Task code of cpoint5

This code performs a comprehensive data analysis and visualization task based on two inventory-related datasets.

1. **Loading the Data**:
   - The code begins by importing necessary libraries (`pandas` for data manipulation and `matplotlib.pyplot` for plotting).
   - It then loads two Excel files: one containing current inventory data (`Inventory Dataset.xlsx`) and the other containing information about new inventory arrivals (`New Inventory.xlsx`).

2. **Data Preprocessing**:
   - The dates in both datasets are converted to pandas' `datetime` format for easier manipulation.
   - The code identifies the starting date for analysis (the earliest date in the current inventory data) and sets an end date (August 26, 2023).

3. **Creating Future Inventory Levels Table**:
   - A new DataFrame is initialized to track inventory levels for each item across a range of future dates.
   - The table is populated with initial inventory levels from the current inventory data.
   - The inventory levels are then updated for each day in the specified date range, accounting for new inventory arrivals as indicated in the new inventory dataset.
   - This step addresses the problem of predicting future inventory levels based on current stock and known incoming stock.

4. **Data Transformation**:
   - The future inventory levels DataFrame is transposed to align with the format of the example provided, where dates are rows and items are columns.

5. **Generating a Monthly Inventory Bar Chart**:
   - The index of the DataFrame is converted back to a `DatetimeIndex` to facilitate resampling (grouping data based on time intervals).
   - The total inventory level is calculated at the end of each month by summing up all item inventories.
   - A bar chart is generated to visually represent these total monthly inventory levels.
   - This visualization addresses the problem of understanding how total inventory levels are expected to change over time on a monthly basis.

The final output includes a detailed table of projected inventory levels on specific future dates for each item and a bar chart summarizing total inventory levels at the end of each month.
