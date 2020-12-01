<div class='center'> <a href='http://toolshed.g2.bx.psu.edu'>![Galaxy Main ToolShed](/src/images/logos/ToolShed.jpg)</a> </div>

# Simple Repository Dependencies

Simple repository dependencies are repository dependency definitions that define relationships from the dependent repository (the one containing the **repository_dependencies.xml** file) to any number of additional, separate required repositories. These definitions are categorized as "simple" because the the contents of the related repositories is not considered. These kinds of relationships include 2 features:

* they enable installation of multiple related repositories
* The status of the dependent repository will display the status of its repository dependencies

An example of a repository that contains a simple repository dependency definition is the [emboss_5](http://toolshed.g2.bx.psu.edu/view/devteam/emboss_5) repository in the [main Galaxy ToolShed](http://toolshed.g2.bx.psu.edu). The  [emboss_datatypes](http://testtoolshed.g2.bx.psu.edu/view/devteam/emboss_datatypes) repository defined as a required repository with the inclusion of a file named **repository\_dependencies.xml** in the emboss\_5 repository.
Here are the contents of the **repository\_dependencies.xml** file contained within the emboss\_5 repository.

    <?xml version="1.0"?>
    <repositories description="Emboss 5 requires the Galaxy applicable data formats used by Emboss tools.">
         <repository toolshed="http://toolshed.g2.bx.psu.edu" name="emboss_datatypes" owner="devteam" changeset_revision="a89163f31369" />
    </repositories>

The `<repositories>` tag set can contain any number of `<repository>` tags, each of which will define a dependency relationship to a specific repository name/owner/changeset revision combination within the ToolShed.

**=========================================================================================**
**Important note:** the `<repository>` tag requires 2 of the 4 attributes shown above (name and owner are required), while the other 2 (toolshed and changeset\_revision) are optional. If the toolshed attribute is not defined, the attribute will be set as the local ToolShed. If the changeset\_revision is not defined, the attribute will be defined as the latest installable changeset\_revision of the repository within the ToolShed defined by name and owner. In either case, the repository\_dependencies.xml file will be automatically altered to have these attributes included in the tag with these default values. This automatic alteration will take place before the changeset containing the repository\_dependencies.xml file is committed to the repository in the ToolShed. A 5th attribute named **prior\_installation\_required** is optional as well. If defined, the value should always be "True". When used, this attribute ensures that the required repository will be installed prior to it's dependent repository. See the [Supported tags sets for the tool_dependencies.xml file](https://galaxyproject.org/toolshed/tool-dependencies-tag-sets/) section of the ToolShed wiki for details about all of the supported tool dependency definition tag sets.
**=========================================================================================**
