# TRAFFIC

### Question Statement
I was monitoring my network traffic and found some weird stuff someone was searching for some weird things on the internet.

> Author - Gurupreet Singh

 <a href="https://ctf.htbsrmist.tech/files/feb7edbbce3bcf208a145c5fa9a64e5a/TRAFFIC.pcapng?token=eyJ1c2VyX2lkIjo0NiwidGVhbV9pZCI6bnVsbCwiZmlsZV9pZCI6MTJ9.ZeOOZA.JL6dZCmeaTp85lweRsUQCHowVwQ">TRAFFIC.pcapng</a>


### Solution
The given file is a pcapng file. We shall use  <a href="https://apackets.com/upload">Apackets</a> to analyze the file online.
After the file is done uploading, we look at the HTTP Communication section

<a href="https://ibb.co/QNT4gJJ"><img src="https://i.ibb.co/tsv9GHH/chrome-q-Jnc-Equ-OYq.png" alt="chrome-q-Jnc-Equ-OYq" border="0"></a>

Here we look through the list and one of them looks interesting...

<a href="https://imgbb.com/"><img src="https://i.ibb.co/61VXFbb/chrome-ds-ZPBMc-U15.png" alt="chrome-ds-ZPBMc-U15" border="0"></a>

Going through this one we see a suspicious Username pattern:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/myc1Mch/chrome-n-HQ6p-COEi-Z.png" alt="chrome-n-HQ6p-COEi-Z" border="0"></a>

Joining all the 'User-Agent' strings together and putting them in the <a href="https://www.dcode.fr/cipher-identifier">Dcode Cipher Identifier</a> we see that its encrypted with ROT13. Decoding it we get:

<a href="https://ibb.co/N7TgrN5"><img src="https://i.ibb.co/M9Byf1r/chrome-IC77g-B8zk4.png" alt="chrome-IC77g-B8zk4" border="0"></a>

Hence we get our flag ```HTBSRMIST{Y0u_H4V3_4_KEEN_3ye_S1R}```

