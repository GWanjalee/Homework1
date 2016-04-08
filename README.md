# Homework1
OverTheWire: Wargames - Bandit

The Bandit wargame is aimed at absolute beginners. It teaches the basics needed to be able to play other wargames.Like most other games, this game also contains several levels. We can start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level. While playing this game I got a good knowledge about linux commands.

Hints and commands given in the "OverTheWire" website was used as a guide to find the password for the next level.

Below it shows the levels which were completed by me.

Level 0

This was a simple challenge in which I had to log-in in via ssh to the target machine using the password "bandit0".

![0](https://cloud.githubusercontent.com/assets/18299123/14381501/83c118f0-fda4-11e5-8056-bc4466cc2672.PNG)

Level 0 - Level 1

Then read the level 1 password from the file readme on the home directory of level 0. The password in the file is for the bandit1 user which is the user for the level 1.

![0-1](https://cloud.githubusercontent.com/assets/18299123/14381502/83c13cae-fda4-11e5-9816-623c5dff325f.PNG)

Level 1 - Level 2

So in this level 1 there was a file called “-” in the home directory and it contains the password for the level 2.I used “./” to the absolute path of the file.

![1-2](https://cloud.githubusercontent.com/assets/18299123/14381503/83c13c68-fda4-11e5-8a57-79050c95a357.PNG)

Level 2 - Level 3

The password for the level 3 was stored in a file called "spaces" "in" "this" "filename" located in the home directory in level 2.As the above example I gave the path as "spaces\ in\ this\ filename".

![2-3](https://cloud.githubusercontent.com/assets/18299123/14381504/83c4a5b0-fda4-11e5-835b-f64556ab96a6.PNG)

Level 3 - Level 4

The password for the level 4 was stored in a hidden file in the inhere directory in level 3. For this challenge I added the “a” switch, it displayed all files including hidden files and by using “.” as part of the filename in Linux specifies that the file is a hidden file.

![3-4](https://cloud.githubusercontent.com/assets/18299123/14381500/83c070c6-fda4-11e5-9cb4-0f7f501a59f5.PNG)

Level 4 - Level 5

The password for the level 5 was stored in the only human-readable file in the inhere directory in level 4. Therefore with the file command I found that -file07 is the only file with ASCII text.

![4-5](https://cloud.githubusercontent.com/assets/18299123/14381505/83ccb5e8-fda4-11e5-8c3b-5fec4706ab49.PNG)

Level 5 - Level 6

The password for the level 6 was stored in a file somewhere under the inhere directory and has all of the following properties: human-readable, 1033 bytes in size, not executable. Here they told us the file containing the password is 1033 bytes, therefore I used the find command to find a file of a specific size.

![5-6](https://cloud.githubusercontent.com/assets/18299123/14381509/83e9b67a-fda4-11e5-84bb-f80647d0c123.PNG)

Level 6 - Level 7

The password for the level 7 was in a file somewhere on the server and have the following characteristics: owned by user bandit7, owned by group bandit6, 33 bytes in size.Therefore again I used the find command to find the password.

![6-7](https://cloud.githubusercontent.com/assets/18299123/14381508/83e938c6-fda4-11e5-99aa-186bcf5462b9.PNG)

Level 7 - Level 8

the password for the level 8 was in the file called “data.txt” which was next to the word “millionth”, time to pipe the output from cat of the file into grep searching for “millionth”.

![7-8](https://cloud.githubusercontent.com/assets/18299123/14381506/83e800f0-fda4-11e5-96b2-63def317e331.PNG)

Level 8 - Level 9

The goal was to the find the password instead the file “data.txt”, the password line only occurs once in the file. Therefore here I used the command “sort” and then pipe the output from sort into the command “uniq” with the switch operator “-u” to find the unique string.

![8-9](https://cloud.githubusercontent.com/assets/18299123/14381507/83e93286-fda4-11e5-9f31-a6f92376a7e2.PNG)

Level 9 - Level 10

The password for the level 10 was stored within the file called “data.txt” which contains only a few lines of human-readable strings starting with the character “=”.For this I used the “strings” command and pipe the output to grep searching for the “=” character.

![9-10](https://cloud.githubusercontent.com/assets/18299123/14381510/83ece8a4-fda4-11e5-87a0-d104e76d09a1.PNG)

Level 10 - Level 11

The password for the level 11 was stored in the file “data.txt” which contains base64 encoded data. For this I used the “base64” command in Linux to decode the string.

![10-11](https://cloud.githubusercontent.com/assets/18299123/14381514/841a5fbe-fda4-11e5-92f7-90e0c4370a61.PNG)

Level 11 - Level 12

The password was stored in the data.txt file and all lowercase and uppercase letters have been rotated by 13 potions. for this one, using the "tr" command I was able to reverse it.

![11-12](https://cloud.githubusercontent.com/assets/18299123/14381516/841c2a1a-fda4-11e5-983e-a53ae2c23ce5.PNG)

Level 12 - Level 13

The goal for this challenge was to read the file data.txt file which contains a hexdump of a file that has been compressed several times. It was suggested for this level to make a directory in the /tmp directory to work in and copy the hexdump file to this location. After that I used "xxd" command, which allows to turn hex data into a binary file, by doing this I would be able to convert the hex data in the “data.txt” file into the binary file it represented.Next I used zcat to decompress the file.After that using bzip I decompressed to the next level.After decompressing the gzip file I was give a tar archive.Unpacking the two tar archives I found another bzip archive, using the same method before I decompressed the bzip archive.Again repeat the earlier step for unpacking tar archives for this new file.Again using zcat I decompressed the file.

![12](https://cloud.githubusercontent.com/assets/18299123/14381512/8419e99e-fda4-11e5-9cb8-ae192d7ed1e6.PNG)
![13](https://cloud.githubusercontent.com/assets/18299123/14381515/841a9092-fda4-11e5-9cdc-4a80bbe68c80.PNG)

Level 13 - Level 14

The goal for this level was to get to the password which is located in “/etc/bandit_pass/bandit14” which can only be read by the user bandit14. 

![14](https://cloud.githubusercontent.com/assets/18299123/14381517/842d8562-fda4-11e5-98a2-955a5c27614d.PNG)
![13-14](https://cloud.githubusercontent.com/assets/18299123/14381513/8419c554-fda4-11e5-849e-32ff7beb5c9c.PNG)

Level 14 - Level 15

The goal for this level was to connect to port 30,000 on the localhost and submit the password for the current level which if correct will return the password for the next level. Here I used the "Netcat" command.

![14-15](https://cloud.githubusercontent.com/assets/18299123/14381521/84421cca-fda4-11e5-9c28-883ca42a7f0a.PNG)

Level 15 - Level 16

This level had the same challenge which was in level 14 but this time SSL encryption has been added into the mix.I was a bit puzzled at this staged as I thought I had done everything right and so I was expected to get the password for the bandit16 user, eventually I went back to the webpage for this level to see if I had missed anything, which I had. I missed the hint “Helpful note: Getting “HEARTBEATING” and “Read R BLOCK”? Use -quiet and read the “CONNECTED COMMANDS” section in the manpage. Next to ‘R’ and ‘Q’, the ‘B’ command also works in this version of that command…“, so I ran the same command again but included the -quiet switch in my command to execute.

![15](https://cloud.githubusercontent.com/assets/18299123/14381520/84421982-fda4-11e5-8f3a-cf3f16070828.PNG)
![15-16](https://cloud.githubusercontent.com/assets/18299123/14381518/84408ab8-fda4-11e5-8c5f-8ac6d8f25591.PNG)

Level 16 - Level 17

the goal of this level built on the previous challenge, we have to preform the same action as before but this time we don’t know the actual port to connect to but instead we know the port to connect to lies within the port range of 31000 to 32000, using nmap we can quickly identify the port we need.From the nmap scan I found that there are 5 listening ports within range of ports from 31000 to 32000 but only one of these ports support SSL encryption.Then I tested all the ports, eventually I found the correct port to be 31790 and when I entered the password for the current level I was given a private key, then I used the private key to connect to server with the user bandit17 and the ssh private key.

![17](https://cloud.githubusercontent.com/assets/18299123/14381522/8444df8c-fda4-11e5-8938-90d18d047528.PNG)
![17-16](https://cloud.githubusercontent.com/assets/18299123/14381523/845f79c8-fda4-11e5-96be-1a7dfd154ecc.PNG)

Problems occured - 

ssh doesn't support to the university WIFI-because Sssh is affect to internal servers.

After completing the 17th level, it didn't show me any password which I needed for the level 18.
