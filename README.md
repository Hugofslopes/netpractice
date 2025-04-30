<html>
  <p align="center">
      <img src="https://www.42porto.com/wp-content/uploads/2024/08/42-Porto-Horizontal.png" alt="Pipex Image" />
  </p>
  <h1 align="center">netpractice</h1>
  <p align="center">
      <img src="https://github.com/user-attachments/assets/67bf6472-92d7-4e7d-8c7a-f10111bc6e28" alt="Image" />
  </p>

On this project we learn how to manage some networks given different interfaces such as routers, computers, and switches.<br> 

I use these videos to learn the basics of IP addresses and subnetting: [YouTube Playlist](https://youtube.com/playlist?list=PLIhvC56v63IKrRHh3gvZZBAGvsvOhwrRF&feature=shared). 

<details>
    <summary>Level 1</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/ee9041a6-5be1-42ca-b4bf-188159af3b29" alt="level1"><br>
    - <b>Host B</b> and <b>Host</b> A are on the same network. Since the IP for <b>B1</b> is 104.96.23.12 and the subnet mask is 255.255.255.0, I have 252 IPs available, from 104.96.23.1 to 104.96.23.254.<br>
    - <b>Host D</b> and <b>Host C</b> are on the same network. Since the IP for <b>C1</b> is 211.191.234.75 and the subnet mask is 255.255.0.0, we have 65,534 IPs available.<br>
</details>

<details>
    <summary>Level 2</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/8adb21a8-59df-4311-a02c-8a35aadc43f1" alt="level1"><br>
    - <b>Host B</b> and <b>host A</b> are on the same network. This network as 28 IP addresses since its mask is 255.255.255.224. So it as from 192.168.82.193 up to 192.168.82.222.<br>
    - <b>Host D</b> and <b>Host C</b> are on the same network that has only 3 IP addresses available. Since we can’t use 0 we got the 1 and 2.<br>
</details>

<details>
    <summary>Level 3</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/d5e5c813-2a00-469c-ab8a-301aa41117b3" alt="level1"><br>
    - <b>Host B</b>, <b>Host A</b> and Host C are on the same network thanks to the switch. We keep the same sub-net mask since they are on the same network. Than we have a range of 124 IP available. From 104.198.102.1 to 104.198.102.126.<br>
</details>

<details>
    <summary>Level 4</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/6860ece4-dc4b-4b97-b86e-c9eaf3fbc69e" alt="level1"><br>
    - We got <b>R2</b> that as the IP from 0 to 127. Then we got <b>R3</b> that as 63 IP reserved (192 up to 255). So we got the range from 128 up to 190 for our network. If we use and mask of 255.255.255.192 we got 63 IP available. I choose the lowest one and the top one to show the range.<br>
</details>

<details>
    <summary>Level 5</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/69b3e6ca-a5e3-4867-8479-534a8f02c749" alt="level1"><br>
    - This exercise introduces routing tables, they exist for the router to know where to send some package when it receives some IP address.  On the left of the routing table you got the destination and then on the right you have the next hop. The routing table on the top of the screen needs to know where to send data so in there we say that the next hop is 147.139.35.254 like it was already defined. The IP of <b>B1</b> has a range of 253 that can be used, from 1 up to 254.
On interface <b>A1</b> we have an range of 126 IP addresses, from 1 up to 126, since our mask  is 128. 
The routing table on the <b>Host A</b>  does exactly the same as the one on the top , but on this case the next hop is </>R1</b> 35.6.186.126.<br>
</details>

<details>
    <summary>Level 6</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/731cd810-6ef7-4544-b8b4-d73ef6829b07" alt="level1"><br>
    - This exercise introduces the internet. In this case we need to connect <b>host A</b> to internet. Starting form the right to left the rout table needs to send to the next hop, which in this case is <b>R1</b>. On this case I selected the IP of <b>R1</b> 65.126.186.226 but as the sub-net mask shows I have one range of 124 IP. On the internet I just update the routing table put that the destination of anything that goes to <b>R2</b> is the range of IP that I got one <b>R1</b> and <b>A1</b>.<br>
</details>

<details>
    <summary>Level 7</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/c53b0ef0-d6f1-45d6-8ce1-6c245fd56482" alt="level1"><br>
    There are a lot of different ways to do this exercise but we need to keep in mind that we have three different networks. I choose every mask to be 255.255.255.252 because each network only needs 2 IP addresses so no need to reserve more. I use similar IP but they are on different networks. I could have on <b>R22</b> 50.50.50.1, on <b>C1</b> 50.50.50.2 and on its routing table 50.50.50.1 it would work the same.<br>
</details>

<details>
    <summary>Level 8</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/19317d44-5eb7-440d-84a3-02fc4b1df6bc" alt="level1"><br>
    I start this one with the internet. The exercise already gave me the destination I only need to put the next hop (the host) which is 163.86.250.12. Then I fill <b>R13</b> which is already defined on the <b>R2</b> routing table. I put <b>R21</b> that will be on the same network as <b>R13</b>. Then I can fill the R1 that will have <b>R21</b> has host and all the IP from <b>R22</b> and <b>R33</b> as destination. Then I got to <b>R23</b> which already as its mask and in this case I have from 129.70.143.1 to 129.70.143.14, and I choose one IP from this range. On the other side its all empty so I choose the next range that I will have from 16 to 18, again 255.255.255.252 as sub-net because I only need to IP on this<br>
</details>

<details>
    <summary>Level 9</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/98c040b8-1066-4f95-ba60-727a085668fd" alt="level1"><br>
   - This exercise has 4 different networks. I start with <b>B1</b>, <b>R11</b> and <b>A1</b>. This network as 124 IP available but in this case I choose only 3 IP that are next to each other. We have to define routing tables same as we did on previous exercises. Note that on my internet routing table I use 1.1.1.0/29 which got us 6 addresses, which is the minimum for what we need. On <b>C1</b> and <b>R22</b> I have one other network with only two IP addresses. I only need to refer them on internet routing table. I use this mask 3.3.3.0/30 because I only got 2 IP on this network. <b>R13</b> and <b>R21</b> are on the same network and have already a sub-net mask that only has 2 IP, do you can choose any range of two consecutive IP. For <b>R23</b> is already defined on <b>host D</b> routing table. Then we can see that the sub-net mask if /18 which give us a big range of valid IP.<br>
</details>

<details>
    <summary>Level 10</summary>
    <br>
    <img src="https://github.com/user-attachments/assets/3e7a71f1-3f65-4066-94f8-a8d00b05e2b1" alt="level1"><br>
   - I start from the right top corner which I already have the IP for <b>H11</b>. I use the sub-net mask from <b>R11</b> for <b>H21</b> and <b>H11</b>. Then I go to the Internet on the left corner which I need to have has destination all the IP on the 169.237.48.0 range. The <b>R13</b>  sub-net mask is the same as <b>R21</b>. The IP for <b>R23</b> is already defined on the <b>H4</b> routing table. Then I just use the mask from <b>H41</b>. For <b>R22</b> and <b>R31</b> I use 193 and 194. On <b>R11</b> I have 128 IP reserved 0 to 127 . Then I Have 63 IP reserved on <b>H41</b> 128 to 191. The other range available will start on 193 (since we can not use the 192).<br>
</details>
</html>
