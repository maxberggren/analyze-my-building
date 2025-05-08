# Interactive Building Performance Analyzer

This repository contains the code for the Interactive Building Performance Analyzer, a web-based tool designed to analyze time-series data from building systems. The primary goal of this tool is to provide a fair and transparent method for determining the real impact of upgrades or control strategy changes made to building systems.

## Motivation

Analyzing building performance data, especially when comparing different time periods, can be challenging due to confounding factors, primarily weather variations. For example, an investment in energy-efficient windows might not show immediate savings if the following year is significantly colder. This tool aims to address this by normalizing data against outdoor temperature and other relevant factors, allowing for more accurate comparisons and revealing the true impact of interventions.

This tool is currently used by Myrspoven AB in Stockholm for impact analytics on building energy performance. It is open source to promote transparency and collaborative improvement in building analytics.

## How it Works

The tool guides users through a four-step process:

1.  **Upload Data:** Users can upload CSV or Excel files containing their building's operational data (timestamps, sensor readings, control signals). The tool also provides an option to load example data.
2.  **Map Columns:** Users specify which columns in their data correspond to key data points like timestamps, outdoor temperature, the primary control signal to be analyzed, and other relevant sensor signals.
3.  **Configure Analysis:** Users set parameters for the analysis, including:
    *   Defining "ON" and "OFF" states for the primary control signal (either threshold-based or by date ranges).
    *   Specifying date ranges for "ON" and "OFF" periods.
    *   Filtering data by outdoor temperature ranges.
    *   Filtering data by specific hours of the day.
4.  **View Results:** The tool presents interactive charts and detailed textual explanations, quantifying the impact of the control strategy under various conditions. Key analyses include:
    *   **Initial Data Overview & ON/OFF Distribution:** Visualizes data after filtering and control state assignment.
    *   **Outdoor Temperature Normalized Analysis:** Compares selected signals during "ON" vs. "OFF" control states, normalized by outdoor temperature. This analysis can be viewed for all days, weekdays, weekends, or individual days of the week. It includes metrics like simple average difference, temperature-occurrence-weighted difference, and optional corrections for uptime and affinity laws (for fan/pump pressure signals).

## Key Features

*   **Local Data Processing:** All analysis is performed locally in the user's web browser. No data is uploaded to any server, ensuring user privacy.
*   **Pedagogical Approach:** Each step and analysis method is explained in detail to help users understand the methodology.
*   **Interactive Visualizations:** Utilizes Plotly.js for dynamic charts.
*   **Support for CSV and Excel:** Parses common data file formats.
*   **Open Source:** The tool is open source, and contributions are encouraged.

## Technologies Used

*   HTML, CSS, JavaScript
*   Plotly.js (for charting)
*   PapaParse (for CSV parsing)
*   SheetJS (xlsx.js) (for Excel parsing)

## Getting Started

1.  Clone this repository.
2.  Open the `index.html` file in a modern web browser.
3.  Follow the on-screen instructions to upload your data and perform the analysis.

## Contributing

Contributions, suggestions, and feedback are highly encouraged. Please feel free to open an issue or submit a pull request on the [GitHub repository](https://github.com) (Note: Replace with the actual GitHub repository link if available). 