#  Mean and variance of a discrete  distribution
### Developed by : NAVEEN KUMAR S

### Register number : 212223040129

# Aim : 

To find mean and variance of arrival of objects from the feeder using probability distribution


# Software required :  

Python and Visual components tool

# Theory:

The expectation or the mean of a discrete random variable is a weighted average of all possible
values of the random variable. The weights are the probabilities associated with the corresponding values. 
It is calculated as,

![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/10df0308-1d67-4fb8-95d5-271b7fa80baf)


The variance of a random variable shows the variability or the scatterings of the random variables.
It shows the distance of a random variable from its mean. It is calcualted as

![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/a8435827-39a5-46b8-9fc2-d74d7e91aeb8)



# Procedure :

1. Construct frequency distribution for the data

2. Find the  probability distribution from frequency distribution.

3. Calculate mean using 
   
   ![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/302e18cf-e5d0-4bc5-8088-64355646c229)


4. Find  
   
   ![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/057ac1ff-2a81-4efe-9619-368ec32d2445)


5.  Calculate variance using 
  
      ![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/b9d1d381-d59c-47f3-8d35-53aa85314760)



# Experiment :

![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/a5e8371f-6b12-45ca-b92e-63bbf0787ba0)


# Program :

```
import numpy as np
L=[int(i) for i in input().split()]
N=len(L); M=max(L) 
x=list();f=list()
for i in range (M+1):
    c = 0
    for j in range(N):
        if L[j]==i:
            c=c+1
    f.append(c)
    x.append(i)
sf=np.sum(f)
p=list()
for i in range(M+1):
    p.append(f[i]/sf) 
mean=np.inner(x,p)
EX2=np.inner(np.square(x),p)
var=EX2-mean**2 
SD=np.sqrt(var)
print("The Mean arrival rate is %.3f "%mean)
print("The Variance of arrival from feeder is %.3f "%var) 
print("The Standard deviation of arrival from feeder is %.3F "%SD)
```

# Output : 
![image](https://github.com/NAVEEN-2006/Mean-and-Variance/assets/152067648/7989238b-308e-44b4-b3b6-400a78db13d4)




# Results :
The mean and variance of arrivals of objects from feeder using probability distribution are calculated.

