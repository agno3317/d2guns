# Step 1
download guns.csv

# Step 2
copy the code from create table and paste it in the sql editor. Make sure that the file location leads to where the guns.csv folder is. 

# Step 3
Query! Suppose you are a new player and want to know which weapons drop from the moon, you would type

        Select * 
        From Guns
        Where gun_source = 'Moon';

Note: The Select statement specifies which columns you want returned in a query. In this case, we want to see all the columns, so we use * which means all.

The From statement specifies the table. We are working with the guns table so we just put guns. 

The where function acts as a filter within a column. In this query, we want to look for entries in the table where the gun source is the Moon.

# Step 4 
You can go even further!
Maybe you want to see the list of all the void hand cannons in the game.
you would type:

        Select * 
        From Guns
        where weapon type = 'hand_cannon'
        and gun_element = 'Void';

Note: The where function in SQL is case sensitive in some softwares (pgadmin looking at you). If you want to bypass that restriction, you can use the lower function which will convert all the characters in the column to lower case for the query
As an example, the previous query would be written as:

        Select * 
        From Guns
        where lower(weapon type) = 'hand_cannon'
        and lower(gun_element) = 'void';

Make sure that everything inside '' is in lowercase when using lower. 

That's all folks!

Update 7/12/2021: I have made an extended tutorial on how to normalize and make a view. If you are interested, go normalization_view.sql in main
