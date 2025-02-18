# Route Optimization for Store Locations in London

A route optimization visualization project for store locations in London using Python. The project solves and visualizes a Traveling Salesman Problem (TSP) for a driver starting from a designated store location. It displays the optimal route and animations on an interactive map.

## Features

- **Store Location Data**: Filters store data for the city of London.
- **Map Visualization**: Visualizes store locations on a map using `folium`.
- **Graph Creation**: Creates a street network graph with edge speeds and travel times using `osmnx`.
- **Shortest Path Calculation**: Calculates the shortest path between store locations using `NetworkX`.
- **Route Optimization**: Uses Google’s OR-Tools to solve the TSP and find an optimized route.
- **Route Animation**: Animates the route on an interactive map using `plotly.express`.

## Technologies Used

- **Pandas**: For data manipulation and filtering.
- **Numpy**: For numerical calculations.
- **Matplotlib & Seaborn**: For data visualization and heatmaps.
- **Folium**: For interactive map visualization.
- **Plotly Express**: For route animation visualization.
- **OSMnx**: For creating and analyzing street networks.
- **NetworkX**: For graph-based shortest path calculations.
- **Google OR-Tools**: For route optimization and solving the TSP.

## Data Preparation

1. **Store Data Filtering**:  
   The data is filtered to include only store locations in London and is reset with new indices.  

2. **Marker Assignment**:  
   - The starting point is marked in **red**.  
   - All other locations are marked in **black**.  
   
3. **Map Display**:  
   The filtered store locations are displayed on a map using `folium`.

## Route Optimization Process

1. **Graph Creation**:  
   A street network graph is created using `OSMnx`, centered around the starting location. Edge speeds and travel times are calculated for the network.

2. **Distance Matrix**:  
   A distance matrix is computed for all store location pairs using `NetworkX` to calculate the shortest paths.

3. **TSP Solving**:  
   Google OR-Tools is used to solve the TSP, generating the optimal route for the driver.

## Route Animation

1. **Animation Data**:  
   The path between nodes is plotted, and route animations are generated using `plotly.express`.

2. **Map Markers**:  
   - **Start Point**: Red marker.
   - **End Point**: Green marker.
   - **Store Locations**: Black markers.

3. **Route Path**:  
   The optimized route is displayed on the map in **blue**.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/tryAhmad/RouteOptimization-StarBucks/.git
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn folium plotly osmnx networkx ortools
   ```

3. Run the script:
   ```bash
   python route_optimization.py
   ```

## Usage

1. **Data File**: Ensure the `data_stores.csv` file is in the same directory as the script.
2. **Starting Location**: The starting store location is automatically marked and used for optimization.
3. **Route Visualization**: View the optimal route and animation on an interactive map.

## Notes

- If any errors occur, ensure the road network is complete and the distance matrix is correctly computed.
- Browser security warnings may appear for map visualization links—use a trusted hosting service if sharing publicly.
