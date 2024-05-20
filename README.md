# README: Summarizing Statistical Data Exercise

## Overview
This exercise involves summarizing and visualizing statistical data from a representative sample of 200 consumers at a petrol filling station. The data details the number of litres of petrol purchased by customers. The tasks include creating a pie chart, histogram, and frequency polygon to represent the data visually.

## Data Provided
The data consists of the number of litres of petrol purchased and the corresponding number of customers.

| Number of litres of petrol purchased | Number of customers |
|-------------------------------------|---------------------|
| 0 and < 2                           | 15                  |
| 2 and < 4                           | 40                  |
| 4 and < 6                           | 65                  |
| 6 and < 8                           | 40                  |
| 8 and < 10                          | 30                  |
| 10 and < 12                         | 10                  |

## Visual Representations

### Pie Chart
The pie chart displays the proportion of customers within each range of petrol purchased. Each slice of the pie represents the percentage of the total number of customers who fall into each range.

### Histogram
The histogram shows the frequency distribution of petrol purchases. The x-axis represents the ranges of litres purchased, and the y-axis represents the number of customers.

### Frequency Polygon
The frequency polygon is a line graph that connects the midpoints of each range of petrol purchased. It shows the number of customers for each interval, providing a visual understanding of the data distribution.

## Instructions for Visualization

### Requirements
- Python
- matplotlib library

### Steps to Create Visualizations

1. **Install matplotlib** (if not already installed):
   ```sh
   pip install matplotlib
   ```

2. **Run the provided Python script** to generate the visualizations:
   ```python
   import matplotlib.pyplot as plt

   # Data
   intervals = ['0-2', '2-4', '4-6', '6-8', '8-10', '10-12']
   customers = [15, 40, 65, 40, 30, 10]
   total_customers = 200

   # Pie Chart
   percentages = [x / total_customers * 100 for x in customers]
   plt.figure(figsize=(8, 6))
   plt.pie(percentages, labels=intervals, autopct='%1.1f%%', startangle=140)
   plt.title('Pie Chart of Petrol Purchased')
   plt.show()

   # Histogram
   plt.figure(figsize=(8, 6))
   plt.bar(intervals, customers, width=0.8, color='skyblue')
   plt.xlabel('Number of Litres of Petrol Purchased')
   plt.ylabel('Number of Customers')
   plt.title('Histogram of Petrol Purchased')
   plt.show()

   # Frequency Polygon
   midpoints = [1, 3, 5, 7, 9, 11]
   plt.figure(figsize=(8, 6))
   plt.plot(midpoints, customers, marker='o', linestyle='-', color='blue')
   plt.xlabel('Midpoint of Number of Litres of Petrol Purchased')
   plt.ylabel('Number of Customers')
   plt.title('Frequency Polygon of Petrol Purchased')
   plt.grid(True)
   plt.show()
   ```

3. **Interpret the Charts**:
   - **Pie Chart**: Observe the proportion of customers for each interval of petrol purchased.
   - **Histogram**: Examine the frequency distribution of customers across the different intervals.
   - **Frequency Polygon**: Analyze the trend and distribution of the data through connected points.

## Conclusion
This exercise helps in understanding various methods of summarizing statistical data and visualizing it through different types of charts. By following the steps above, you can effectively represent and analyze the given data set.