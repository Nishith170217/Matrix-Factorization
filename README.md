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
To get two entities of both P and Q we need to initiate the 2 matrics and calculate the difference of the product named as matrics M. Next we minimize the difference through the iteration. The method we used here is Gradient Discent (GD) aiming at finding local minimum of the differences,
