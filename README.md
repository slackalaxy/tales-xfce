# tales-xfce

Xfce 4.12 for Slackware 15.0. An update of https://github.com/slackalaxy/tales

A seta of SlackBuilds for Xfce 4.12 for Slackware 15.0. Names of most packages are changed by adding a `tales-` siffux for those that are part of Slackware. The rest have the same name as on SBo. Make sure you do not install anything from the XFCE group and that you do not have Xfce-related stuff from SBo.


The SlackBuilds follow SBo's style for 15.0.


The build order is listed in the `xfce.sqf` queue file. You can use [sbopkg](https://sbopkg.org/):
* Place the repo folder (e.g. `tales-xfce-main`) as a local repository (e.g. `/var/lib/sbopkg/local/local/tales-xfce-main`)
* Put the `xfce.sqf` in `/var/lib/sbopkg/queues/`
* load queue and proceed as normal.

What I did was, use my [SBoUtils](https://github.com/slackalaxy/sboutils) tools:
* Download the repo
* Run `sborun` on the list:
```
cat xfce.sqf | while read -r a ; do cd $a ; sborun -d -b -ri ; cd .. ; done
```
