---
layout: post
title: "tricks and know how"
date: 2016-04-05
---

#Tricks and know how:

###How to mount folder from home(through one hidden ssh)?

using transmit
http://superuser.com/questions/49838/how-to-transfer-files-when-given-two-ssh-accounts

###How to generate non-overlap CCDS bed file?
download file from UCSC, extract ccds intervals,  use bedtools to merge
```
$ wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/database/ccdsGene.txt.gz
$ python extract_interval.py  
$ bedtools sort -i ccds_overlap.bed > ccds_overlap.sorted.bed
$ bedtools merge -i ccds_overlap.sorted.bed > ccd_hg19.bed
```
