
# Theory

This is a step by step explanation of some of the implementation found in this code

## Segmentation 
Segementation is used to segment a point cloud in order to create 2 or more segments of the original point cloud.

Segmenation is performed by the the SegmentPlane Function.

#### SegementPlane Function Signature
```cpp
std::pair<typename pcl::PointCloud<PointT>::Ptr, typename pcl::PointCloud<PointT>::Ptr> SegmentPlane(typename pcl::PointCloud<PointT>::Ptr cloud, int maxIterations, float distanceThreshold);
```
This function takes a point cloude, max iterations, and sistance tolerance as arguments. Segmentation is iterative, more iterations result in better results but take linger. The segmentation algorithm fits a plane to the points and uses the distance tolerance to decide which points belong to that plane. A larger tolerance includes more points in the plane.

`SegmentPlane` returns `std:pair` holding point cloud pointer types. The pair will be used to hold segemented results (obstacles,road point cloud). These can later be visualised in pcl viewer.
