# Gaza Before and After Effect Analysis

## Project Overview

This project analyzes satellite imagery of Gaza before, during, and after the 2023 conflict that began on October 7, 2023. The analysis uses Sentinel-2 satellite imagery to detect and quantify visible changes to the landscape and infrastructure across different regions of Gaza.

**🗓️ Note**: This analysis is limited to data from the year **2023** only.

## Dataset

The dataset consists of:

* Satellite images from Sentinel Hub's Sentinel-2 L2A collection
* Images organized by geographic sections (`section_1`, `section_2`, etc.)
* Temporal coverage spanning **before, during, and after** the conflict
* Metadata for each image including coordinates, date range, and section information

## Methodology

The analysis follows these steps:

1. **Data Preprocessing**:

   * Filtering out invalid images (too dark or with white spots)
   * Organizing images by section and date
   * Converting images to grayscale for better change detection

2. **Change Detection**:

   * Comparing consecutive images from pre-war period to establish baseline
   * Analyzing changes at war start by comparing last pre-war image with first war-time image
   * Measuring post-war damage by comparing post-war images with the last pre-war image

3. **Quantification**:

   * Calculating change scores by measuring pixel-level differences between images
   * Categorizing analysis by war phase (`pre-war`, `war-start`, `post-war`)
   * Aggregating data to identify most affected regions

4. **Visualization**:

   * Box plots showing change intensity across different war phases
   * Interactive map displaying war damage intensity across geographic sections
   * Color-coded visualization of affected areas
   * City name labels added to maps for context

## Key Findings

* Distinct patterns of visual change between pre-war, war-start, and post-war periods
* Identification of areas with highest damage intensity
* Temporal analysis of change progression throughout the conflict

## Technical Implementation

* **Programming Language**: Python
* **Key Libraries**:

  * NumPy and Pandas for data handling
  * PIL (Python Imaging Library) for image processing
  * Matplotlib and Seaborn for statistical visualization
  * Folium and Branca for interactive mapping
  * JSON for metadata processing

## Usage

1. Install required dependencies:

   ```bash
   pip install numpy pandas matplotlib seaborn pillow folium
   ```
2. Run the Jupyter notebook to reproduce the analysis
3. Explore the visual outputs and interactive map

## Limitations

* Analysis is based purely on visual changes detected in satellite imagery
* Cloud cover or atmospheric conditions may affect image quality
* Resolution limitations of publicly available satellite imagery

## Data Source

The satellite imagery is from the **Sentinel Hub's Sentinel-2 L2A collection**, accessed via the Kaggle dataset:
📦 [Gaza Before and After](https://www.kaggle.com/datasets/abdoomoh/gaza-before-and-after-2)
🧑‍💻 Provided by: **@abdoomoh** on Kaggle

## Presentation

🎥 [View the project presentation on Canva](https://www.canva.com/design/DAGnOyh1wPY/yIt4DiJietofMWdSAdyBhQ/edit?utm_content=DAGnOyh1wPY&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

## Acknowledgment

Special thanks to **@abdoomoh** on Kaggle for sharing the Gaza satellite imagery dataset used in this analysis.
This project is dedicated to highlighting the real-world consequences of war using transparent, data-driven methods.

## License

MIT License
