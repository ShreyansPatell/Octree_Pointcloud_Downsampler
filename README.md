# Octree_Pointcloud_Downsampler
In the course of our research, we frequently encounter unfiltered pointclouds– that is, 3D scans from our car’s sensors that have not been processed. These unfiltered pointclouds contain usually contain many more points than we need.

We use a process called “downsampling” to remove unnecessary points. By downsampling, the complexity of our 3D data is reduced, which makes our algorithms faster down the road.

# Program Requirements
Write a program in either C++ or Python that reads a pointcloud from a labelled CSV file, downsamples this pointcloud, then writes the result to a second CSV file.

1. Input: input.csv (Available in the repository)
2. Output: output.csv (with the same general format as the input CSV)
3. Submission: A single .cpp or .py file with a main function. The file can be formatted in any way you choose.
4. Downsampling can be done by any method, from removing points at random to distributing points along a voxel grid, anything works. Probably the coolest implementation would involve distributing points using an octree– (https://en.wikipedia.org/wiki/Octree) that’s code we would actually use on the car!

# Target Qualities
We’re looking for efficient, cleanly written downsamplers that fulfill the requirements above. Everything else is up to you, including:

1. How many points to remove (this depends on your implementation, but it doesn’t really matter to us),
2. How to select which points to remove (see requirement above), and so on.

Implementations that remove points systematically (i.e. uniformly in space, or based on a target feature like edges) will be scored higher than programs that remove points randomly. If this all sounds crazy, keep it simple and just submit something that works.

# Evaluation Process
Submissions will be evaluated by a blind panel of developers on our team. That is, your submission will be anonymized before evaluation. This panel will score your code within the following categories using a 12-point scale:

1. Efficacy: Does your program work? Does it remove points systematically? (5 points)
2. Clarity: Is your code readable? Does it have a clear structure, with functions separated logically? (4 points)
3. Efficiency: Does your code have a reasonable runtime, or does it have excessive runtime complexity? (3 points)
4. Creativity: This is where our panel can recognize extra effort, unique approaches, and so on. (3 bonus points possibly)

# Notes and Tips
1. You should be able to accomplish this with standard C++ libraries, but Boost is also perfectly welcome.
2. The input positions are in meters, though this is arbitrary.
3. You’re welcome to accept additional parameters from the user or from a config file, but you can stick to hardcoded values as well.
4. The input pointcloud is a scan of an apartment from this dataset (https://projects.asl.ethz.ch/datasets/doku.php?id=laserregistration:apartment:home).
5. If you’d like to visualize your input and output pointclouds, Paraview (https://www.paraview.org/) is a popular data visualiztion program that can do just that (and it handles CSV files easily). Not required, but could help.