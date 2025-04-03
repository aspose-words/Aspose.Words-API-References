---
title: Zip64Mode enumeration
linktitle: Zip64Mode enumeration
articleTitle: Zip64Mode enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Saving.Zip64Mode enumeration. Specifies when to use ZIP64 format extensions for OOXML files."
type: docs
weight: 950
url: /nodejs-net/aspose.words.saving/zip64mode/
---

## Zip64Mode enumeration

Specifies when to use ZIP64 format extensions for OOXML files.

OOXML file is a ZIP-archive that has a 4 GB (2^32 bytes) limit on uncompressed size of a file,
compressed size of a file, and total size of the archive, as well as a limit of 65,535 (2^16-1) files in archive.
ZIP64 format extensions increase the limits to 2^64.


### Members

| Name | Description |
| --- | --- |
| Never | Do not use ZIP64 format extensions. |
| IfNecessary | If necessary use ZIP64 format extensions. |
| Always | Always use ZIP64 format extensions. |

### See Also

* module [Aspose.Words.Saving](../)
* property [OoxmlSaveOptions.zip64Mode](../ooxmlsaveoptions/zip64Mode/)

