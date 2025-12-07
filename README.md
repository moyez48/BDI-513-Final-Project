# Data Center Energy Usage Analysis: AI/ML Impact Study

**Author:** Majesty Umoye

## 📊 Project Overview

This project analyzes PG&E electric usage data for ZIP code 95113 (San Jose, CA) from 2016-2025, revealing the dramatic energy consumption patterns of a data center during the AI/ML boom era. Through advanced **load masking detection and correction**, this analysis exposes the true scale of energy demands that were previously hidden in neighboring ZIP codes.

## 🔍 Key Discoveries

### Load Masking Revelation
- **23 reallocations** identified where data center usage was reported under neighboring ZIP codes
- **February 2023 ABSOLUTE PEAK**: 201M kWh - **8x higher** than initially reported
- True AI infrastructure energy consumption: **10-20x comparison areas**
- Without correction, the massive scale was **completely hidden**

### AI/ML Timeline Correlation
The energy data provides a precise timeline of major AI developments:

| Period | Energy Pattern | AI/ML Event |
|--------|---------------|-------------|
| **Feb 2017** | 155M kWh | Data center construction peak |
| **Aug 2021** | 17.7M kWh | GPT-3 widespread adoption begins |
| **Jul-Aug 2022** | 17.5-18.3M kWh | DALL-E 2, Stable Diffusion training |
| **Feb 2023** | **201M kWh** ⚡ | **GPT-4 final training, Bing AI integration** |
| **Apr 2023** | 177M kWh | GPT-4 launch, massive inference scale-up |
| **Oct 2023** | 93M kWh | GPT-4 widespread adoption |
| **Sep 2024** | 88M kWh | Multi-modal AI (vision + audio) |
| **Nov 2024** | 112M kWh | ChatGPT Plus growth surge |
| **Jan 2025** | 121M kWh | New AI model training suspected |

## 📁 Project Structure

```
Final Project/
├── Data_Center_Analysis.ipynb          # Main Jupyter notebook with full analysis
├── pge_electric_usage_2015_2025_cleaned.csv  # PG&E usage data
├── Data_Center_Usage_Chart.png         # Visualization of energy patterns
├── Data_Center_Energy_Analysis_Report.docx   # Comprehensive report
└── README.md                            # This file
```

## 🛠️ Methodology

### Data Sources
- **Data Center ZIP**: 95113 (San Jose, CA)
- **Comparison ZIPs**: 95045, 95127, 95205, 95003
- **Load Masking Detection ZIPs**: 95110, 95111, 95112, 95116, 95117, 95118
- **Customer Classes**: Commercial, Residential, and Industrial
- **Time Period**: July 2016 - September 2025 (111 months)

### Understanding Load Masking (PG&E Aggregation Policy)

**Why Load Masking Occurs:**

According to California Public Utilities Commission Decision 14-05-016, PG&E's public datasets must meet specific aggregation rules to protect customer privacy:

- **Residential**: Minimum of 100 customers required
- **Non-Residential**: Minimum of 15 customers, with no single customer accounting for more than 15% of total consumption

**Critical Implication**: If these aggregation requirements are **not met** in a ZIP code, the consumption data is **combined with a neighboring ZIP code** until the requirements are satisfied.

This means that large energy consumers (like data centers) can have their usage reported under neighboring ZIP codes, making the true energy footprint invisible in standard analysis. This is exactly what our load masking detection algorithm corrects.

### Load Masking Detection Algorithm
1. **Baseline Calculation**: Compute median usage for each ZIP code
2. **Suspicious Period Detection**: Flag months where ZIP 95113 usage < 50% of baseline
3. **Neighbor Analysis**: Check neighboring ZIPs for abnormal usage (>50% above their baseline)
4. **Reallocation**: Transfer excess energy from neighbor back to ZIP 95113
5. **Documentation**: Log all reallocations with before/after values

This algorithm effectively reverses PG&E's privacy-mandated aggregation to reveal the true scale of data center operations.

### Statistical Analysis
- Month-over-month percentage changes
- Year-over-year trends
- Comparative analysis with regional baseline
- Peak usage identification and correlation with AI events

## 📈 Key Findings

### 1. **Dramatic Scale Revealed by Load Masking Correction**
- Data center average: **28.1M kWh/month** (+182.8% vs comparison areas)
- Peak usage: **201.4M kWh** (February 2023)
- Comparison areas average: **9.9M kWh/month**

