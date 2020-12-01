### Tool Development Resources

* [A somewhat complete description](/src/admin/tools/tool-config-syntax/index.md) of tags used for in tool XML files.
* A place to share your tools with the community: the [Galaxy Tool Shed](http://toolshed.g2.bx.psu.edu/) - more information on [publishing tools to the ToolShed](/src/toolshed/index.md).
* [Planemo](https://planemo.readthedocs.org/en/latest/) a CLI tool to assist tool developer - easily lint, test, and preview your tools. ([Quick Start](https://planemo.readthedocs.org/en/latest/readme.html#quick-start), [Planemo on Github](https://github.com/galaxyproject/planemo))
* [Tool Development Training Materials](https://github.com/Public-Health-Bioinformatics/galaxy-tool-tutorials) - from Hsiao lab, BC Public Health Microbiology & Reference Laboratory, BC Centre for Disease Control.
  * [Tool Development Slides (PDF)](https://github.com/Public-Health-Bioinformatics/galaxy-tool-tutorials/blob/master/Galaxy%20Tool%20Development.pdf?raw=true)
  * [Tool Versioning Slides (PDF)](https://github.com/Public-Health-Bioinformatics/galaxy-tool-tutorials/raw/76e1511413202122fbb3a758510744442b2726b7/Galaxy%20Tool%20Versioning.pdf)
* [A tutorial](/src/admin/tools/Writing Tests/index.md) on writing of functional tests
* [What to do](/src/future/Job Failure When stderr/index.md) if Galaxy incorrectly reports that your tool failed to execute
* [Best Practices](https://galaxy-iuc-standards.readthedocs.org/) for Tool Development
* Discussions on [consuming](http://bit.ly/gcc2014workflows) and [producing](https://bitbucket.org/galaxy/galaxy-central/pull-request/634/allow-tools-to-explicitly-produce-dataset) collections of datasets in tools.
* [A discussion](/src/admin/tools/multiple-output-files/index.md) on outputing multiple individual datasets
* [Tips on writing secure tools](/src/develop/security-tool-tips/index.md).
* Tool conversion and generation efforts:
  * [argparse2tool](https://github.com/hexylena/argparse2tool) - a drop in replacement of Python's argparse to generate Galaxy tools by Helena Rasche.
  * A [discussion](https://groups.google.com/forum/#!searchin/common-workflow-language/galaxy/common-workflow-language/xa7HeDfIhw4/oAfg2Dk7ZHMJ) on converting common workflow language tool descriptions into Galaxy tools - with prototype by Peter Amstutz.
  * If you need to run an arbitrary working script (Python, Perl, R or Bash currently supported), and optionally turn it into a proper Galaxy tool, the [Tool Factory](https://bitbucket.org/fubar/galaxytoolfactory) can be installed in a local Galaxy from the Main Tool Shed to instantly wrap arbitrary scripts. It will turn these into Tool Shed archives ready to upload to a new repository from where they can be automagically installed into any Galaxy. **Only runs for administrative users** - exposes insecure unrestricted scripting, so only install in private development clones please. Generated tools are as secure as any other Galaxy tools.
  * Unavailable June 2020: A tool interface generator at [http://cli-mate.lumc.nl](http://cli-mate.lumc.nl). Github last update Aug 15, 2014  [https://git.lumc.nl/humgen/cli-mate](https://git.lumc.nl/humgen/cli-mate).
* Popular tool repositories on [github](https://github.com/) to contribute to and serve as best practice examples:
  * [tools-iuc](https://github.com/galaxyproject/tools-iuc) - A collection of tools developed and maintained by the the Intergalactic Utilities Commission (the IUC). ([Contributing to tools-iuc](https://github.com/galaxyproject/tools-devteam/blob/master/CONTRIBUTING.md))
  * [tools-devteam](https://github.com/galaxyproject/tools-devteam) - A collection of tools developed and maintained by the 'devteam'. ([Contributing to tools-devteam](https://github.com/galaxyproject/tools-devteam/blob/master/CONTRIBUTING.md))
  * [Bjoern's Galaxy Tools](https://github.com/bgruening/galaxytools) - A collection of tools developed and maintained by [BjoernGruening](/src/people/bjoern-gruening/index.md). ([Contributing to galaxytools](https://github.com/bgruening/galaxytools/blob/master/CONTRIBUTING.md))
  * [galaxy_blast](https://github.com/peterjc/galaxy_blast) - A best practice set of tools wrapping NCBI BLAST+ and related applications maintained by Peter Cock. ([Contributing to the BLAST+ tools](https://github.com/peterjc/galaxy_blast/blob/master/CONTRIBUTING.md))
  * [GalaxyP Tools](https://github.com/galaxyproteomics/tools-galaxyp) - A collection of tools for proteomics maintained by the GalaxyP team.
