#Intro the Zotero API

First need to download libZotero, a Python module that allows you to interact with Zotero API, with`pip install libZotero`

From here, we can follow each step, but when we reached `for item in items: print item.bibContent` to get full bibliographic informatin we received an error that read:

![unicode error](https://drive.google.com/file/d/0ByTTKpFauSsSMHVMRzNyaFlmYjQ/view?usp=sharing)

So, start back at the beginning, `from libZotero import zotero`, then tell Python the user/group code and API Key for the Zotero library you want to use.

If we use the Programming Historian Library they advise, we get no input with the command, `items = zlib.fetchItemsTop({'limit': 5, 'content': 'json,bib,coins'})` 

As well as we don't get the same metadata detail from command, `for item in items:
print 'Item Type: %s | Key: %s | Title: %s' % (item.itemType,item.itemKey, item.title)`

![Programming Historian Zotero Library](https://camo.githubusercontent.com/c53413ff1d1989a494a885fa0704613383b27747/68747470733a2f2f64726976652e676f6f676c652e636f6d2f66696c652f642f30427954544b70466175537353596b3935566c4e34565556665554412f766965773f7573703d73686172696e67)

However, by synching the informatin we inputted into Zotero Standalone Desktop in Pandoc Tutorial by going Actions>Preferences>Synch and entering our account information that can be created on the Zotero website.

![synching account](https://drive.google.com/file/d/0ByTTKpFauSsSdGRBQkhJVEJIWkU/view?usp=sharing)

You information you inputted into the desktop are now found online. From here, you need to find your User code and API Key to tell Python where your account API is located. To do this, go to Settings>Feeds/API. Your userID will be displayed and you create a 'new private key'.

![Zotero account API/userkey](https://drive.google.com/file/d/0ByTTKpFauSsSU2tMeXR3SGNBRUU/view?usp=sharing)

Now you can replace `zlib=zotero.Library('group','155975','<null>','9GLmvmZ1K1qGAz9QWcdlyf6L')` with your information, switching `group` with `user` and inputting your user code and API Key.

![personal library results](https://drive.google.com/file/d/0ByTTKpFauSsSQ0F4bU9kRmszQU0/view?usp=sharing)

This is an interesting way to see the organization of your own metadata or if you wanted to pull sources from a group's or person's Zotero account. However, I wasn't sure if you could just look up the API keys for groups or if you needed to be a member. For example, I wasn't able to find the information they provided in the tutorial (user code and API key) on the Zotero account of Programming Historian example. 

Tutorial 2: Creating a New Item
Simple to follow instructions. Can pick from list of things you want to create. But I received "403: Write access denied"

![Creating New Item error](https://drive.google.com/file/d/0ByTTKpFauSsSUHpUaEdYNTJwclk/view?usp=sharing)

![Creating New Item with script](https://drive.google.com/file/d/0ByTTKpFauSsSWFV2N2hvcXYzWFE/view?usp=sharing)

