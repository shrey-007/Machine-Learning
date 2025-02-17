Any data jo ki baakio se bahut alag hai vo outlier hota hai, and unhe remove krna bahut important hota hai else model will not work properly  

## oulier detection using standard deviation
Works with data having Normal distribution 
68% values lies between [m-std,m+std]  {1 standard deviation}
95% values lies between [m-2std,m+2std] {2 standard deviation}
99.7% values lies between [m-3std,m+3std]   {3 standard deviation}
Standard deviation show much much deviated you are from mean value. 1 standard deviation means you are close to mean, 2 standard deviation is far from mean, 3 standard deviation is very far from mean   
So any data which lies outside of the range of 3 standard deviation i.e [m-3std,m+3std], is an outlier  


## oulier detection using Z score
Z score is the measure of how many standard deviation you are away from mean, 1 standard deviation means z=1, 2 standard deviation ,eans z=2  
z=(x-mean)/stadard deviation , har data point x ke liye z score alag hoga  
So if z score is less than -3 or greater than 3 than it is an outlier  


## oulier detection using IQR[Inter Quartile Range]
min- min value of data  
Q1(25 percentile)- value bigger than 25% of data  
Q2(50 percentile)- value bigger than 50% of data   
Q3(75 percentile)- value bigger than 75% of data  
max- max value of data  

IQR= Q3-Q1  
lower_limit= Q1 - 1.5*IQR  
upper_limit= Q3 + 1.5*IQR  

If some data is ouside the range of [lower_limit,upper_limit] then it is outlier










