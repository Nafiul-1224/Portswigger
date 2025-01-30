This lab has a stock check feature which fetches data from an internal system.

To solve the lab, use the stock check functionality to scan the internal `192.168.0.X`range for an admin interface on port `8080`, then use it to delete the user `carlos`.

After starting the lab we go to the stock change feature and capture the request using burpsuite.

![](images/f766f8556b760d618270238d48ff376c_MD5.jpeg)

After capturing it we send the request to intruder 

![](images/8f8a6e89600eea413c59cec7debdfcf4_MD5.jpeg)

At **StockApi** we will write http://192.168.0.1:8080/admin (url encoded) then set a payload to the last digit of ip address

![](images/79351208bfac04e210f0471ea9a2d921_MD5.jpeg)

then we will go to the payloads section to configure our payload like the image given below

![](images/c91629221606deb1708b3afe65216e5e_MD5.jpeg)

after this we will click on start attack and look for status code 200

![](images/9571c97e0725444e689650cfa66a64f8_MD5.jpeg)

After selecting the request with 200 status code right click and select **show response in browser**

![](images/5df6ac5a9a3dd4c94c9b9a17db570b41_MD5.jpeg)

Copy the url and paste it on the browser and you will see this

![](images/4186f40b07a316032dfff15a663d3cb3_MD5.jpeg)

All of these to find the right internal IP address which is for our case is **192.168.0.192**

Now we will go back to our Intruder attack and from the request we will send it to repeater then we will go to to response and there we will see delete account option for carlos

![](images/fb5961a21ab8269eafde2089325765dd_MD5.jpeg)

We will use this Carlos delete accont url in the request we send to repeater which is
http://192.168.0.192:8080/admin/delete?username=carlos and also url encode it

![](images/20e1f8782765b88d011fe4a7c59272d4_MD5.jpeg)

Now we send the request and by doing that it will solve the lab.

![](images/c5f45c13750e44977b6faa93d5eff8e1_MD5.jpeg)

![](images/71b3956ce070689ea1292b060fbd923a_MD5.jpeg)



