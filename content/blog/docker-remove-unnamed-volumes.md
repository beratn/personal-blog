---
path: docker-remove-unnamed-volumes
date: 2020-08-02T11:06:37.570Z
title: Docker Remove Unnamed Volumes
description: Docker Remove Unnamed Volumes
---
It's a basic script to remove unnamed volumes.

`docker volume ls --format "{{.Name}}" | while read -r line; do [ "64" == "${#line}" ]&& docker volume rm  "$line"; done`

**This code removes volumes which name has 64 chars. Make sure that you have not any volume name has 64 chars length**