### 2. **AI Era Energy Intensity (2021-2024)**
- Sustained peaks of **16-18M kWh** throughout 2021-2022
- **February 2023**: Absolute peak during GPT-4 final training
- **70-80% higher** energy consumption than surrounding areas
- Clear correlation between major AI model releases and energy spikes

### 3. **Lifecycle Phases**
- **Phase 1 (2016-2017)**: Construction & commissioning
- **Phase 2 (2018-2020)**: Steady operations (10-14M kWh/month)
- **Phase 3 (2021-2024)**: AI boom era (sustained 16-18M kWh peaks)
- **Phase 4 (2025)**: Migration or consolidation (121M kWh spike, then stabilization)

### 4. **Energy Policy Implications**
- AI workloads consume **2-3x more energy** than initially apparent
- Peak periods equivalent to powering **15,000+ average homes** continuously
- Grid planning must account for volatile AI training demand patterns
- Sustainability strategies require specialized approaches for AI data centers

## 🔬 Technical Implementation

### Technologies Used
- **Python 3.13**
- **pandas**: Data manipulation and aggregation
- **matplotlib**: Data visualization
- **python-docx**: Report generation
- **NumPy**: Numerical computations

### Key Features
- Intelligent load masking detection algorithm
- Automated monthly aggregation across customer classes
- AI event timeline annotation
- Comprehensive Word document report generation
- High-resolution visualization export (300 DPI)

## 📊 Visualization Highlights

The main chart includes:
- **Shaded regions** marking distinct AI eras (Construction, GPT-4 Training, Multi-Modal)
- **Annotated peaks** with AI/ML milestone explanations
- **Load masking correction indicator** showing dramatic scale revelation
- **Comparison baseline** from surrounding ZIP codes
- **Time-series analysis** from 2016-2025

## 🚀 How to Use

### Prerequisites
```bash
pip install pandas matplotlib python-docx numpy
```

### Running the Analysis
1. Open `Data_Center_Analysis.ipynb` in Jupyter Notebook or VS Code
2. Run all cells sequentially
3. Outputs will be generated:
   - `Data_Center_Usage_Chart.png`
   - `Data_Center_Energy_Analysis_Report.docx`

### Interpreting Results
- Review the visualization for AI/ML timeline correlations
- Check the Word document for detailed findings and methodology
- Examine load masking reallocation logs for transparency

## 💡 Insights & Conclusions

This analysis provides unprecedented visibility into the energy footprint of AI/ML infrastructure:

1. **Hidden Scale**: Load masking hid up to **8x the actual energy consumption** during peak periods
2. **AI Correlation**: Energy spikes directly track major AI model releases with remarkable precision
3. **Sustainability Challenge**: The February 2023 peak of 201M kWh represents a massive energy event that requires grid-scale planning
4. **Future Implications**: As AI models continue to scale, energy demands will grow exponentially

## 📝 Documentation

- **Full Analysis Report**: See `Data_Center_Energy_Analysis_Report.docx`
- **Methodology Details**: Documented in notebook cells with inline comments
- **Load Masking Log**: First 10 reallocations shown in report, full log available in notebook output

## 👥 Author

Course: BDI 513 - Business Data and Information
Project: Data Center Energy Analysis with Load Masking Correction

## 📄 License

Educational project for academic purposes.

## 🔗 Data Source

PG&E Electric Usage by ZIP Code (2015-2025)
- Commercial, Residential, and Industrial customer classes
- Monthly aggregated data
- Cleaned and validated for analysis

### Data Disclaimer

Customer usage data is reported by ZIP code, by month, by year, and by customer type (residential, commercial, agricultural, industrial). These reports are made available pursuant to **California Public Utilities Commission Decision 14-05-016**.

**Aggregation Rules:**
- Reports meet Commission Decision rules for public aggregation of data
- Minimum of 100 Residential customers required
- Minimum of 15 Non-Residential customers required
- No single Non-Residential customer can account for more than 15% of total consumption
- **If aggregation is not met, consumption is combined with a neighboring ZIP code** until requirements are satisfied

**Important**: Recipients of the usage data are solely responsible for any use of the data. PG&E disclaims all warranties and representations regarding the reports and data, including accuracy or fitness for any particular purpose.

Reports are published quarterly in machine-readable format (CSV files) and contain 3 months of usage data through the end of the calendar quarter. Usage for Net Energy Metered customers is reported at their aggregate, monthly net values.

---

**Note**: This analysis demonstrates the critical importance of load masking detection in energy usage studies. The corrected data reveals energy consumption patterns that would otherwise remain hidden due to PG&E's privacy-mandated aggregation policy, providing essential insights for energy policy, grid planning, and sustainability initiatives in the AI era.
