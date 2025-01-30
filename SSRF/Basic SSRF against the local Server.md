# This lab has a stock check feature which fetches data from an internal system.

To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

After starting the lab we go to the stock change feature and capture the request using burpsuite

![[Labs/SSRF/images/6431effda94b18955eafaeab181fccf5_MD5.jpeg]]

We send the request to Repeater then at **stockApi** we paste http://localhost/admin

![[Labs/SSRF/images/84c4fd4698f43a56e4d5eb9266d136a4_MD5.jpeg]]

then we send the request

![[Labs/SSRF/images/6689bc4b701e701448664aacc741e6d2_MD5.jpeg]]

Now we will delete the user Carlos to do that at **stockApi** we will use this
url:http://localhost/admin/delete?username=carlos

[[Labs/SSRF/images/bba4f3e5cfa4537c88d22491b608cafd_MD5.jpeg|Open: Pasted image 20250130224412.png]]
![[Labs/SSRF/images/bba4f3e5cfa4537c88d22491b608cafd_MD5.jpeg]]

Now we send the request and it will solve the lab

![[Labs/SSRF/images/8c1900636381d6d7bad37b2ecbace0c3_MD5.jpeg]]


![[Labs/SSRF/images/49434c33fcf20c5414d34f9c0a80b772_MD5.jpeg]]
