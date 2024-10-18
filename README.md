# RATINGS: scRaping and AnalyzIng biTcoIN mininG poolS

## Project Overview:
**RATINGS** is a project aimed at de-anonymizing and analyzing Bitcoin miners and mining pools by working with early Bitcoin transaction data (2009–2012). Using a combination of **blockchain transaction datasets** and **web scraping**, the project uncovers the behavior of mining pools and tracks Bitcoin flows. Key aspects include identifying major mining pools, analyzing their transaction behaviors, and studying their historical impact on Bitcoin's network.

## Key Objectives:
- **De-anonymize Mining Pools**: Identify the addresses used by early mining pools through web scraping and map them to their activities in the blockchain dataset.
- **Analyze Blockchain Transaction Data**: Examine trends in transaction fees, script usage, and mining activity between 2009 and 2012.
- **Trace Bitcoin Flows**: Use network graphs to follow Bitcoin as it moves from miners to the wider network.

## Dataset Information:
The project uses a custom dataset containing Bitcoin transaction data from **block 0 (Genesis block, January 2009)** to **block 214562 (December 2012)**. The dataset is a smaller, transformed subset of the full Bitcoin blockchain, with the following files:
- **`transactions.csv`**: Contains transaction details (timestamps, block IDs, fees).
- **`inputs.csv`**: Details the inputs of each transaction (including previous transaction references).
- **`outputs.csv`**: Provides output information, including receiving addresses and amounts.
- **`mapping.csv`**: Maps anonymized address IDs to actual Bitcoin addresses for analysis.

## Important: 
Due to the size of the Dataset, i am unable to upload it here, in case of need contact me at leopuosi@protonmail.com

## Main Features:
1. **Transaction Fee and Congestion Analysis**:
   - Analyze the relationship between transaction fees and network congestion during the early days of Bitcoin.
   - Measure congestion by calculating transaction sizes and observe how fees varied as congestion increased.

2. **Script Type Evolution**:
   - Study the usage of different Bitcoin script types over time, focusing on their role in Bitcoin transactions during the dataset period.
   - Investigate changes in transaction patterns based on script types.

3. **Mining Pool De-anonymization**:
   - Scrape data from **WalletExplorer** to associate Bitcoin addresses in the dataset with known mining pools (e.g., DeepBit, Eligius, BTC Guild, BitMinter).
   - Identify the top individual miners and classify addresses that belong to large pools versus independent miners.
   
4. **Mining Pool Statistics**:
   - Provide detailed statistics for each mining pool, including the number of blocks they mined and the total rewards they received.
   - Analyze trends in mining activity over two-month intervals, capturing changes in the dominance of different pools.

5. **Bitcoin Flow Tracing**:
   - Perform **taint analysis** by tracking the flow of Bitcoin from specific mining pools through multiple transactions.
   - Visualize the flow using **network graphs** to see how mined Bitcoin was spent and circulated in the network.

## Libraries and Tools:
- **Pandas**: Data handling and manipulation of CSV datasets.
- **Matplotlib & Seaborn**: Data visualization for transaction trends, mining pool statistics, and network congestion.
- **NetworkX**: Creation of network graphs to trace Bitcoin flows.
- **BeautifulSoup & Requests**: Web scraping tools used to fetch Bitcoin address data from WalletExplorer for de-anonymization purposes.
- **Additional Libraries**: `fake_useragent`, `random`, `re`, and `time` are used for managing web scraping and other utilities.

## How to Get Started:

1. **Install Dependencies**:
   Install the required Python libraries:
   ```bash
   pip install pandas matplotlib seaborn requests beautifulsoup4 fake-useragent networkx
   ```
2. **Download Datasets**: Ensure the following datasets are available in a Datasets directory:

    transactions.csv
    inputs.csv
    outputs.csv
    mapping.csv

3. **Run the Notebook**: Open Progetto.ipynb in Jupyter Notebook. Execute the cells to run the analyses, which include fee trends, mining pool de-anonymization, and Bitcoin flow tracing.

## Graph examples:
### Correlation between Network Congestion and Average Fee:
   
![image](https://github.com/user-attachments/assets/cfcb2578-dfe9-4183-90da-05b40862be0a)

### Taint Analysis:
   
![image](https://github.com/user-attachments/assets/2a1c5c5e-988e-4443-a1b8-3f33925cf014)


