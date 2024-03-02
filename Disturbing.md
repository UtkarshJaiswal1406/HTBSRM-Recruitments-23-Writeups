# Disturbing

### Question Statement
While going through my file system i found a zip file which was encrypted. Though i know some basic knowledge of hashing and encryption. But i can not crack this file. Can you please help me out?

> Author - Devansh Gupta

 <a href="https://ctf.htbsrmist.tech/files/ca870dadc0248715071a4666bbbf6992/disturb.zip?token=eyJ1c2VyX2lkIjo0NiwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6M30.ZeOJWQ.97jXPwhByewhEWJ2nlJXYFzeiyE">disturb.zip</a>

### Solution
Downloading and looking at the zip file we see that it's password-protected. Hence we need to crack the password.

I'll demonstrating how to do this process on linux. This can definetely still be done in Mac and Windows systems as well.

First we use  <a href="https://github.com/openwall/john/blob/bleeding-jumbo/src/zip2john.c">Zip2John</a> to create a hashes file for the zip.

<a href="https://ibb.co/TkkNyKf"><img src="https://i.ibb.co/t441RZG/Virtual-Box-VM-z-St5x7m9m-D.png" alt="Virtual-Box-VM-z-St5x7m9m-D" border="0"></a>

Then we use  <a href="https://github.com/openwall/john/tree/bleeding-jumbo">JohnTheRipper</a> to crack the password using the standard rockyou.txt wordlist and save the answers to a file password.txt.

<a href="https://ibb.co/12h3CgH"><img src="https://i.ibb.co/KyRYtPC/Virtual-Box-VM-e-Kc-Cx-L1bc-K.png" alt="Virtual-Box-VM-e-Kc-Cx-L1bc-K" border="0"></a>

Reading the contents of the password.txt file, we get:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/jyX6ymR/Virtual-Box-VM-80e-Ajc-BHx-Y.png" alt="Virtual-Box-VM-80e-Ajc-BHx-Y" border="0"></a>

We see that we have successfully cracked the password of the pdf which is ```1fukuhack```

using this password we unzip the file:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/Br4rDty/Virtual-Box-VM-9-FVm7g-JICp.png" alt="Virtual-Box-VM-9-FVm7g-JICp" border="0"></a>

Now reading the contents of the extracted pdf, we see:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/QXbrVnL/Virtual-Box-VM-N9zo-Nb-Nb-Yb.png" alt="Virtual-Box-VM-N9zo-Nb-Nb-Yb" border="0"></a>

The flag seems to be encrypted using some sort of a cipher. Using <a href="https://www.dcode.fr/cipher-identifier">Dcode Cipher Identifier</a> we see that the cipher is Rot47.
Decoding this code we get:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/M8KCsTD/chrome-b-Jo-Pzm-S1t-I.png" alt="chrome-b-Jo-Pzm-S1t-I" border="0"></a>

Hence we get our flag ```HTBSRMIST{g00d_j0b}```




