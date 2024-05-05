## Title: Importance of Encryption
## Details:
* difficulty: Medium
* category: Cryptography
* author: Sarmed
* flags: Flag{Good_Work}

## Description:
This is a medium difficulty lab that requires a keen eye for finding the flag that is encrypted using cryptographic algorithm. 

## Hint:
Read the Importance of Cryptography carefully.

## Intended Learning and outcome:
With the given challenge, I was able to learn how to use python to automate a repititive task and understanding modern day crytographic algorithm. 

## Solution: 
There are 2 files in this repository, the encrypted text one and the other one containing a passage on _Importance of Cryptography._ When we read the passage we notice 2 things, firstly, the passage contains some special symbols in place of letters and, secondly, the second paragraph is about AES 256. It's safe to assume that the text is encrypted in AES 256 but for decryption we require a password. We then proceed to extract all the special letters in the passage, we can do this through multiple ways, I'll show it through the python script using regex.

```python
import regex as re
string = #paste_passage_here
regex_pattern = r'[a-zA-Z0-9-,.;!\' ]'
non_matching_characters = [char for char in string if not re.match(regex_pattern, char)]
non_matching_string = ''.join(non_matching_characters)
print(non_matching_string)
```
We find this **ᎥժτʜêěɴɑɢᎻėᎥᏚᚱᏞᏞ** which would look like this in english **idTHeeNaGHeiSRLL**. We then use this secret and as the passage explains specifically about ECB 128bits, we use this cipher mode and keysize to decrypt the text.

........





