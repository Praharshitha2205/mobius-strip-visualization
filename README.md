# mobius-strip-visualization - Short- write up

How I Structured the Code:
I organized the code in an object-oriented manner by declaring a Python class called MobiusStrip. It served to consolidate all concerned functionalities—such as mesh creation, visualization, surface area calculation, and edge length determination—into one reusable framework. The class accepts three arguments: radius R, width w, and resolution n. The surface is created based on a parametric formula of a Mobius strip, and the visualization() function uses matplotlib to visualize the 3D surface.

How I Approximated Surface Area:
I approximated the surface area by using a triangular mesh. The surface was discretized in the first place by a grid of n x n points. Then, in each small quadrilateral (defined by neighbor grid points), I subdivided it into two triangles. The area of each triangle was calculated based on the magnitude of the cross product of two edge vectors. I added all the areas of the triangles to obtain an approximation of the overall surface area.

Challenges I Faced:
One of the main challenges was understanding how to properly parametrize the Mobius strip in 3D space. Getting the twist and orientation right required careful application of trigonometric functions. Another tricky part was computing surface area from a discretized mesh—making sure the order of points in each triangle was correct to avoid negative or incorrect area values. 
