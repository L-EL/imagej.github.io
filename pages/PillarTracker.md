---
autogenerated: true
title: PillarTracker
breadcrumb: PillarTracker
layout: page
author: test author
categories: Tracking,Visualization,Analysis,Filtering,Plugins
description: test description
---

<div style="float:right;">


{% capture author%}
{% include person content='Xu Xiaochun' %}, {% include person content='Felix Martin Margadant' %}
{% endcapture %}

{% capture maintainer%}
{% include person content='Xu Xiaochun' %}
{% endcapture %}

{% capture source%}
{% include github org='scottreen' repo='PillarTracker' %}
{% endcapture %}
{% include info-box software='ImageJ/Fiji' name='PillarTracker' author=author maintainer=maintainer source=source released='June 2017' latest-version='"""1.1.6 May 2018"""' status='stable, active' category='[Tracking](:Category:Tracking "wikilink"), [Visualization](:Category:Visualization "wikilink"), [Filtering](:Category:Filtering "wikilink"), [Analysis](:Category:Analysis "wikilink"), [Plugins](:Category:Plugins "wikilink")' %}

</div>

This plugin enables user to track pillars with drift correction and visualize the trajectories and deflections.

## Installation

It can be automatically downloaded and installed by Fiji's updater(*Help-\>Update...*). Activate the **PillarTracker** checkbox in *Manage update sites*. For more details about how to update Fiji in a most convenient way, please refer to our documentation here. However, if user doesn't want to use the updater for some reason, one can still download it from following link, and then install it manually.

Latest version: [Pillar\_Tracker\_GUI-1.1.6-SNAPSHOT.zip](https://drive.google.com/file/d/0B3hxvkn3VvhCWUlMZ29OTEZ6ZWs) (\<1 MB)

[PillarTracker\_Documentation.pdf](https://drive.google.com/file/d/0B3hxvkn3VvhCVWJsdUN3eDUyNkk) (\~3 MB)

[Sample\_Files.zip](https://drive.google.com/file/d/0B3hxvkn3VvhCYjFCaWx5dnNpSlE) (61.9 MB)

## Update History

version **1.1.6** (since Apr. 03, 2018)

`(1).save text of trajectories and deflections as CSV file, separately.`

`(2).basic Statistic in Drift Analysis.`

`(3).output ROI data for all frames as table.`

`(4).source code on `[`Github``   ``repository`](https://github.com/scottreen/PillarTracker)`.`

version **1.1.5**

`(1).draw dragon tails for tracks.`

`(2).faster create movie.`

`(3).performance improved for muliti-threading`

`(4).add mean filter to detect maximas`

version **1.1.4**: beta for internal use

version **1.1.3**

`(1).use pillar reconstruction algorithm to establish exact grid.`

`(2).sub-pixel centered kernel when extracting pillar profile.`

`(3).fast compute drift and stabilize the image by phase correlation. `

`(4).create better movie in grid analysis`

version **1.1.2**

`(1).mask filter in frequency domain(FD).`

`(2).fixed bugs on pillar detection.`

version **1.1.1**

`(1).refine the grid based on the silent pillars.`

`(2).faster save data into binary files.`

`(3).hunt contractile unit(CU).`

`(4).save settings into drift binary file.`

version **1.1.0**

`(1).performance improved. GPU acceleration for image cross correlation with kernel.`

`(2).minor bugs are fixed.`

version **1.0.9**

`(1).support BCC arranged pillar, which has 60 degree of grid angle. `

`(2).support fast localization algorithm: center of mass(CM).`

## Acknowledgement

This work is funded by Mechanobiology Institute,Singapore.

If you have any suggestion or comment, please email to:

MR Xu Xiaochun (mbixxc@nus.edu.sg)

DR Felix Martin Margadant (mbifmm@nus.edu.sg)

[Category:Tracking](Category:Tracking "wikilink") [Category:Visualization](Category:Visualization "wikilink") [Category:Analysis](Category:Analysis "wikilink") [Category:Filtering](Category:Filtering "wikilink") [Category:Plugins](Category:Plugins "wikilink")