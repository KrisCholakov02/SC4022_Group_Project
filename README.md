# SC4022 NETWORK SCIENCE - Group Project

## Project Title: **Network Science-Based Analysis of Collaboration Network of Data Scientists**

## Group Members

- **CHOLAKOV KRISTIYAN KAMENOV** (U2123543B)
- **DHANYAMRAJU HARSH RAO** (U2023045C)
- **CHUA WEE SIANG FRASER** (U2122535E)

---

## Project Overview

In this project, we perform a **network science-based analysis** of the collaboration network of data scientists. By leveraging real-world data extracted from DBLP, we construct and analyze a large-scale collaboration network, providing insights into its structure, properties, and evolution over time.

Our study explores various aspects of the network, including **degree distribution, clustering coefficients, centrality measures, and network evolution**, as well as comparisons with randomly generated networks. Additionally, we propose methods to **reduce network size** while preserving key structural properties.

### **Purpose and Objectives**
- Construct a **collaboration network** of data scientists using **DBLP data**.
- Perform **statistical and visual** analysis of the network’s structure.
- Compare the real-world network with a **randomly generated Erdős-Rényi network**.
- Study the **evolution of the network** over time.
- Investigate the impact of **external collaborators** on the network.
- Develop **network reduction techniques** that maintain essential properties.

### **Novelty and Contributions**
- **Comprehensive Data Analysis**: We apply **advanced data preprocessing and cleaning** techniques to create a high-quality dataset.
- **Real vs. Random Comparison**: Our study contrasts the **real-world collaboration network** with a **randomly generated** network, identifying key differences.
- **Network Evolution Insights**: We analyze how **data science collaborations** evolved over time and how major hubs emerged.
- **Network Reduction Techniques**: We propose and evaluate methods for reducing the network while **preserving connectivity** and diversity.
- **Visualization and Interpretation**: We employ **state-of-the-art network visualization tools** to illustrate key findings.

---

## Data Collection and Processing

We extract data from **DBLP**, a publicly available database of scientific publications. Our dataset consists of over **1000 data scientists** and their collaborative relationships. The data was processed as follows:

1. **Data Crawling**: Extracting author details and publication records from DBLP.
2. **Preprocessing & Cleaning**:
   - Removing duplicates and inconsistencies.
   - Extracting relevant metadata (e.g., author names, institutions, publication year).
3. **Network Construction**: Building an undirected graph where nodes represent **scientists**, and edges represent **collaborations**.

---

## Network Analysis

We analyze the collaboration network using **NetworkX**, a powerful Python library for network analysis. Key properties examined include:

### **1. Network Properties**
- **Degree Distribution**: Follows a **power-law**, confirming a **scale-free** network structure.
- **Centrality Measures**: Identifies key hubs (most influential scientists).
- **Clustering Coefficient**: Measures local connectivity between scientists.
- **Connected Components**: Identifies isolated researchers.

### **2. Network Evolution Over Time**
- Tracking the **growth of the giant component**.
- Observing how **hubs** emerge over time.
- Measuring **diameter and average path length** changes.

### **3. Comparison with a Random Network**
- We generate an **Erdős-Rényi (ER) model** with the same number of nodes and edges.
- Our results highlight structural differences:
  - **The real network follows a scale-free structure, while the ER model is uniform.**
  - **The real network has a higher clustering coefficient, showing natural group formation.**
  - **Real network hubs play a crucial role in connectivity.**

### **4. Network Reduction Strategies**
We propose two strategies for reducing network size while maintaining **structural integrity**:
1. **Hard Cutoff for Normalized Degree Difference** (Best Performing)
2. **Scale-Free Reduction using Closeness Centrality Difference**

---

## External Collaborators Analysis

To enhance our understanding, we include **external collaborators** from the DBLP dataset. Key findings:
- The inclusion of external authors **increases the network size significantly**.
- The **degree distribution still follows a power-law**, confirming its scale-free nature.
- **Central hubs remain dominant**, even with new connections.

---

## Installation and Setup

To run this project, install the required dependencies:

### **Prerequisites**
- Python 3.8+
- NetworkX
- Pandas
- Matplotlib
- NumPy

### **Installation**
Run the following command to install the required libraries:

```bash
pip install -r requirements.txt
```

---

## Results and Insights

### **Key Takeaways**
- **Data science collaborations exhibit a scale-free network structure.**
- **A few highly connected scientists act as hubs, enabling efficient knowledge sharing.**
- **Over time, the network evolved to be more interconnected, with a decreasing diameter.**
- **Compared to a random network, real-world collaborations are more clustered and structured.**
- **Effective network reduction techniques can be applied without losing key properties.**

---

## Future Work
- **Exploring temporal dynamics further** using predictive models.
- **Studying institutional influence** on collaborations.
- **Applying machine learning** for automated pattern detection.

---

## References
- **Clauset, A., Shalizi, C. R., & Newman, M. E. J.** (2009). *Power-law distributions in empirical data.* SIAM Review, 51(4), 661-703. doi: [10.1137/070710111](https://doi.org/10.1137/070710111)

---

## Acknowledgments
This project was completed as part of **SC4022 - Network Science** at **Nanyang Technological University (NTU), Singapore**. We would like to thank our professor and teaching assistants for their guidance.

