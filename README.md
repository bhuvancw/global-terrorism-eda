# global-terrorism-eda

A concise exploratory data analysis (EDA) of the Global Terrorism Database (2000–2017) implemented in a Jupyter notebook.

Project summary

This repository contains an EDA that loads the Global Terrorism Dataset (GTD), performs data cleaning and aggregation, and explores temporal, regional, tactical, and geographic patterns in recorded terrorist incidents between 2000 and 2017. The analysis includes time-series trends, regional breakdowns, attack-type distributions, correlation and outlier analysis (incidents vs. casualties), and interactive mapping of event locations.

Dataset

- Source / file: extracted_data\datasets\globalterrorismdb_0718dist.tar.bz2 (the notebook expects the GTD data archive to be present and extracted in the `extracted_data` folder).

Key methodology

- Load GTD (bz2) into pandas, handle mixed dtypes and missing values, and create derived columns (year, month, casualties).
- Aggregate incidents and casualties by year, region, and attack type; compute correlations and identify outlier events.
- Visualize trends using matplotlib/seaborn and create an interactive folium map (marker clustering) for geographic exploration.

Key findings (brief)

- Global incidents peaked in 2014 (≈16,900 reported incidents) and declined to ~10,900 by 2017; the rise is temporally associated with ISIL activity but many incidents remain recorded as "Unknown" perpetrators.
- Incidents and total casualties are strongly correlated at the yearly level (r ≈ 0.96), but a small number of catastrophic single events (e.g., 9/11, 2014 mass-casualty incidents in Iraq, Mogadishu 2017) drive a large portion of total deaths.
- Bombing/Explosion is the dominant attack type worldwide (by a large margin), with regional tactical variation: the Middle East & North Africa shows extreme bombing concentration; South Asia has a more balanced mix (bombings + armed assault); Sub-Saharan Africa shows relatively more hostage-taking incidents.
- Geographic concentration is clear: the Middle East, South Asia, and parts of Sub-Saharan Africa show the highest incident densities in the 2000–2017 window.


View on GitHub: https://github.com/bhuvancw/global-terrorism-eda/blob/main/global_terrorism_eda.ipynb
