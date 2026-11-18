---
title: Aspose::Words::Saving::Zip64Mode enum
linktitle: Zip64Mode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::Zip64Mode enum. Specifies when to use ZIP64 format extensions for OOXML files in C++.'
type: docs
weight: 88000
url: /cpp/aspose.words.saving/zip64mode/
---
## Zip64Mode enum


Specifies when to use ZIP64 format extensions for OOXML files.

```cpp
enum class Zip64Mode : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Always | 2 | Always use ZIP64 format extensions. |
| IfNecessary | 1 | If necessary use ZIP64 format extensions. |
| Never | 0 | Do not use ZIP64 format extensions. |

## Remarks

 OOXML file is a ZIP-archive that has a 4 GB (2^32 bytes) limit on uncompressed size of a file, compressed size of a file, and total size of the archive, as well as a limit of 65,535 (2^16-1) files in archive. ZIP64 format extensions increase the limits to 2^64. 
## See Also

* [Zip64Mode](../ooxmlsaveoptions/get_zip64mode/)

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
