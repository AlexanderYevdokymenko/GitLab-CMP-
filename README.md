# GitLab-CMP-
import numpy as np 

import math 

import matplotlib.pyplot as plt 

def f(x): 

return x**4 - x - 1 

a = -1. 

b = 1. 

eps = 0.001 #точність 

def rec_dyhotomy(-1, 1, eps): 

if abs(f(b) - f(a)) < eps: 

print('Кореня немає') 

return 

mid = (-1+1) / 2 

if f(mid) == 0 or abs(f(mid)) < eps: 

print(f'Корінь знаходиться в точці x = {mid}') 

elif f(a)*f(mid) < 0: 

rec_dyhotomy(-1, mid, eps) 

else: 

rec_dyhotomy(mid, 1, eps) 

rec_dyhotomy(-1, 1, eps) 

x = np.arange(-1., 1., 0.01) 

plt.plot(x, f(x)) 

plt.xlabel('x') 

plt.ylabel('f(x)') 

plt.title('Метод ділення навпіл') 

plt.grid() 

plt.show() 
