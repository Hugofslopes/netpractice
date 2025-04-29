<html>
  <p align="center">
      <img src="https://www.42porto.com/wp-content/uploads/2024/08/42-Porto-Horizontal.png" alt="Pipex Image" />
  </p>
  <h1 align="center">netpractice</h1>
  <p align="center">
      <img src="https://github.com/user-attachments/assets/67bf6472-92d7-4e7d-8c7a-f10111bc6e28" width="165" alt="Image" />
  </p>

  <style>
      #top {
            position: absolute;
            top: 0;
        }
    </style>

On this project we learn how to manage some networks given different ­interfaces such as routers, computers and Switch. 
I use this videos to learn the basics of IP adress and subnetting : https://youtube.com/playlist?list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&feature=shared. 

<details>
    <summary>Level 1</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/ee9041a6-5be1-42ca-b4bf-188159af3b29" alt="level1"><br>
    - host b and host a are on the same network. Since the IP for B1 is 104.96.23.12 and the sub-net mask is 255.255.255.0 I have 252 IP available. From 104.96.23.1 to 104.96.23.254.<br>
    - host d and host c are on the same network. Since the IP for C1  is 211.191.234.75 and the sub-net mask is 255.255.0.0 we have 503 IP available.
    <div align="center">
      <b><a href="#top">↥ back to top</a></b>
    </div>
    </br>
</details>

---

## Level 2
- host B and host A are on the same network. This network as 28 IP addresses since its mask is 255.255.255.224. So it as from 192.168.82.193 up to 192.168.82.222.
-host D and host C are on the same network that has only 3 IP addresses available. Since we can’t use 0 we got the 1 and 2.

## Level 3
- Host B, Host A and Host C are on the same network thanks to the switch. We keep the same sub-net mask since they are on the same network. Than we have a range of 124 IP available. From 104.198.102.1 to 104.198.102.126.

## Level 4
- We got R2 that as the IP from 0 to 127. Then we got R3 that as 63 IP reserved (192 up to 255). So we got the range from 128 up to 190 for our network. If we use and mask of 255.255.255.192 we got 63 IP available. I choose the lowest one and the top one to show the range.

## Level 5
- This exercise introduces routing tables, they exist for the router to know where to send some package when it receives some IP address.  On the left of the routing table you got the destination and then on the right you have the next hop. The routing table on the top of the screen needs to know where to send data so in there we say that the next hop is 147.139.35.254 like it was already defined. The IP of B1 has a range of 253 that can be used, from 1 up to 254.
On interface A1 we have an range of 126 IP addresses, from 1 up to 126, since our mask  is 128. 
The routing table on the Host A  does exactly the same as the one on the top , but on this case the next hop is R1 35.6.186.126.

## Level 6
- This exercise introduces the internet. In this case we need to connect host A to internet. Starting form the right to left the rout table needs to send to the next hop, which in this case is R1. On this case I selected the IP of R1 65.126.186.226 but as the sub-net mask shows I have one range of 124 IP. On the internet I just update the routing table put that the destination of anything that goes to R2 is the range of IP that I got one R1 and A1.

## Level 7
­ There are a lot of different ways to do this exercise but we need to keep in mind that we have three different networks. I choose every mask to be 255.255.255.252 because each network only needs 2 IP addresses so no need to reserve more. I use similar IP but they are on different networks. I could have on R22 50.50.50.1, on C1 50.50.50.2 and on its routing table 50.50.50.1 it would work the same. 

## Level 8
- I start this one with the internet. The exercise already gave me the destination I only need to put the next hop (the host) which is 163.86.250.12. Then I fill R13 which is already defined on the R2 routing table. I put R21 that will be on the same network as R13. Then I can fill the R1 that will have R21 has host and all the IP from R22 and R33 as destination. Then I got to R23 which already as its mask and in this case I have from 129.70.143.1 to 129.70.143.14, and I choose one IP from this range. On the other side its all empty so I choose the next range that I will have from 16 to 18, again 255.255.255.252 as sub-net because I only need to IP on this.

## Level 9
- This exercise has 4 different networks. I start with B1, R11 and A1. This network as 124 IP available but in this case I choose only 3 IP that are next to each other. We have to define routing tables same as we did on previous exercises. Note that on my internet routing table I use 1.1.1.0/29 which got us 6 addresses, which is the minimum for what we need. On C1 and R22 I have one other network with only two IP addresses. I only need to refer them on internet routing table. I use this mask 3.3.3.0/30 because I only got 2 IP on this network. R13 and R21 are on the same network and have already a sub-net mask that only has 2 IP, do you can choose any range of two consecutive IP. For R23 is already defined on host D routing table. Then we can see that the sub-net mask if /18 which give us a big range of valid IP.

## Level 10
- I start from the right top corner which I already have the IP for H11. I use the sub-net mask from R11 for H21 and H11. Then I go to the Internet on the left corner which I need to have has destination all the IP on the 169.237.48.0 range. The R13  sub-net mask is the same as R21. The IP for R23 is already defined on the H4 routing table. Then I just use the mask from H41. For R22 and R31  I use 193 and 194. On R11 I have 128 IP reserved 0 to 127 . Then I Have 63 IP reserved on H41 128 to 191. The other range available will start on 193 (since we can not use the 192).
</html>