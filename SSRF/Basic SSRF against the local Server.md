# This lab has a stock check feature which fetches data from an internal system.

To solve the lab, change the stock check URL to access the admin interface at http://localhost/admin and delete the user carlos.

After starting the lab we go to the stock change feature and capture the request using burpsuite

[[Labs/SSRF/images/71f747fda1063f4e34a5d3cf9c7da4f8_MD5.jpeg|Open: Pasted image 20250130223754.png]]
![[Labs/SSRF/images/71f747fda1063f4e34a5d3cf9c7da4f8_MD5.jpeg]]

We send the request to Repeater then at stockApi we paste http://localhost/admin

[[Labs/SSRF/images/eb35045b5c3828c17d06524e6ddf6d4f_MD5.jpeg|Open: Pasted image 20250130224017.png]]
![[Labs/SSRF/images/eb35045b5c3828c17d06524e6ddf6d4f_MD5.jpeg]]

then we send the request
[[Labs/SSRF/images/ddf76d8d6b90a4903c49ee7bbe7cea5f_MD5.jpeg|Open: Pasted image 20250130224137.png]]
![[Labs/SSRF/images/ddf76d8d6b90a4903c49ee7bbe7cea5f_MD5.jpeg]]

Now we will delete the user Carlos to do that at **stockApi** we will use this
url:http://localhost/admin/delete?username=carlos

[[Labs/SSRF/images/bba4f3e5cfa4537c88d22491b608cafd_MD5.jpeg|Open: Pasted image 20250130224412.png]]
![[Labs/SSRF/images/bba4f3e5cfa4537c88d22491b608cafd_MD5.jpeg]]

Now we send the request and it will solve the lab

[[Labs/SSRF/images/0669c0fe7d4a4e8ce9d5832b19b146ff_MD5.jpeg|Open: Pasted image 20250130224546.png]]
![[Labs/SSRF/images/0669c0fe7d4a4e8ce9d5832b19b146ff_MD5.jpeg]]


[[Labs/SSRF/images/9c90bc3a3b4fb1455aef8c45702ced34_MD5.jpeg|Open: Pasted image 20250130224608.png]]
![[Labs/SSRF/images/9c90bc3a3b4fb1455aef8c45702ced34_MD5.jpeg]]
