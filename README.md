# 2D Point Distribution Algorithms

This project demonstrates various algorithms for distributing points in a 2D plane. The algorithms include random distribution, Poisson disk sampling, centroidal Voronoi tessellation, farthest point sampling, K-means clustering, and several noise-based methods.

## Features

- **Uniformly Random**: Distributes points randomly across the plane with uniform distribution.
- **Poisson Disk Sampling**: Generates random points that are at least a minimum distance apart, creating an even distribution without regular patterns.
- **Centroidal Voronoi**: Positions points such that each point is at the centroid of its Voronoi cell, creating an evenly spaced distribution.
- **Farthest Point Sampling**: Iteratively places each new point at the position farthest from all existing points, maximizing coverage.
- **K-Means Clustering**: Positions points to minimize the distance between points and cluster centers, creating distinct groupings.
- **Simplex Noise Displacement**: Uses simplex noise to offset the position of points from a regular grid, creating a displacement effect.
- **Simplex Noise Density Control**: Uses Simplex noise to determine the probability of a point being placed. Areas with higher noise values have a higher density of points.
- **Simplex Noise Mask**: Uses simplex noise to create a mask, placing points only where the noise value is above a certain threshold.
- **Jittered Grid**: Starts with a uniform grid and adds a small random offset to each point's position, creating a slightly irregular but still evenly spaced distribution.
- **Perfect Grid**: Distributes points in a perfect grid pattern, with each point evenly spaced from its neighbors.

## Usage

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/point-distribution.git
    ```
2. Open `index.html` in your web browser to view the application.

## Metrics

The application calculates and displays various metrics to evaluate the point distributions:

- **Avg Nearest Neighbor Distance**: The average distance between each point and its nearest neighbor. Lower values indicate denser clustering.
- **Voronoi Cell Area Variation**: The standard deviation of the areas of the Voronoi cells. Lower values suggest a more uniform distribution.
- **Grid-Based Density**: The standard deviation of the number of points in each grid cell. Lower values indicate a more uniform density distribution.
- **Clark-Evans Index**: Compares the observed mean nearest neighbor distance to the expected mean nearest neighbor distance in a random distribution. Values less than 1 indicate clustering, values around 1 indicate randomness, and values greater than 1 indicate uniformity.
- **Spatial Autocorrelation (Moran's I)**: Measures the degree to which points are clustered or dispersed. Positive values indicate clustering, negative values indicate dispersion, and values around 0 indicate randomness.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## Acknowledgements

- [Voronoi.js](https://github.com/gorhill/Javascript-Voronoi) for Voronoi diagram calculations.
- [SimplexNoise.js](https://github.com/jwagner/simplex-noise.js) for noise generation.

## Contact

For any questions or suggestions, please contact [avanderw](mailto:avanderw@gmail.com).