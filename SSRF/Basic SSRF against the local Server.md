This lab has a stock check feature which fetches data from an internal system.

To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

After starting the lab we go to the stock change feature and capture the request using burpsuite.

![](images/6431effda94b18955eafaeab181fccf5_MD5.jpeg)

Then we send the request to repeater and at **stockApi** we write http://localhost/admin

![](images/84c4fd4698f43a56e4d5eb9266d136a4_MD5.jpeg)

Now we send the request

![](images/6689bc4b701e701448664aacc741e6d2_MD5.jpeg)

Our objective is to delete the user Carlos to do that at **stockApi** we will write
http://localhost/admin/delete?username=carlos

![](images/534ca760320348e7c732138800e0d363_MD5.jpeg)

We will send this request and by doing so it will solve the lab.

![](images/8c1900636381d6d7bad37b2ecbace0c3_MD5.jpeg)

![](images/49434c33fcf20c5414d34f9c0a80b772_MD5.jpeg)

