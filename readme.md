CSE 102 Programming Assignment 1

Description
    • This is an individual assignment. Please do not collaborate
    • If you think that this document does not clearly describe the assignment, ask questions before its too late.
    This is a C Programming assignment. You will write a C program according to the following description.
    • Your program captures user input, learns and tests a simple classifier. This assignment is about using control
    statements, performing arithmetic operations and simple input/output.
    • You are expected to divide the solution into blocks and use functions.
    Program Description
    There are three clusters(groups) of points in a 2 dimensional cartesian coordinate system. Every point has an x and
    y coordinate.

 Program Flow
    • The program first accepts center points for three clusters (Cluster 1, 2 and 3).
    • After reading center points of three clusters, the program continues to capture point coordinates.
    • Once a point coordinate is captured, the program decides to put this point to a particular cluster.
    • After including a point in one of the three clusters, the program updates the center point of the chosen cluster.
    • The program stops after capturing N number of points. (N is a macro)
    • At the end of the program, averages of x,y coordinates of every cluster and the total number of points included
    in each cluster is printed.

 • Format:
    Cluster 1: x_coordinate_of_the_center, y_coordinate_of_the_center, number_of_points_in_cluster_1
    Cluster 2: x_coordinate_of_the_center, y_coordinate_of_the_center, number_of_points_in_cluster_2
    Cluster 3: x_coordinate_of_the_center, y_coordinate_of_the_center, number_of_points_in_cluster_3
    
    How to decide which cluster a point belongs to?
    
        • Given a point, calculate distances of this point to three cluster centers.
        • Choose the closest cluster if there is at least X percent difference between the closest one and the next closest
        one. (X is a macro)
        • If there is less than X percent difference, discard the point. Ignore the point and don’t change any center
        points of any clusters.
        • If the point was discarded, print the following message:
        Point x_coordinate, y_coordinate was discarded.
        • If a point was included in one of the clusters(Example: Cluster 1), print the following message:
        Point x_coordinate, y_coordinate was included in Cluster 1
        How to update the center point of a clusters?
        • Update x and y coordinates of the center point of the cluster by calculating a new average x and average y by
        including the new point. You have to include the total number of points in the calculation.
        • new_x = (old_x*number_of_points + point_x)/(number_of_points+1)
        
    Input Format
    x_coordinate y_coordinate
