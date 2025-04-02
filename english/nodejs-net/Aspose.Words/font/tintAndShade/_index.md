---
title: Font.tintAndShade property
linktitle: tintAndShade property
articleTitle: tintAndShade property
second_title: Aspose.Words for NodeJs
description: "Font.tintAndShade property. Gets or sets a double value that lightens or darkens a color."
type: docs
weight: 530
url: /nodejs-net/Aspose.Words/font/tintAndShade/
---

## Font.tintAndShade property

Gets or sets a double value that lightens or darkens a color.


```js
get tintAndShade(): number
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throw if set this property to a value less than -1 or more than 1. |
| RuntimeError (Proxy error(InvalidOperationException)) | Throw if set this property for [Font](../) object with non-theme colors. |

### Remarks

The allowed values are in range from -1 (darkest) to 1 (lightest) for this property.

Zero (0) is neutral.




### See Also

* module [Aspose.Words](../../)
* class [Font](../)

