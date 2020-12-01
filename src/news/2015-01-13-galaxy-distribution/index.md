---
title: "January 13, 2015 Galaxy Distribution"
date: "2015-01-13"
---
<div class='right'><a href='http://getgalaxy.org'><img src="/src/images/logos/GetGalaxyOrg.png" alt="width=175" /></a></div>
**[Complete News Brief](http://wiki.galaxyproject.org/DevNewsBriefs/2015-01-13)**
<br />
# Highlights

## Security

Several *critical* security vulnerabilities were recently discovered by Bartlomiej Balcerek and colleagues at the Wroclaw Centre for Networking and Supercomputing. This [stable Galaxy release contains fixes for those vulnerabilities](/src/archive/dev-news-briefs/2015-01-13/index.md#security). **The Galaxy Team strongly encourages Galaxy server administrators to update their Galaxy servers immediately.**

## IPython Integration

Thanks to the awesome work of community members Björn Grüning and Helena Rasche, [Galaxy now features integration with the popular IPython project](/src/archive/dev-news-briefs/2015-01-13/index.md#ipython-integration). The [Galaxy-IPython](https://github.com/bgruening/galaxy-ipython) project has been merged into Galaxy core and made into a generic plugin framework of interactive environments based on Docker. 

## Tool Form Upgrade (for Beta Testing)

In Galaxy's development branch, the basic tool from has been [redesigned and modernized to address certain limitations in Galaxy's responsiveness when working with longer forms containing multiple parameter choices](/src/archive/dev-news-briefs/2015-01-13/index.md#tool-form-upgrade-for-beta-testing). This new tool form will become the default with the next release - but we are hoping tool author's and power users enable it and provide feedback during this release cycle in order to ensure it is working ideally when it becomes the default.

## Get The Distribution

<table>
  <tr>
    <td rowspan=3 style=" border: none;"> <a href='http://getgalaxy.org/'><img src="http://galaxy.psu.edu/static/getgalaxy.png" alt="getgalaxy" width=70 /></a> &nbsp;&nbsp; </td>
    <td colspan=2 style=" border: none;"> <strong><a href='http://wiki.galaxyproject.org/Admin/Get%20Galaxy'>getgalaxy.org</a></strong> </td>
  </tr>
  <tr>
    <td style=" border: none;"> <strong><a href='http://galaxy-dist.readthedocs.org'>galaxy-dist.readthedocs.org</a></strong> </td>
    <td style=" border: none;"> </td>
  </tr>
  <tr>
    <td style=" border: none;"> <strong><a href='http://bitbucket.org/galaxy/galaxy-dist'>bitbucket.org/galaxy/galaxy-dist</a></strong> </td>
    <td style=" border: none;"> </td>
  </tr>
  <tr>
    <td style=" border: none;"> </td>
  </tr>
  <tr>
    <td style=" border: none;"> <strong>new</strong>: </td>
    <td style=" border: none;"> <code>$ hg clone https://bitbucket.org/galaxy/galaxy-dist#stable </code> </td>
  </tr>
  <tr>
    <td style=" border: none;"> <strong>upgrade</strong>: </td>
    <td style=" border: none;"> <code>$ hg pull </code> <br /> <code>$ hg update latest_2015.01.13</code> </td>
  </tr>
</table>

<br /><br />
*Thanks for using Galaxy!* <br />
[The Galaxy Team](/src/galaxy-team/index.md)
