# Matrix-Factorization (MF)
Matrix factorization is a way to generate latent features when multiplying two different kinds of entities.
Suppose we have a user item table, where there are 5 users and 5 items . The 5 users rates the item differently.
![image](https://user-images.githubusercontent.com/45823099/125603428-1f80bfbc-346b-4cad-88f7-ca8c4ec28398.png)
From the image we can see that there are some missing valuesm in the given table. With the help of MF we can predict the missing values.

Mathematical Concept::
Suppose, U = set of users
D = items
R = size of |U| and |D|
|U| * |D| includes all the ratings given by the user.
k = latent features
P = user and feature value
Q = item and feature value
Now,
![image](https://user-images.githubusercontent.com/45823099/125604892-8a2f319a-7a36-4cfb-9f7a-6f319e2ec44d.png)
We can get the prediction of a rating of an item by calculation of the dot product of the 2 vectors corresponding to u_i and d_j.
![image](https://user-images.githubusercontent.com/45823099/125607346-8ef1a792-1e97-4191-9b37-b5628143f548.png)
To get two entities of both P and Q we need to initiate the 2 matrics and calculate the difference of the product named as matrics M. Next we minimize the difference through the iteration. The method we used here is Gradient Discent (GD) aiming at finding local minimum of the differences,
![image](https://user-images.githubusercontent.com/45823099/125711109-4193f0f3-9afb-4b25-96ef-f5d83553fe14.png)
From the gradient, the mathematic formula can be updated for both p_ik and q_kj. a is the step to reach the minimum while the gradient is calculated, and a is usually set with a small value.
![image](https://user-images.githubusercontent.com/45823099/125711305-5de712b0-d5c8-455a-a7d8-8bf22c6a5e40.png)
From the above equation, p’_ik and q’_kj can both be updated through iterations until the error converges to its minimum.
