# generate-lead-alignments
Python code to generate lead alignments of the institutes into a text format which we can link with the signup form

## Overview

This script fetches alignment data for a specified entity from a remote JSON API and writes the alignment information to a file in a specific format. The data is retrieved from the URL `https://gis-api.aiesec.org/v2/lists/mcs_alignments.json?mc_id[]=495&mc_id[]=537` and filtered based on the provided entity ID (`EY_ID`). The filtered data is then written to a file named `alignments.txt`.

## Prerequisites

- Python 3.x
- Internet connection (to fetch data from the API)

## Setup

1. Ensure you have Python 3.x installed on your machine. You can download it from [python.org](https://www.python.org/).

2. Install necessary libraries if they are not already installed. The script uses the following Python libraries:
   - `urllib.request` (comes with the standard library)
   - `json` (comes with the standard library)

3. Replace the placeholder `ENTITY CODE HERE` with the actual entity code. For example:
   ```python
   EY_ID = 1623

##Running the Script

1. Save the script to a file, e.g., fetch_alignments.py.


2. Open a terminal or command prompt and navigate to the directory where the script is saved.

3.Run the script using Python:

 ```python
   python fetch_alignments.py
```
4. If the script runs successfully, it will create a file named alignments.txt in the same directory as the script.

## Script Explanation
- The script starts by importing necessary libraries.
- The EY_ID variable should be set to the entity ID for which you want to fetch alignments.
- The URL https://gis-api.aiesec.org/v2/lists/mcs_alignments.json?mc_id[]=495&mc_id[]=537 is used to fetch JSON data.
- The data is then parsed into a JSON object.
- The script iterates through the entities in the JSON object and processes the one that matches the EY_ID.
- For the matching entity, it writes the alignment data to a file named alignments.txt in the specified format.

Example Output
The alignments.txt file will contain lines like:

```php
<option data-id="12345" value="67890">Alignment Name</option>
<option data-id="54321" value="09876">Another Alignment</option>
```





```python
