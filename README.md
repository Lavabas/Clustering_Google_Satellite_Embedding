# Clustering Google’s Satellite Embedding Dataset for Colombo, Sri Lanka
## Overview

This project demonstrates how Google’s Satellite Embedding Dataset (GOOGLE/SATELLITE_EMBEDDING/V1/ANNUAL) can be leveraged to extract meaningful spatial patterns through unsupervised clustering. The analysis focuses on a selected region in Colombo, Sri Lanka, where urban growth and land cover diversity make it an ideal testbed.

The importance of this type of analysis lies in the ability of AI-derived embeddings to capture complex spatial, spectral, and contextual information that goes beyond traditional remote sensing indices. By clustering these embeddings, we can uncover hidden spatial patterns in land use and urban form, identify zones with similar morphological characteristics, and monitor subtle transformations that may not be evident through raw imagery. In rapidly growing cities like Colombo, such insights are valuable for urban planning, environmental monitoring, and sustainable development decision-making. Furthermore, embedding-based clustering reduces the need for manually labeled training data, making it a powerful tool for scalable, data-driven exploration of Earth Observation datasets.

### Raw Embedding Visualization
<img width="583" height="455" alt="image" src="https://github.com/user-attachments/assets/91437363-7181-474c-a631-b64236e39074" />

- Satellite embedding values (Band A01) for the Colombo ROI, capturing spectral and contextual information from Google’s Satellite Embedding dataset.

### Clustering Result (KMeans – 7 Clusters)
<img width="558" height="455" alt="image" src="https://github.com/user-attachments/assets/736077e5-84c5-4f21-ad29-24cf4051226e" />

- Unsupervised clustering of the embedding data into 7 distinct land-cover/land-use groups within Colombo. Each cluster reflects areas with similar spectral and morphological characteristics.

## Tools and Libraries
- Google Earth Engine (GEE) – for accessing and processing the satellite embedding dataset
- geemap – interactive visualization and ROI selection
- xee – Python engine for direct extraction of Earth Engine datasets into Xarray
- xarray – handling large multidimensional geospatial datasets
- rioxarray – CRS handling and GeoTIFF export
- scikit-learn – KMeans clustering of embedding features
- matplotlib – visualization of results

## Dataset
Google’s Satellite Embedding Dataset (GOOGLE/SATELLITE_EMBEDDING/V1/ANNUAL)
 1. Provides annual embeddings derived from global satellite imagery
 2. Captures complex spatial and spectral features useful for machine learning tasks
 3. Temporal coverage: 2015–2022 (annual composites)
 4. Applied here for 2021 data over part of Colombo

## Notes
- The ROI was selected near Colombo, Sri Lanka, with a ~5km extent to balance detail and compute efficiency.
- The KMeans clustering output does not represent land cover classes directly; rather, it groups similar embedding patterns. Post-processing or label interpretation is needed for thematic mapping.
- For larger regions, consider scaling cluster numbers or performing dimensionality reduction (e.g., PCA) before clustering.
- The workflow can be extended to other areas (urban, rural, coastal) or adapted for temporal analysis across years.
