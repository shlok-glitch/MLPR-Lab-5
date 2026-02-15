# MLPR-Lab-5
Aim

The aim of this lab is to:
1. Detect human faces from an image using Haar Cascade.
2. Extract color-based features (Hue and Saturation) from detected faces.
3.Perform K-Means clustering on extracted features.
4. Classify a new template image (Dr_Shashi_Tharoor.jpg) into one of the clusters.
5. Visualize clustering results and template classification in feature space.

Methodology

1. Face Detection

Used OpenCV Haar Cascade (haarcascade_frontalface_default.xml).
Converted input image to grayscale.
Detected faces using detectMultiScale().

2. Feature Extraction

Converted face regions from BGR to HSV color space.

Extracted:
Mean Hue and Mean Saturation

Represented each face as a 2D point:
(Average Hue, Average Saturation)

3. Clustering

Applied K-Means clustering (n_clusters = 2).

Assigned cluster labels based on feature similarity.

Computed centroids of both clusters.

4. Template Classification

Detected face in template image.

Extracted HSV features.

Used kmeans.predict() to assign cluster label.

Visualized template in feature space with correct cluster color.

Visualizations

Face Detection Output
![Face Detection](images/face_detection.png)

K-Means Clustering in Hue–Saturation Space
![Cluster Plot](images/cluster_plot.png)


This plot shows:

Green points → Cluster 0

Blue points → Cluster 1

Black/Red markers → Cluster centroids

Template image plotted according to predicted cluster

Key Findings: 

Hue and Saturation are effective low-dimensional features for color-based grouping.

K-Means successfully separated faces into two distinct clusters.

The template image was correctly classified into one of the clusters.

Visualization confirms clustering consistency in HSV space.

Small changes in K value can significantly alter cluster boundaries.

Observations

Face detection parameters strongly affect clustering accuracy.

HSV color space provides better separation than raw RGB.

Mean feature representation simplifies clustering but may lose local texture details.

KNN and K-Means rely heavily on distance metrics.
