# This function finds the greatest common denominator of a number, this is necessary to find repeated PPTs.

def mygcd(a,b):           # I begin by defining a new function named 'mygcd', this will be called to eliminate non-PPTs
    while a!=b:           # This loop runs while a is not equal to b
        if a<b:           # If a is less than b, the following indented line runs
            a,b = b,a     # swap values of a and b so that a is the larger number
        a = a%b           # The Modulo '%' returns the remainder of dividing a by b, a is assigned the remainder
        if a==0:
            return b      # Now, if the remainder is equal to zero, return b, if not return a
    return a
    
from math import sqrt     # The square root function is not embedded into python and must be imported from the math library
max = 5000
A = []
B = []
C = []                    # I created three empty lists for each of a, b, and c
for a in range(1,max):    # I begin the code with a loop testing every a against every larger number up to 5000
    for b in range(a,max):    # By setting the loop b from a to max, b will be larger than a
        c = sqrt(a**2 + b**2) # I use some algebra to find c
                              
        # Is c an integer? This checks if c is an integer, as well as if it is an integer multiple 

        if int(c)==c and mygcd(a,b)==1:   # Integer multiples of a and b will be eliminated, to ensure all are primitive
            #print(a,b,int(c))# Print each triple, the integer function is used otherwise c will print with decimal zero
            A.append(a)
            B.append(b)       # Store each part of each of the PPTs to their respective list
            C.append(c)
import matplotlib.pyplot as plt    # I have to import the function to create a plot from the matplotlib (library)
plt.figure(figsize=(10,10))         # I change the figure size for ease of view
plt.ylabel('C')
plt.xlabel('A,B')
plt.plot(A,C,'ro',markersize = 1)   # I adjusted the marker size to 1 to more clearly see the dispersion
plt.plot(B,C,'co',markersize = 1)
plt.show()                          # This shows the plot

# import matplotlib.pyplot as plot    # I have to import the function to create a plot from the python library
plt.figure(figsize=(10,10))
plt.ylabel('C')
plt.xlabel('C')
plt.plot(C,C,'mo',markersize = 0.4)
plt.show()
plt.ylabel('A')
plt.xlabel('A')
plt.plot(A,A,'co',markersize = 0.4)
plt.show()
plt.ylabel('B')
plt.xlabel('B')
plt.plot(B,B,'ro',markersize = 0.4)
plt.show()
