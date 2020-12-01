---
title: Tool Developers BoF
---
{{> Events/GCC2013/Header }}



{{> Events/GCC2013/LinkBox }}
{{> Events/GCC2013/BoF/LinkBox }}

<div class='left'><a href='/src/events/gcc2013/bof/index.md'><img src="/src/images/logos/GCC2013BoFLogo.png" alt="" width="160" /></a></div>

This page describes the **Tool Developers** [Birds of a Feather](/src/events/gcc2013/bof/index.md) meetup being held at [GCC2013](/src/events/gcc2013/index.md).

The aim is for tool developers to discuss the process of developing tools for galaxy. 

Potential topics could include;

* Best practices for publishing on the toolshed
* Writing good functional tests
* Tool UI choices. What works and what doesn't
* Strategies for dealing with repository dependencies

## When and Where

The [time and location](/src/events/gcc2013/bof/index.md#bof-schedule) for this BoF will be Monday evening in the escape Pub. We will try to be in the pub early (Just after 5pm) to grab a quiet corner.

## Who is Participating

If you are interested, please add your name below and/or send an email to the [Intergalactic Utilities Commission](mailto:galaxy-iuc AT lists DOT bx DOT psu DOT edu).

* [Ira Cooke](mailto:iracooke AT gmail DOT com)
* [Björn Grüning](mailto:bjoern.gruening AT pharmazie DOT uni-freiburg DOT de)
* [JJ Johnson](mailto:jj AT umn DOT edu)
* Peter Cock
* [Greg Von Kuster](/src/people/greg_vonkuster/index.md)
* [Dave Bouvier](/src/people/dave-bouvier/index.md)
* [Dan Blankenberg](/src/people/dan/index.md)
* [Christian Andreetta](http://www.computing.uni.no/staff?nickname=christiana)
* Lionel Guy, Uppsala University
* Christos Kannas, University of Cyprus
* [Graham Etherington](mailto:Graham dot Etherington AT tsl DOT ac DOT uk)
* Nathan Cole, NCI/SAIC

## Other Tool and Tool Shed Content at GCC2013

* "[Introduction to Tool and Data Source Configuration](/src/events/gcc2013/training-day/index.md#introduction-to-tool-and-data-source-configuration)" [Training Day](/src/events/gcc2013/training-day/index.md) session
* "[Advanced Tool and Data Source Configuration"](/src/events/gcc2013/training-day/index.md#advanced-tool-and-data-source-configuration) [Training Day](/src/events/gcc2013/training-day/index.md) session
* "[Galaxy Tool Shed](/src/events/gcc2013/training-day/index.md#galaxy-toolshed)" [Training Day](/src/events/gcc2013/training-day/index.md) session
* "[Reproducible research and the 90/10 rule: Improving the ratio of light script to dark script matter in your Galaxy](/src/events/gcc2013/abstracts/index.md#reproducible-research-and-the-9010-rule-improving-the-ratio-of-light-script-to-dark-script-matter-in-your-galaxy)" talk
* "[Enhancing the Galaxy Tool Shed](/src/events/gcc2013/abstracts/index.md#enhancing-the-galaxy-toolshed)" talk
* "[A Galaxy of learning: Bioinformatics tutorials based on Galaxy](/src/events/gcc2013/abstracts/index.md#a-galaxy-of-learning-bioinformatics-tutorials-based-on-galaxy)" talk
* "[Managing Galaxy's Built-in Data](/src/events/gcc2013/abstracts/index.md#managing-galaxys-built-in-data)" talk
* "[Galaxy-P: Beyond Proteomics](/src/events/gcc2013/abstracts/index.md#galaxy-p-beyond-proteomics)" talk

## Questions?

Send them to the [Intergalactic Utilities Commission](mailto:galaxy-iuc AT lists DOT bx DOT psu DOT edu).

## Notes, Suggestions, Desires from the BoF

* Better visual cues for Groups of parameters
* How to handle datatypes in the toolshed
  * Collisions
  * Searching
* Naming Tabular Columns in the preview / peek
  * especially via datatypes_conf.xml
* Peter's Trello Card on column name selection
* Naming of multiple outputs from tools
  * or naming from input name (possible to do manually via label tag, but some automatic way)
* Groups of files (i.e. the functionality provided by John Chilton's declined pull request that uses composite datatypes, but done 'better')
* Make running buildbot locally easy
* Tool testing framework enhancements
  * grouping parameters (e.g. multiple repeats)
* Trello
  * Slow
  * Search sucks (especially for issue tracking)
* Toolshed: how to offer repository for adoption to other users (including advertising availability)
* Toolshed bitbucket integration
  * Tool's homepage
  * Pull Requests, easier collaboration, etc
* Inheriting toolshed tools from other users (e.g. important tools could be given to IUC / devteam, etc)
* Create IUC Toolshed user ( done :) )
* Per Toolshed User Grant access (can grant on per repo level, but not all of repos on an account; see IUC user being shared between persons, instead )
  * create repo as e.g. IUC user (an 'organization' account)
* How to handle displaying and agreeing to licensing for tools
  * clicking 'I agree' during install or running
  * Avoiding Workflows sharing with licensing agreement checkbox already checked (e.g. when using a validator, see MEME tools)
* Workflows now save tool versions - so for old tool ids could also filter with ID (e.g. migrated tools)
* Uploading workflwo to toolshed using old tool IDs should give a warning to the uploader
* When Searching toolshed, allow limiting to rating/start ranges, etc
* Allow rating tools by users from within Galaxy
  * i.e. user runs a toolshed tool at some Galaxy instance and wants to go rate the tool in the toolshed
* Better / standardized handling of references / citations (right we include it as free text in tool help)
* When using a Galaxy tool, make it easier to get back to the toolshed, e.g. for installing it into your own Galaxy instance (can we create some copy and pasteable link that is in Galaxy tool interface and then can be entered a different Galaxy instance for admin install)
* Estimate remaining runtime
  * e.g. allow a tool itself to provide feed back, many cmdline tools already estimate by e.g. printing to stderr, but we should be able to get this info back into Galaxy in realtime to the user
* Run toolshed automated testing framework on file upload (not just overnight, as is now)
