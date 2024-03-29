# Vector-Field-matplotlib
Vector fields associate a 2D vector to each point of the 2D plane. Vector fields are common in Physics as they provide solutions to differential equations. Matplotlib provides functions to visualize vector fields. To illustrate the visualization of vector fields, let's visualize the velocity flow of an incompressible fluid around a cylinder. We do not need to bother about how to compute such a vector field but only about how to show it. The pyplot.quiver() function is what we need.


How the project work:   
Although the script is a bit long, the purely graphical part is simple. The vector field is stored in the matrices U and V: the coordinates of each vector we sampled from the vector field. The matrices X and Y contain the sample positions. The matrices X, Y, U, and V are passed to pyplot.quiver(), which renders the vector field. Note that pyplot.quiver() can take just U and V as parameters, but then the legend will show the indexes of the samples rather than their coordinates. As the vector field that we used as an illustration here the fluid flow around a shape, the shape itself is shown as follows:  shape = patches.Circle((0, 0), radius = 1., lw = 2., fc = 'w', ec   = 'k', zorder = 0)  plt.gca().add_patch(shape)  The vector field inside the cylinder does not appear; we use a masked array. We first create a mask that defines which samples should be shown. Then, we apply this mask on U and V, as shown in the script. 

Output Plot: 
![Screenshot_2021-09-14-20-43-56-01](https://user-images.githubusercontent.com/34489444/133284513-8a57e679-c59b-4d44-95cf-c7e37dd3178b.jpg)

