# clustering-exercise-

Algorithm, K-means, hierarchical clustering algorithm

Using k-means algorithm and Euclidean distance, cluster the data from A1 to A8. To start, consider A1, A4, A7 as the center of clusters.

A1=(2,10), A2=(2,5), A3=(8,4), A4=(5,8), A5=(7,5), A6=(6,4), A7=(1,2), A8=(4,9)

For questions A, B and C, calculate the algorithm only once and then answer accordingly.

a) Show the new clusters as sets.

b) show the center of the new clusters with a star.

c) Draw a 10x10 coordinate diagram and draw the new clusters and centers after the first calculation of the algorithm.

d) How many times (epoch) is needed for the algorithm to reach convergence? (You can draw only the coordinate diagram of each stage for convenience, otherwise show the clusters as a set.)

**answer**

solve this step by step using the k-means algorithm.

1. **Initialization**: We start with 3 initial clusters with centers at A1, A4, and A7.

2. **Assignment Step**: Assign each data point to the nearest cluster by calculating its distance to each centroid.

3. **Update Step**: Calculate the new centroids (mean) of the points in each cluster.

Let's calculate:

**Assignment Step**:

- Calculate the Euclidean distance from each point to the centroids A1, A4, and A7.

- For A2, the distances to A1, A4, and A7 are:

  $$d(A2, A1) = \sqrt{(2-2)^2 + (5-10)^2} = 5$$
  $$d(A2, A4) = \sqrt{(2-5)^2 + (5-8)^2} = \sqrt{18} \approx 4.24$$
  $$d(A2, A7) = \sqrt{(2-1)^2 + (5-2)^2} = \sqrt{10} \approx 3.16$$

  So, A2 is closest to A7.

- Repeat this process for all other points (A3, A5, A6, A8).

**Update Step**:

- After assigning all points to the closest centroid, recalculate the centroids as the mean of all points in the cluster.

- For example, if the points in the cluster of centroid A1 are {A1, A8}, the new centroid would be the average of these points.

This process is repeated until the centroids do not change significantly, or a certain number of iterations have been reached. For this question, we only need to calculate the algorithm once.

Please note that the k-means algorithm does not guarantee an optimal solution because it depends on the initial placement of the centroids. Therefore, the final solution might be a local optimum. To mitigate this, the algorithm is usually run multiple times with different initial placements. The most common result is chosen as the final solution.
