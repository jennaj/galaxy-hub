---
title: Account quotas
---
[Back to Support Hub](/src/support/index.md)

 Related topic: 
  
   * [Delete versus Delete Permanently](/src/learn/managing-datasets/#delete-vs-delete-permanently)
    
Tutorials

  * [Galaxy Training Network (GTN)](https://training.galaxyproject.org/): [Data Manipulation](https://training.galaxyproject.org/training-material/topics/galaxy-data-manipulation/)

## How account quotas work

Each Galaxy server is independent. How much disk space to allocate for end users is determined by the administrators of that server.

If you are working at [Galaxy Main](/src/main/index.md) (http://usegalaxy.org), each registered account is granted 250 GB of quota space (disk usage for data storage). Review full details [here (account and job quotas)](/src/main/#user-data-and-job-quotas) and [here (account terms)](/src/support/account/index.md).

Should you have questions after reviewing the options below, this is how to get help: 
* Review prior Q&A or ask a novel question at the **Galaxy Help** forum https://help.galaxyproject.org/.
* Chat with us at **Gitter** https://gitter.im/galaxyproject/Lobby/.
* Send an **email** to [galaxy-bugs@lists.galaxyproject.org](mailto:galaxy-bugs@lists.galaxyproject.org) from your registered account email address.
* **All options** https://galaxyproject.org/support/#help-resources.

Working at a different Public Galaxy server? If you question is general, try the Galaxy Help forum. If server specific or account related, that server's home page or directory page usually contains contact and other information concerning account terms, questions, issues, and quota policies: [Galaxy Platform Directory](/src//use/index.md). If you cannot find the contact information, or are not sure about what the problem is exactly, ask for advice at the Galaxy Help forum or at Gitter. The more context you provide (server URL, problem details), the quicker our community will be able to assist you.


## Does your account usage quota seem incorrect?

Log out of Galaxy, then back in again. This refreshes the disk usage calculation dislayed in the Masthead usage (summary) and under *User > Preferences* (exact).

## How to log in or out of Galaxy? 

The options are included under the **User** menu in the top masthead.

## I need more space for my work

If the account usage is showing that quota is exceeded -[over 250 GB](/src/main/index.md):

### Find all Histories and *purge* (aka permenently delete) those not needed

   * All account Histories can be reviewed under **User > Histories**.
   * Only *active* histories are displayed by default.
   * Click on **Advanced Search**, then choose **status = all** to review all *active*, *deleted*, and *purged* histories.
   * Locate *deleted but not permemently deleted histories* and purge them.
   * [Download](/src/support/download-data/index.md) any datasets or entire histories you want to keep **first**. The history will need to be in an *active* state. Histories that are *deleted* can be *undeleted*, but once a history is *purged* (aka permenently deleted) it cannot be recovered, even by an administrator.
   * Histories must be unshared before they can be deleted or purged. Unshare first as needed.
   * **Histories in a *deleted* state are still part of your quota usage.**
   * **Histories must be *purged* (permenently deleted) to not count toward quota.**

### Find all Datasets or just review those in the active history and *purge* (aka permenently delete) those not needed

   * All account Datasets can be reviewed under **User > Datasets**.
   * Within a History, deleted/permenently deleted Datasets can be reviewed by toggling the *deleted* link at the top of the History panel, found immediately under the History name.
   * Both *active* (shown by default) and *hidden* (the other toggle link, next to the *deleted* link) datasets can be reviewed the same way.
   * Click on the far right "X" to delete a dataset. 
   * To permenently delete: use the link from within the dataset, or use the *Operations on Multiple Datasets* functions, or use the *Purge Deleted Datasets* option in the History menu.
   * **Datasets in a *deleted* state are still part of your quota usage.**
   * **Datasets must be *purged* (permenently deleted) to not count toward quota.**
   
### Find Histories that have been shared with you, and unshare those not needed 
   * All account Histories owned by others, but shared with you, can be reviewed under **User > Histories shared with me**. 
   * Review the list. There may be none!
   * Only a small fraction of the data content in "Histories shared with me" are part of your own quota usage, and *unsharing* will not significantly reduce quota usage for most end-users. However, if there are hundreds (or more!), or many large histories shared with you, clearing these up periodically (*unsharing*) could be worth it.
   * The other person does not need to *unshare* a history for you. *Unshare histories yourself* on this page using the pull-down menu per-history.
   * **View** is a review feature. The data cannot be worked with but many details, including tool and dataset metadata/parameters are included. 
   * **Copy** those you want to work with. This will *increase your quota usage* since that history copy is now one of your histories, but that will also allow you manipulate the datasets or the history itself, independently from the original owner. All History/Dataset functions are available if the other person granted full access to the datasets to you. Dataset sharing is a distinct option on the *Share or Publish* form. Only the original History owner can set the level of sharing (History only, or also Datasets). If you need Dataset access and it wasn't granted, you might need to ask the other person to *reshare* with the box for "Also make all objects within the History accessible." checked. The other person can toggle sharing to "off" for review/changes, then toggled back to "on" after. 
   * **Unshare** any on the list not needed anymore. After a history is copied, you will still have your own version of the history, even if later unshared or the other person who shared it with you makes changes to their own version of the history later on. Meaning, each account's version of a History, and the Datasets in it, are distinct (unless the Datasets were not shared -- then you will still only be able to "view" Datasets, but not work with or download them).
   * Dataset and History privacy options, including sharing, can be set under **User > Preferences**. The automatic default is that none of your account data is shared. You must actively choose to share your work -- both the privacy level AND how -- for any Galaxy Object (Dataset, History, Workflow, Visualization).  
   * **A small fraction of space from "Histories shared with me" in a *shared* state are still part of your quota usage.**
   * **Shared Histories must be *unshared* to not count toward quota usage.** 
   * If you *share* a History with someone else, that does not increase OR decrease *your* own quota usage.
   
### Reduce quota usage while still retaining prior work (data, tools, methods)

   * *There are several options to preserve data/work while also reducing your quota usage.* Some examples are below. 
   * **Download** Datasets as individual files or entire Histories as an archive. Then *purge* them from the public server. 
   * **Copy** Datasets or Histories to another Galaxy server, including your own Galaxy. Then purge. 
   * **Copy** your most important Datasets into a new/other History (inputs, results), then purge the original full History. This can be a quicker alternative if the orignal History is very large or complex to review/purge dataset-by-dataset. 
   * Extract a **Workflow** from the History, then purge it. Workflows do not consume quota space as they do not contain any datasets, only tools/parameters. IF you first saved back the original inputs and final result datasets, the analysis can be rerun to recreate the intermediate datasets and to compare the new result with your original. Be aware that minor differences are expected over time, as tools and Galaxy itself are updated.
   * **Back-up your work**. It is a best practice to download an archive of your FULL original Histories periodically, even those still in use, as a backup. 
   * **In short, keep active work on the server and archive/download older work + backups of current work.** You can always reupload prior downloaded Datasets or Histories later. Or, rerun an analysis with a Workfow and the original inputs.
   * **Resources** Much discussion about all of the above options can be found at the Galaxy Help forum https://help.galaxyproject.org/ (in context with difference use cases). The [Support FAQs](/src/support/index.md) and [Admin Docs](https://docs.galaxyproject.org/) are more places to find help. If any option is unclear or you run into problems, ask for more help! https://galaxyproject.org/support/#help-resources 


## I purged but still need more space!
 
Account quotas are generally fixed at 250 Gb for [Galaxy Main](/src/main/index.md). Other Galaxy servers may differ for quota size and policy. For very large projects, consider moving to a local or cloud Galaxy where you can control the resources.

*Important*: Increased working space (quota size) is unrelated to the computational resouces used to process analysis jobs. If your jobs are failing because they are exceeding resources, there is either an input/usage problem or the work is actually too large to process at the server. Not sure? Check here: [My job ended with an error. What can I do?](/src/support/tool-error/index.md).
 
  * Some work is simply too large for the public resource. How to know? Review the [Using Galaxy choices explained here](/src/choices/index.md). 
  * If your work is academic research based and additional short-term space is needed at Galaxy Main (https://usegalaxy.org), please send an email to galaxy-bugs@lists.galaxyproject.org from your registered account email address, briefly explaining your project and we may be able to help.
  * Also include this information in your email or we will request it, delaying action: 1) your primary academic email address 2) how much space you need 3) how long you need the extra space. 
  * Double-check that you are actually purging old work correctly. We will check first before granting any extra quota. 
  * **Note**: If you have registered or are using or have used more than one account at the Galaxy Main server, this violates our [Terms of Usage](https://usegalaxy.org/static/terms.html). Account terms are explained in a simple and specific sentence exactly where you clicked on the activation link in the registration email recieved when the account was first opened. If that was not clear enough, you must *proactively* clear up account issues and get down to and *keep using* just one account *before extra quota can be granted*. Yes, we will check when you ask, and deny requests that are incomplete. Duplicated accounts created/detected after extra quota is granted will result in the loss of all associated accounts and data, without another reminder. 
  * Not sure what to do? If you have more than one account (old or new) at UseGalaxy.org, manage the data yourself and delete extra/old accounts under *User > Preferences*. Review here if terms of usage are not clear and email us to sort things out if you need to: [Getting an account at Galaxy Main (http://usegalaxy.org)](/src/support/account/index.md)
  * Other Public Galaxy server's may have different account terms or quota increase request proccesses. Check the server's home page or the server's directory page here to locate contact and other information concerning account terms, questions, issues, and quota policies: [Galaxy Platform Directory](/src//use/index.md)
