# 100 Days Of Code - Log

### Day 0: June 21, 2021

**Today's Progress**: Removed secrets hard-coded in my discord bot (so bad I know!) and replaced it with a proper Azure KeyVault reference.

**Thoughts:** Although using the Azure Key Vault is a good step in the right direction, the end goal will be to work on a pipeline that will handle the secrets, so credentials no longer have to be cached when running the program. I'm currently using VisualStudioCredentials() to grab the creds from my working instance of VScode. 

**Link to work:** No link, since it's a private repo, but maybe a link to the discord bot's website in the future. Maybe part of this will be it's front end site??

### Day 1: June 22, 2021

**Today's Progress**: Finished removing the last of my secrets (mine!) and started on bot command logic. 

**Thoughts:** No more db string in the code, which is great. I was able to modify some of the character class definitions, so I can get more information the db models. I worked on "attacking the enemy" commands that will allow characters to attack monsters with the character they created. I created a very rough system to keep track of the 'state' of the mob and to let people know it's dead if someone kills it off. I am falling in love with functional programming. I am using it to return the best spells a user has at their current level.  

**Link to work:** Still no link :). Access upon request, or maybe you can add it to your discord server one of these days! It needs a website, I know...

### Day 2: June 23, 2021

**Today's Progress**: Finished the attack command for mly discord bot. I created a weapon model and migration for the "dropping" of items by monsters

**Thoughts:** I have no idea how I'm going to create a bag system, and how that will play with data in the PostgresDB. I'm thinking when a monster dies and it "drops" it's items those items will be copied and stored in some type of array or list in the database, associated with the user's character? Not sure if there is a way to point to the records in the table without deleting the records when the item is moved from their bag. I just need a system of pointers...?

**Link to work:** Still no link :). Access upon request, or maybe you can add it to your discord server one of these days! It needs a website, I know...

### Day 3: June 26, 2021

**Today's Progress**: Implemented a bag table and model for my discord bot

**Thoughts:** Lots of work tomorrow to get this bag log set up for the character. Also need to work on populating the weapons bag with some type of script. It would be cool if I could pull in all of the weapons from some existing weapons database. I could then populate my own rarity and stat values.

**Link to work:** Still no link :). Access upon request, or maybe you can add it to your discord server one of these days! It needs a website, I know...

### Day 4: June 27, 2021

**Today's Progress**: Implemented drop system for killing mobs

**Thoughts:** didn't get to the bag implementation, due to fighting over relationship queries. I was able to get the drop system in place, so mobs drop a random item depending on a "roll". If the roll is past a certain threshold the chance to get rarer items increases.

**Link to work:** Still no link :). Access upon request, or maybe you can add it to your discord server one of these days! It needs a website, I know...

### Day 5: June 29, 2021

**Today's Progress**: Started a scraping project to grab dofus asssets

**Thoughts:** Okay, I ran into a bot called poketwo for discord, and I just had a lightbulb of, "Why am I trying to come up with everything on my own, when I could just get all the assets from a game I love!" I'll still have all the features I want, but I can have it themed off of dofus. I'm going to open source the bot as well, since I imagine there are copyright issues with making money off a game with assets based on a real game. 

**Link to work:** https://github.com/cjw21824/scrapus/

### Day 6: June 30, 2021

**Today's Progress**: Gathered and formatted URLs for each monster's page

**Thoughts:** fought with pandas table scraping with no real luck, so I pivoted to findign the href of each row and putting it in a queue for further processing. From there I'll go to each moster's page and grab the info I need. Things like name, type, level, characteristics, drops, drop images, monster image, etc 

**Link to work:** https://github.com/cjw21824/scrapus/

### Day 7: July 1st, 2021

**Today's Progress**: Learned all about threading and the threadpoolexecuter!

**Thoughts:** Threading is fun, and can lead to fun unexpected results! I was able to run the selenium webdriver for chrome in multiple threads, chewing through generated URLs 5x faster than I would otherwise! Time to start scraping all the character data from each page and putting it somewhere! I'll have to put the images in the lfs, and the rest of the data in the db. I'll have to keep a field for referencing the correct image as well. 

**Link to work:** https://github.com/cjw21824/scrapus/

### Day 8: July 6th, 2021

**Today's Progress**: Implement the logic to scrape all of the monster's characteristics

**Thoughts:** Scraping can be fun, it can also make me pull out my hair. I finally found a way to scrape the necessary info without too much code being written. Still seems overly complicated but at least I was able to reuse a lot of the code for each piece of info. 

**Link to work:** https://github.com/cjw21824/scrapus/

### Day 9: July 7th, 2021

**Today's Progress**: Implement Image scraping

**Thoughts:** More scraping! Luckily with urllib, I was able to quickly save the images with the name I need for future reference.  

**Link to work:** https://github.com/cjw21824/scrapus/

### Day 10: July 8th, 2021

**Today's Progress**: Store images in Azure blob storage

**Thoughts:** Don't put your images on LFS, when you can easily use blob storage :). Using the azure python sdk is a breeze! I want to start working on infrastructure, but I feel like I need some type of history for the bot, so I don't overwrite work done in the past. This would be in situations where I push new code to production. I also need to work on putting the monster data in a database. I need to re-run migrations to fit the new schema.   

**Link to work:** https://github.com/cjw21824/scrapus/