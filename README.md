# d8-matplotlib
#line
from matplotlib import pyplot as ply

plt.plot([1,2,3],[4,5,1])
plt.show()

x = [5,8,10]
y = [12,16,6]
plt.plot(x,y)
plt.title('Info')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.show()

from matplotlib import pyplot as plt
from matplotlib import style
style.use('ggplot')

x = [5,8,10]
y = [12,16,6]
x1 = [6,9,11]
y1 = [6,15,7]
plt.plot(x,y,'g',label='LineOne',linewidth=5)
plt.plot(x1,y1,'c',label='LineTwo',linewidth=5)
plt.title('Info')
plt.xlabel('X axis')
plt.ylabel('Y axis')
plt.legend()
plt.grid(True,color='K')
plt.show()  

#bar
plt.bar([1,3,5,7,9],[5,2,7,8,2],label='Example One')
plt.bar([2,4,6,8,10],[8,6,2,5,6],label='Example Two',color='g')
plt.title('Bar graph')
plt.xlabel('bar number')
plt.ylabel('bar height')
plt.legend()
plt.show()

#histogram
population_ages = [22,55,62,45,21,22,34,42,42,4,99,102,110,120,
                   121,122,130,111,115,112,80,75,65,54,44,43,42,48]
bins=[0,10,20,30,40,50,60,70,80,90,100,110,120,130]
plt.hist(population_ages,bins,histtype='bar',rwidth=0.5)
plt.xlabel('x')
plt.ylabel('y')
plt.title('Histogram')
plt.legend()
plt.show()

#Scatter Plot
x = [1,2,3,4,5,6,7,8]
y = [5,2,4,2,1,4,5,2]
plt.scatter(x,y,label='skitscat',color='k')
plt.xlabel('x')
plt.ylabel('y')
plt.title('Scatter')
plt.legend()
plt.show()

#Stack Plot
days = [1,2,3,4,5]
sleeping = [7,8,6,11,7]
eating = [2,3,4,3,2]
working = [7,8,7,2,2]
playing = [8,5,7,8,13]
plt.plot([],[],color='m',label='Sleeping',linewidth=5)
plt.plot([],[],color='c',label='Eating',linewidth=5)
plt.plot([],[],color='r',label='Working',linewidth=5)
plt.plot([],[],color='k',label='Playing',linewidth=5)
plt.stackplot(days,sleeping,eating,working,playing,colors=['m','c','r','k'])
plt.xlabel('x')
plt.ylabel('y')
plt.title('Stack Plot')
plt.legend()
plt.show()

#Pie Chart
slices = [7,2,2,13]
activities = ['sleeping','eating','working','playing']
cols=['m','c','r','g']
plt.pie(slices,
        labels=activities,
        colors=cols,
        startangle=90,
        shadow=True,
        explode=(0,0.1,0,0),
        autopct='%1.1f%%')
plt.title('Pie Plot')
plt.show()

#Multiple Plots
from matplotlib import pyplot as plt
import numpy as np

def f(t):
    return np.exp(-t) * np.cos(2*np.pi*t)
t1=np.arange(0.0,5.0,0.1)
t2=np.arange(0.0,5.0,0.02)
plt.subplot(211)
plt.plot(t1,f(t1),'bo',t2,f(t2))
plt.subplot(212)
plt.plot(t2,np.cos(2*np.pi*t2))
plt.show()
