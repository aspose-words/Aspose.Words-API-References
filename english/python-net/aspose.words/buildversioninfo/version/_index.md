﻿---
title: BuildVersionInfo.version property
linktitle: version property
articleTitle: version property
second_title: Aspose.Words for Python
description: "BuildVersionInfo.version property. Gets the product version."
type: docs
weight: 20
url: /python-net/aspose.words/buildversioninfo/version/
---

## BuildVersionInfo.version property

Gets the product version.


```python
@property
def version(self) -> str:
    ...

```

### Remarks

The product version is in the "Major.Minor.Hotfix.0" format.




### Examples

Shows how to display information about your installed version of Aspose.Words.

```python
print(f'I am currently using {aw.BuildVersionInfo.product}, version number {aw.BuildVersionInfo.version}!')
```

### See Also

* module [aspose.words](../../)
* class [BuildVersionInfo](../)

