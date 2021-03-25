---
title: hackthebox- misc - misDIRection Writeup
date: 2021-03-25 20:30:00 +0700
categories: [Writeup, hackthebox]
tags: [web, writeup]     # TAG names should always be lowercase
---

# hackthebox - Misc - Authentication

*Link: https://app.hackthebox.eu/challenges/55*

```
import glob

path = './*/*'
files = glob.glob(path)

l = []
for name in files:
    l.append(name[2:])
dct ={}
for s in l:
    dct[s.split("/")[1]]=s.split("/")[0]
sorted_key = sorted(dct.keys())

for i in sorted_key:
    print(dct[i],end="")
```