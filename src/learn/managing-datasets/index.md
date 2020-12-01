---
title: Managing Datasets in Galaxy
---
***Datasets*** are the inputs and outputs of each step in an analysis project in Galaxy. Datasets are associated with at least one History, which can be labeled, manipulated, and shared with anyone, whether they have a Galaxy account or not. **Watch the *["Datasets" video](http://vimeo.com/galaxyproject/datasets1)***

The tracking information associated with Datasets in a History represent an experimental record of the methods, parameters, and other inputs. These methods are easily extracted into **[Workflows](/src/learn/advanced-workflow/index.md)**, making an analysis pathway transparent, reproducible, and *reusable*.

Effectively managing datasets is important for general organization, collaboration, publishing, and for staying within the quotas set by the [Main](/src/main/index.md), [Test](/src/test/index.md), and other host instances.

# Getting Datasets in Galaxy

You have multiple options how to get your files into Galaxy thus making them datasets:

<div class='right'>![Upload Modal Icon](/src/learn/managing-datasets/upload_icon.png)</div>
* **Upload modal** - Interface within Galaxy that suits the best for uploading small files from disk or fetching data from other servers. You can reach it by clicking on its icon (right picture) in the tool panel. 
* **FTP upload** - In case of large files (the upload modal ~~has ~2GB browser limit~~ can now handle data over 2 GB in most cases) or unpredictable connection (support for pausing and resuming) you might want to use FTP instead. The Galaxy server you want to upload data to has to have an FTP service configured (both [Main](/src/main/index.md) and [Test](/src/test/index.md) instances do). See more details at [FTPUpload](/src/ftp-upload/index.md).

# Dataset Icons & Text

Watch the **[Datasets 1](http://vimeo.com/galaxyproject/datasets1)** video to get oriented with these functions using a variety of real datasets on **Galaxy's** public **[Main](/src/main/index.md)** server **[usegalaxy.org](http://usegalaxy.org)**.
* Upper right corner
  * ![](/src/images/icons/eye.png) Display data in browser "eye icon"
  * ![](/src/images/icons/pencil.png) Edit attributes "pencil icon"
  * ![](/src/images/icons/deleteX.png) Delete "'X' icon"
* Lower right corner
  * Edit dataset tags
  * Edit dataset annotation
* Upper left corner
  * Dataset name
  * Dataset size/number of lines (actual or estimated)
  * format [datatypes](/src/learn/datatypes/index.md)
  * database
  * ![](/src/images/icons/HistoryInfo.png) Info (optional)
* Lower left corner
  * Download
  * View Details
  * Run this job again ![](/src/images/icons/arrow-circle.png)
  * Display in [trackster](/src/learn/visualization/index.md) (optional)
  * display at [UCSC](http://genome.ucsc.edu) main  (optional)
  * display at [Ensembl](http://www.ensembl.org) Current (optional)

# Data size and disk Quotas

* The size limit for a file loaded using [FTP](/src/ftp-upload/index.md) is 50G.
* The size limit for a job's output is (unrelated to quotas):
  * 50G on the [Test](/src/test/index.md) server
  * 200G on the [Main](/src/main/index.md) server
* The size limit for all data (quotas) on the Galaxy public servers is explained at:
  * [Test](/src/test/index.md) server
  * [Main](/src/main/index.md) server
* Administrative instructions for [ disk quotas](/src/admin/disk-quotas/index.md)

# Format

* The format of a dataset is ideally defined by the assigned **[datatype](/src/learn/datatypes/index.md)** attribute. Deviations in input dataset format are the first variable to examine when a tool (job) fails. Many of the tools in the "Text Manipulation" tool group can be used to both examine and correct a dataset's format to bring it into alignment with the assigned [datatype](/src/learn/datatypes/index.md) attribute specification.
* To initially **assign** a dataset's [datatype](/src/learn/datatypes/index.md) attribute, the uploaded/imported file can be specified with some import tools or be named with the appropriate file extension. To specify, modify or correct a dataset's [datatype](/src/learn/datatypes/index.md) attribute after upload, click on the "pencil" icon ![](/src/images/icons/pencil.png) in the right corner of the dataset's box to reach the "Edit Attributes" form. Use the "Change data type" section of the form to make changes and click on *Save*. Galaxy will modify the [datatype](/src/learn/datatypes/index.md) and metadata.
* To **transform** a dataset format (original &rarr; new [datatype](/src/learn/datatypes/index.md) attribute), use one of the many tools in the *Convert Formats* group.
* ***TIP*** The quickest way to locate tools that manipulate specific formats is to use the Tool Search (top of left Galaxy Tool panel, *gear icon* menu). For example, type in  *[M-A-F](/src/learn/datatypes/index.md#maf)* to locate tools in the tool group *Convert Formats* that transform to/from Multiple Alignment Format.

# Visualize

* For many [datatypes](/src/learn/datatypes/index.md), clicking on the **eye icon** ![](/src/images/icons/eye.png) for "Display data in browser" will display the contents or a preview of the contents in as unformatted text in the center pane (exceptions include compressed [datatypes](/src/learn/datatypes/index.md) such as BAM).
* Direct links to view a dataset within a browser may include:
  * [Trackster "Galaxy Track Browser (GTB)"](/src/learn/visualization/index.md)
  * [GeneTrack](http://atlas.bx.psu.edu/software/genetrack.html)
  * [UCSC](http://genome.ucsc.edu)
  * [Ensembl](http://www.ensembl.org)

# Copy

* To copy the datasets within a history to another history, from the right history pane's top *Options* menu select *Copy Datasets*. On the form in the center pane, specify the *From* and *To* history/histories.
  * From: Select the datasets to be copied in the left column *Source History:*.
  * To: Select the location to copy the datasets in the right column *Destination History:*.
    * Options include a single existing history, multiple existing histories, or a newly created and named history.
* ***TIP*** to *Copy* a **Hidden** dataset (see below), in the *From* histories right pane, use *gear icon &rarr; Unhide Hidden Datasets*, then once the datasets refresh, use *This dataset has been hidden. Click  _here_ to unhide.*

# Clone (deprecated)

* To clone a history is to create an exact copy of the prior history in one step. The new history will be named with the original history's name prefixed by *Clone of*. Clone is the simplest way to manage datasets when some items in a history need to be retained but the remainder can be deleted (permanently, to reduce disk usage).
  * Options are:
  * *Clone all history items, including deleted items*
  * *Clone only items that are not deleted*
* ***TIP*** One use of this option is to **quickly retain some datasets and permanently delete others** (to reduce disk use counted in user [quota](/src/admin/disk-quotas/index.md) on [Main](/src/main/index.md) or [Test](/src/test/index.md)). First, in the History pane, in the original history, delete individual datasets by clicking on the *X* delete icon ![](/src/images/icons/deleteX.png) if not to be **Cloned**, remember to delete **Hidden** datasets, (see below). Next, *Clone* the original History. Once complete, the cloned History will contain the datasets to be retained and the original History can be deleted permanently with *gear icon &rarr; Saved Histories*, select original History from the list, and clicking the button *Delete Permanently*.

# Hidden

* Datasets may be hidden in the default History view as a Workflow option. If you have run a workflow with hidden datasets, choose "gear icon &rarr; Include Hidden Datasets or Unhide Hidden Datasets" or use the toogle at the top of the history panel (directly below the history name) to view them.
  * When using **Clone** (see above) to manage datasets to reduce disk usage for [quotas](/src/admin/disk-quotas/index.md), viewing and deleting hidden datasets can be a very important step. Unless deleted, hidden datasets are moved to the new cloned history.
  * When using **Copy** (see above) to manage datasets to reduce disk usage for [quotas](/src/admin/disk-quotas/index.md), hidden datsets will not be in the "From" list of datasets available to transfer unless they are unhidden using *gear icon &rarr; Unhide Hidden Datasets*, then *This dataset has been hidden. Click__here_ to unhide.*

# Delete vs Delete Permanently

Tutorials

  * [Galaxy Training Network (GTN)](https://training.galaxyproject.org/): [Data Manipulation](https://training.galaxyproject.org/training-material/topics/galaxy-data-manipulation/)

Methods

* Deleting Datasets and Histories
  * **Watch how it works in the [Managing Histories](http://vimeo.com/galaxyproject/managehistories) video.**
  * **Deleted** datasets and histories **can be recovered** by users as they are retained in Galaxy for a time period set by the instance administrator. For the Galaxy public instances [Main](/src/main/index.md) and [Test](/src/test/index.md), this is currently several months.
  * **Permanently deleted** datasets and histories **cannot be recovered** by the user or administrator.
  * Deleted datsets can be undeleted or permanently deleted within a History. 
  * Links to show/hide deleted (and hidden) datasets are at the top of the History panel. Only active datasets are shown by default.
  * To review or adjust an individual dataset, click on the name to expand it. If it is only deleted, but not permenently deleted (purged), you'll see a message with links to recover or to purge: *This dataset has been deleted*. Click on *Undelete it* to recover the dataset, making it active and accessible to tools again. Click on *Permenently remove it from disk* to purge the dataset and remove it from the account quota calculation.
  * To review or adjust multiple datasets in batch, click on the "checked box" icon near the top right of the history panel to switch into "Operations on Mulitple Datasets" mode. Several options to show, hide, delete, undelete, purge, and group datasets are available. A selection box will be available for each individual dataset. Check the datasets you want to modify and chose your option. 
  
  
* [Quotas](/src/admin/disk-quotas/index.md) for Datasets and Histories
  * **Deleted** datasets and **deleted** histories containing datasets **are considered when calculating [quotas](/src/admin/disk-quotas/index.md)** on [Main](/src/main/index.md) or [Test](/src/test/index.md).
  * **Permanently deleted** datasets and **permanently deleted** histories containing datasets **are not considered**.
  * Imported native **Data Library** datasets **are not considered**.
  * Datasets can be associated with one or more History, but are only considered once.
  * All copies of a dataset must be permanently deleted for it to not be considered.
  * Histories/datasets that are shared with you are *only partially considered* unless you import them.
  * **Active** and **Deleted** histories can be **permanently deleted** under *User &rarr; Histories*. Click on *Advanced Search*, then set *status: all*. 
  * To review or change the status for an individual History, click on the History name and choose an option from the pull-down menu. *Peremenently delete* will purge an entire History and all Datasets it includes.
  * To review or change the status for multiple Histories, check the boxes for the Histories to be discarded and then click on one of the the buttons at the bottom of the form. *Permanently delete* will purge entire Histories and all Datasets included.
  * Note: A History must be *Unshared* before it can be *Deleted* or *Permenently deleted*. Adjust the sharing state for a History on the *User &rarr; Histories* form or from the History menu on the *Share or Publish* form.
  
* ***WARNING*** **Permanently deleted (purged)** datasets and histories **cannot be recovered** by the end user or an administrator. The best way to avoid losing important data by accident is to clearly name all important histories and datasets.
  * Name a dataset:
    * Click on the *pencil icon* ![](/src/images/icons/pencil.png) on the top right of a Dataset to reach the *Edit Attributes* form. A dataset's primary *Name, Info , Annotation, and Notes* can be adjusted on the first tab, and other metadata attributes can be adjusted on the other tabs.
    * ***TIP*** Copying the Galaxy default *Name* into the "Info: field, then adding in a custom *Name* is one way to preserve the tool output original *Name* while still distinguishing one similarly named dataset from another. This can be useful when reviewing analysis steps and choosing which datasets to retain and which to remove when an analysis is under review or completed.
  * Name a history:
    * Click near the top of the right history pane where the default text *Unnamed history* is located. Enter the new name and and press "enter/return".
    * From *User &rarr; Saved Histories*, check the histories (one or more) to be renamed, then click on the bottom button *Rename*. On the *Rename* form, *Current Name* is on the left, *New Name* is on the right. Edit *New Name* for each history then click on the button *Rename Histories*.

# Searching Datasets

You can ***search your datasets*** in a number of ways:

* A search bar is at the top of every History. 
* *Type* text into the field (advanced options are described below) and press "enter/return". The list of Datasets in the History will change to include only those that match the search term, excluding those that don't. 
* *Clear* the search by removing the text in the bar and pressing enter, or by pressing the ESC key while the text is highlighted, or by clicking on the "clear search" button on the right side of the bar. 

Some notes:
* Searches are case insensitive: 'some' will match both 'some' *and* 'Some'.
* *Searches will persist until cleared*. If you switch histories while searching, the list of datasets will still be
    narrowed to what matches your search terms.
* Terms are space separated. For example, to search for an interval datatype dataset named *~MyDataset* when more than
    one interval dataset is present and more than one dataset is named ~MyDataset, use `interval MyDataset` (or
    `MyDataset interval` - order doesn't matter).
* Deleted and hidden datasets are not shown unless you've included them by using the *Include deleted datasets* and/or
    *Include hidden datasets* options in the history options menu (the gear icon at the top left of the history panel).

Advanced Options:
* To search for terms that include whitespaces (e.g. a dataset named 'My Dataset' which includes a space) you can
    enclose a search term with double quotes ("My Data") and this will match the dataset in the example but exclude any
    dataset that may have matched an un-enclosed term (such as '~MyInterval' or 'Some Data').
* Search terms are applied to many of the 'fields' that describe a dataset (i.e. name, format, database, info, 'blurb') and, by default, check all fields against each term. To apply a search term to only one field, use the field name followed by an equals sign and then followed by the term (or double quote enclosed term). E.g. `name="My Dataset" format=interval`. Here is a list of field names that can be used:
  * `name` or `title`: the name or partial name of the dataset(s)
  * `database` or `genome_build`: the name or partial name of the genome database (e.g. *hg19*)
  * `format` or `file_ext`: the file type/datatype of the dataset(s)
  * `description`: the text or partial text of description of the dataset(s) - the text just below the dataset title shown when the dataset is expanded.
  * `info`: the text or partial text of the info box of the dataset(s) - the text just below the format and database and above the download and info buttons shown when the dataset is expanded.
  * `annotation`: the text or partial text of your annotation on the dataset(s)
  * `tag`: the text or partial text of any applied you to the dataset(s)
* The field name specifiers can be applied more than once. For example, to find datasets that have both the 'paper1' and '2nd paper' tags (as opposed to those that have *one or the other*), use `tag=paper1 tag="2nd paper"`.

----
