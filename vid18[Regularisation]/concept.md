When we train data, it can create a overfitting or underfitting model.
1. Hume age of players given hai and find krna ha ki us age ke players match jita paaege ki nhi
2. Toh pehle simple linear function of age use kra, but usse bahut error aa rha hai, it is called underfit
3. Phir linear ki jagah higher order of age introduce kri(second graph) and usse training data ke points bahut achhe se map ho gye but agar ise testing data doge toh ye galat ans dega, it is like isne concept ko samajahne ki jagah ratt liya, isne koi pattern dhoonda hi nhi data mai
4. So in third graph humne kuch higher powers ko drop kra and is baar balanced fit model mila hume
![img](images/Screenshot%202024-08-31%20120608.png)
5. So we have to reduce the higher powers of features, and for that we use L1 Regularization(Lasso) and L2 Regularization(Ridge)
![img](images/Screenshot%202024-08-31%20120704.png)
6. Toh jo humara normal Cost function hota hai usme hum ye extra term add kr dete hai jisse higher powers of age ke coefficients  0 ho jaate hai. 
![img](images/Screenshot%202024-08-31%20121313.png)
![img](images/Screenshot%202024-08-31%20121321.png)
