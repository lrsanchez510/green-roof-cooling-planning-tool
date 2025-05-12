# green-roof-cooling-planning-tool
This repository hosts the "Green Roof Cooling Planning Tool", a digital mapping tool that allows urban planners to understand which green roof projects could yield the greatest local cooling potential.

This tool serves as the culminating final project for ESPM 288 Reproducible & Collaborative Data Science at UC Berkeley for the Spring 2025 semester for Lino Sanchez.

The Green Roof Cooling Planning Tool leverages geospatial analysis and machine learning to help predict where an installed green roof will yield the greatest surrounding cooling impact as a direct function of land coverage and land surface temperature. The goal of this tool is to support efforts of urban heat island mitigation by allowing for strategic deployment of green roof strategies across major cities facing challenges of heat risk. 

New York City is chosen as an initial case study for this tool, given the city's known efforts to mitigate the urban heat island effect, but also given the great accessibility of geospatial data that would make such a tool functional. Because the City of New York provides so much data that is publicly accessible, there is much potential to leverage available data sets for environmental planning purposes. Here, we leverage land cover data derived from LiDAR (Light Detection and Ranging) and land surface temperature to understand how the urban environment influences localized outdoor temperatures and heat vulnerability.

The core functionality of this tool involves mapping a building footprint for New York City and calculating the mean land surface temperature for each building within a 50-meter radius, and calculating the percentage of pixels within that buffer that are registered as either paved or vegetated. This is followed by marking whether each building has a green roof or does not have a green roof, accounting for building height and roof surface area. Random Forest Regression (RFR) is then implemented to predict the total surrounding cooling potential of any building without a green roof, if it were to have a green roof installed. The RFR model is trained across the entire building footprint, learning how well green roofs are able to lower surrounding land surface temperatures as a function of surounding land cover, with the idea that some green roof projects will lead to a more substantial localized cooling impact than others.

Accordingly, this tool allows the user to pan through a mapped building footprint of New York City and visualize all green roof buildings next to all non-green roof buildings. The user can simply click on a non-green roof building (dark grey polygons) to reveal the total cooling potential within 50 meters should a green roof be installed.

![image](https://github.com/user-attachments/assets/b709f346-5c26-4e2b-bf7d-fbdd057398e9)

For this tool to work, specifically utilizing the 'Green_Roof_Planning_Tool.ipynb' a some data will need to downloaded and referenced within the Jupyter Notebook:

New York City Land Cover Data (2021): https://zenodo.org/records/14053441
