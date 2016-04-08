# Homework1
OverTheWire: Wargames - Bandit

The Bandit wargame is aimed at absolute beginners. It will teach the basics needed to be able to play other wargames.This game, like most other games, is organised in levels. We can start at Level 0 and try to “beat” or “finish” it. Finishing a level results in information on how to start the next level. While playing this game I got a good knowledge about linux.

Hints and commands given in the OverTheWire website was used as a guide to find the password fro the next level.

Level 0

This was a simple challenge in which I had to log-in in via ssh to the target machine using the password "bandit0".

![0](https://cloud.githubusercontent.com/assets/18299123/14381501/83c118f0-fda4-11e5-8056-bc4466cc2672.PNG)

Level 0 - Level 1

Then read the level 1 password from the file readme on the home directory of level 0. The password in the file is for the bandit1 user which is the user for the level 1.

![0-1](https://cloud.githubusercontent.com/assets/18299123/14381502/83c13cae-fda4-11e5-9816-623c5dff325f.PNG)

Level 1 - Level 2

So in this level 1 there is a file called “-” in the home directory and it contains the password for the level 2.I used “./” to the absolute path of the file.

![1-2](https://cloud.githubusercontent.com/assets/18299123/14381503/83c13c68-fda4-11e5-8a57-79050c95a357.PNG)

Level 2 - Level 3

The password for the level 3 is stored in a file called "spaces" "in" "this" "filename" located in the home directory in level 2.As the above example I gave the path as "spaces\ in\ this\ filename".

![2-3](https://cloud.githubusercontent.com/assets/18299123/14381504/83c4a5b0-fda4-11e5-835b-f64556ab96a6.PNG)

Level 3 - Level 4

The password for the level 4 was stored in a hidden file in the inhere directory in level 3. For this challenge I added the “a” switch, it displayed all files including hidden files and by using “.” as part of the filename in Linux specifies that the file is a hidden file.

![3-4](https://cloud.githubusercontent.com/assets/18299123/14381500/83c070c6-fda4-11e5-9cb4-0f7f501a59f5.PNG)

Level 4 - Level 5

The password for the level 5 is stored in the only human-readable file in the inhere directory in level 4. Therefore with the file command I found that -file07 is the only file with ASCII text.

![4-5](https://cloud.githubusercontent.com/assets/18299123/14381505/83ccb5e8-fda4-11e5-8c3b-5fec4706ab49.PNG)

Level 5 - Level 6

The password for the level 6 is stored in a file somewhere under the inhere directory and has all of the following properties: human-readable, 1033 bytes in size, not executable. Here they told us the file containing the password is 1033 bytes, therefore I used the find command to find a file of a specific size.

![5-6](https://cloud.githubusercontent.com/assets/18299123/14381509/83e9b67a-fda4-11e5-84bb-f80647d0c123.PNG)

Level 6 - Level 7

The password for the level 7 was in a file somewhere on the server and have the following characteristics:

owned by user bandit7
owned by group bandit6
33 bytes in size
Therefore again I used the find command to find the password.

![6-7](https://cloud.githubusercontent.com/assets/18299123/14381508/83e938c6-fda4-11e5-99aa-186bcf5462b9.PNG)

Level 7 - Level 8

the password for the level 8 was in the file called “data.txt” which was next to the word “millionth”, time to pipe the output from cat of the file into grep searching for “millionth”.

![7-8](https://cloud.githubusercontent.com/assets/18299123/14381506/83e800f0-fda4-11e5-96b2-63def317e331.PNG)



![8-9](https://cloud.githubusercontent.com/assets/18299123/14381507/83e93286-fda4-11e5-9f31-a6f92376a7e2.PNG)
![9-10](https://cloud.githubusercontent.com/assets/18299123/14381510/83ece8a4-fda4-11e5-87a0-d104e76d09a1.PNG)
![10](https://cloud.githubusercontent.com/assets/18299123/14381511/83fb6b22-fda4-11e5-8dc7-acdb43681b70.PNG)
![10-11](https://cloud.githubusercontent.com/assets/18299123/14381514/841a5fbe-fda4-11e5-92f7-90e0c4370a61.PNG)
![11-12](https://cloud.githubusercontent.com/assets/18299123/14381516/841c2a1a-fda4-11e5-983e-a53ae2c23ce5.PNG)
![12](https://cloud.githubusercontent.com/assets/18299123/14381512/8419e99e-fda4-11e5-9cb8-ae192d7ed1e6.PNG)
![13](https://cloud.githubusercontent.com/assets/18299123/14381515/841a9092-fda4-11e5-9cdc-4a80bbe68c80.PNG)
![13-14](https://cloud.githubusercontent.com/assets/18299123/14381513/8419c554-fda4-11e5-849e-32ff7beb5c9c.PNG)
![14](https://cloud.githubusercontent.com/assets/18299123/14381517/842d8562-fda4-11e5-98a2-955a5c27614d.PNG)
![14-15](https://cloud.githubusercontent.com/assets/18299123/14381521/84421cca-fda4-11e5-9c28-883ca42a7f0a.PNG)
![15](https://cloud.githubusercontent.com/assets/18299123/14381520/84421982-fda4-11e5-8f3a-cf3f16070828.PNG)
![15-16](https://cloud.githubusercontent.com/assets/18299123/14381518/84408ab8-fda4-11e5-8c5f-8ac6d8f25591.PNG)
![16](https://cloud.githubusercontent.com/assets/18299123/14381519/8441209a-fda4-11e5-8685-708cea8728ab.PNG)
![17](https://cloud.githubusercontent.com/assets/18299123/14381522/8444df8c-fda4-11e5-8938-90d18d047528.PNG)
![17-16](https://cloud.githubusercontent.com/assets/18299123/14381523/845f79c8-fda4-11e5-96be-1a7dfd154ecc.PNG)
