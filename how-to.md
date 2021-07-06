# Step 1
download guns.csv

# Step 2
copy the code from create table and paste it in the sql editor. Make sure that the file location leads to where the guns.csv folder is. 

# Step 3
Query! Suppose you are a new player and want to know which weapons drop from the moon, you would type

        Select * 
        From Guns
        Where gun_source = 'Moon';

Note: * just means all. Make sure that whatever you are looking for is within ''

# Step 4 
You can go even further!
Maybe you want to see the list of all the void hand cannons in the game.
you would type:

        Select * 
        From Guns
        where weapon type = 'hand_cannon'
        and gun_element = 'Void';

Note: The where function in SQL is case sensitive. If you want to bypass that restriction, you can use the lower function which will convert all the characters in the column to lower case for the query
As an example, the previous query would be written as:

        Select * 
        From Guns
        where lower(weapon type) = 'hand_cannon'
        and lower(gun_element) = 'void';

Make sure that everything inside '' is in lowecase when using lower. 

That's all folks!
