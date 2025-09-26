# Task: High and highest voltage substations & generators analysis  for Brandenburg & Sachsen

## Objective
Analyze geospatial data to identify high and highest voltage substations in Germany, associate nearby generators with them, and fill the dataset with state-level information.


## Task Instructions

### 1. Extract Generators
- Obtain all objects tagged as generators or plants from OpenStreetMap (OSM) or another reliable source. (e.g. tags in OSM: `power=generator` or `power=plant`)
- Keep relevant attributes such as generator type or energy source.

### 2. Extract Substations
- Obtain all objects tagged as `power=substation`.
- Filter substations with **voltage ≥ 110 kV**.

### 3. Assign Bundesland Information
- Obtain a shapefile or geospatial dataset of German Bundesländer (states).
- Assign each substation to its corresponding Bundesland via spatial join or intersection.

### 4. Associate Generators to Substations
- For each generator, find the **nearest substation** using a spatial nearest-neighbor approach.

### 5. Aggregate & Summarize
- For each substation, calculate:
  - Number of nearby generators.
  - Breakdown of generators by type.
  - Generator capacities if available.


## Deliverables
1. **Repository** implementing all steps above and with folder "output" that contains the final geodataframes.


## Notes
- Data may be incomplete; focus on methodology.
- You may use any suitable geospatial libraries or tools.
- Visualize sample substations 
