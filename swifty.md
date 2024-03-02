# swifty

### Question Statement
During the 100 BC, There was a queen named Taylor and her kingdom was called swifty. The swifties always had the desire to take over the world using their unimaginable intelligence. You need to stop this evil. Adonis, the ruler of the neighbouring kingdom wants you to decode the message which was being carried to the swifties via a pig

VkdoaGJtdGZlVzkxWDJZd2NsOXpZWFl6YVc1blgyUmZkMjl5YkdRJg==

flag_format = HTBSRMIST{flag_here}

### Solution
We put the given code in <a href="https://www.dcode.fr/cipher-identifier">Dcode Cipher Identifier</a> and find that its a Base64 cipher.
Decoding it once gives us the following output:

<a href="https://imgbb.com/"><img src="https://i.ibb.co/g6pPWmc/chrome-amn-UBPa39-A.png" alt="chrome-amn-UBPa39-A" border="0"></a>

This output doesnt make much sense. We copy this output into the Base64 decoder and decode it again to get the following output:

![image](https://github.com/PYTRanger/HTBSRMIST_Recruitment_CTF_Writeup/assets/51047021/0ebd9447-c39a-4b5e-95d1-4255e9cf8a08)

Hence we have our flag ```HTBSRMIST{Thank_you_f0r_sav3ing_d_world}```
