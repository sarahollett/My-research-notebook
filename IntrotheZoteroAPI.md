#Intro the Zotero API

First need to download libZotero, a Python module that allows you to interact with Zotero API, with`pip install libZotero`

From here, we can follow each step, but when we reached `for item in items: print item.bibContent` to get full bibliographic informatin we received an error that read:

![unicode error](http://s29.postimg.org/cj0pc6hyf/unicodeerror.jpg)

So, start back at the beginning, `from libZotero import zotero`, then tell Python the user/group code and API Key for the Zotero library you want to use.

If we use the Programming Historian Library they advise, we get no input with the command, `items = zlib.fetchItemsTop({'limit': 5, 'content': 'json,bib,coins'})` 

As well as we don't get the same metadata detail from command, `for item in items:
print 'Item Type: %s | Key: %s | Title: %s' % (item.itemType,item.itemKey, item.title)`

![Programming Historian Zotero Library](http://s29.postimg.org/biiu60uhz/proghistzoterolib.jpg)

However, by synching the informatin we inputted into Zotero Standalone Desktop in Pandoc Tutorial by going Actions>Preferences>Synch and entering our account information that can be created on the Zotero website.

![synching account](http://s9.postimg.org/5cfpz3ldb/zoterosynch.jpg)

You information you inputted into the desktop are now found online. From here, you need to find your User code and API Key to tell Python where your account API is located. To do this, go to Settings>Feeds/API. Your userID will be displayed and you create a 'new private key'.

![Zotero account API/userkey](http://s10.postimg.org/byjtybr55/Zotero_API.jpg)

Now you can replace `zlib=zotero.Library('group','155975','<null>','9GLmvmZ1K1qGAz9QWcdlyf6L')` with your information, switching `group` with `user` and inputting your user code and API Key.

![personal library results](http://s10.postimg.org/4jz3jound/personallibrary.jpg)

This is an interesting way to see the organization of your own metadata or if you wanted to pull sources from a group's or person's Zotero account. However, I wasn't sure if you could just look up the API keys for groups or if you needed to be a member. For example, I wasn't able to find the information they provided in the tutorial (user code and API key) on the Zotero account of Programming Historian example. 

Tutorial 2: Creating a New Item
Simple to follow instructions. Can pick from list of things you want to create. But I received "403: Write access denied"

![Creating New Item error](http://s13.postimg.org/u4ugxd5nb/creatingnewitem.png)

![Creating New Item with script](http://s21.postimg.org/rgh4hcrh3/createnewitemwithscript.png)

