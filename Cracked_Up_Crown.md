# Cracked up Crown

### Question Statement
I thought giving you guys a jigsaw puzzle would be a nice idea :) Dont worry you will figure it out, you have time till 1 March

> Author - Jayesh Gaba

 <a href="https://ctf.htbsrmist.tech/files/01196d065b4b47ebe146a5f16ea3fd66/puzzle.jpg?token=eyJ1c2VyX2lkIjo0NiwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6Nn0.ZeOZrA.tiJH34i5C3peYtMHQ0lt081hdRI">puzzle.jpg</a>

### Solution
We are given an image which is divided into several square pieces like a jigsaw. We use a tool called  <a href="https://github.com/nemanja-m/gaps">Gaps</a> to analyze and reconstruct the image.

Ill be showing this process on linux but it's completely doable on all platforms.

After cloning the Gaps repo and setting it up, we run the following command that analyzes and reconstructs the image and saves the out put as answer.jpg:

<a href="https://ibb.co/Xtwcvmj"><img src="https://i.ibb.co/tDdVWyQ/Virtual-Box-VM-5-AIDd-Ak-XBe.png" alt="Virtual-Box-VM-5-AIDd-Ak-XBe" border="0"></a>

On opening the answer.jpg file, we see two QR codes in the image:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/Wck30b7/Virtual-Box-VM-FGxx-Kl66d0.png" alt="Virtual-Box-VM-FGxx-Kl66d0" border="0"></a>

On scanning these QR Codes we get:

<a href="https://ibb.co/d4fgLhX"><img src="https://i.ibb.co/Mkg6GXK/Whats-App-Image-2024-03-03-at-3-03-57-AM.jpg" alt="Whats-App-Image-2024-03-03-at-3-03-57-AM" border="0"></a>
<a href="https://ibb.co/h2gdnhm"><img src="https://i.ibb.co/bN6vyqK/Whats-App-Image-2024-03-03-at-3-04-04-AM.jpg" alt="Whats-App-Image-2024-03-03-at-3-04-04-AM" border="0"></a><br />

Hence we get our flag: ```HTBSRMIST{puzzl25_4r3_fun_0r_m4yb3_n0t_h3h}```
