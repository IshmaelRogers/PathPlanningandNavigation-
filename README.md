# PathPlanningandNavigation

The inputs to a Path Planning Algorithm:

0. Environment Geometry
1. Robot Geometry 
2. Start Pose of the Robot 
3. Goal Pose of the Robot 

The algorithm uses this information to produce a path from start to goal. 

# Examples

A land rover is dropped off at one position and needs to navigate its way to the another postion on a map. The robot know that there are obstacles in its path based on the provided map. GPS data and aerial photographs aid the robot in finding its goal location. 

Obstacles can make it difficult to traverse the shortest path. In this case the robot must find another path to reach its goal. 

## Terminology 

* Complete - An algorithm is complete if it can find a path between start and the goal when one exists
* Optimal - An algorithm is optimal if it is able to find the best solution. 

*Note* - "Best" solution can depend on many factors. In most cases it means finding the shortest path from start to goal location.

## Bug Algorithm 

The Bug Algorithm can be implemented as followed:

0. Head in directly towards the goal
1. If an obstacle is encountered:
    Traverse the obstacle clockwise until the robot can follow the original path towards the goal again. 
 
 The bug algortihm is neither complete nor optimal.

# Approaches 

## Discrete Planning 

Explicitly discretizes the robot's workspace into a *Connected Graph* and applies a *Graph-search* algorithm to caclulate the best path. The approach is very precise and very throrough. Discrete planning can be very computationally expensive- possibly impossible for large path planning problems. It is best suited for low-dimensional problems. For high-dimensional problems, * Sample-based Path Planning is a more appropriate approach. 

## Sample-based Planning 

Probes the workspace to incrementally construct a graph. Instead of discretizing every segment of the workspace, sample-based planning takes a number of samples and uses them to build a discrete representation of the workspace. The resultant graph is not a precise as the one generated using discrete planning but it is much quicker to create because of the small number of samples used.

A path generated using sample-based planning may not be the *best* path but in certain applications, it's better to generate a feasible path quickly rather than wait hours or days to generate the optimal path. 

## Pobabilistic Planning

Takes into account the uncertainity of the robot's motion. This doesn't provide significant benefits in some environments, it is especially helpful in highly-constrained environments or environments with sensitive or high-risk areas. 

# Discrete Planning

1. Develop Continuous Representation, by representing the problem space as the configuration space (C-Space). The C-Space takes in account the geometry of the robot and makes it easier to apply discrete search algorithms . 


# Continuous Representation

# Minkowski Sum 

# Translation and Rotation

# 3D Configuration Space

# Discretization

# Road Map

# Visibility Graph

# Voronoi Diagram

# Cell Decomposition 

# Approximate Cell Decomposition

# Potential Field 

# Graph Search 

# Terminology

# Breadth-First Search

# Depth-First Search 

# Uniform Cost Search

# A* Search 

# Overall Concerns

# Graph-Search 

# Discrete Planning (wrap up)
