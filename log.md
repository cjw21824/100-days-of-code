# 100 Days Of Code - Log

### Day 0: June 21, 2021

**Today's Progress**: Removed secrets hard-coded in my discord bot (so bad I know!) and replaced it with a proper Azure KeyVault reference.

**Thoughts:** Although using the Azure Key Vault is a good step in the right direction, the end goal will be to work on a pipeline that will handle the secrets, so credentials no longer have to be cached when running the program. I'm currently using VisualStudioCredentials() to grab the creds from my working instance of VScode. 

**Link to work:** No link, since it's a private repo, but maybe a link to the discord bot's website in the future. Maybe part of this will be it's front end site??

### Day 1: June 22, 2021

**Today's Progress**: Finished removing the last of my secrets (mine!) and started on bot command logic. 

**Thoughts:** No more db string in the code, which is great. I was able to modify some of the character class definitions, so I can get more information the db models. I worked on "attacking the enemy" commands that will allow characters to attack monsters with the character they created. I created a very rough system to keep track of the 'state' of the mob and to let people know it's dead if someone kills it off. I am falling in love with functional programming. I am using it to return the best spells a user has at their current level.  

**Link to work:** Still no link :). Access upon request, or maybe you can add it to your discord server one of these days! It needs a website, I know...

