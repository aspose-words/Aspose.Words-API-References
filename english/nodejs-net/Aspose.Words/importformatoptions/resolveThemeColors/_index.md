---
title: ImportFormatOptions.resolveThemeColors property
linktitle: resolveThemeColors property
articleTitle: resolveThemeColors property
second_title: Aspose.Words for Node.js
description: "ImportFormatOptions.resolveThemeColors property. Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly"
type: docs
weight: 90
url: /nodejs-net/aspose.words/importformatoptions/resolveThemeColors/
---

## ImportFormatOptions.resolveThemeColors property

Gets or sets a boolean value that specifies whether to resolve theme colors of the shapes forcibly.
The default value is ``false``.



```js
get resolveThemeColors(): boolean
```

### Remarks

Please note that this option is only relevant for the [ImportFormatMode.KeepSourceFormatting](../../importformatmode/#KeepSourceFormatting) mode.


Normally, Aspose.Words doesn't resolve source theme colors when importing styles can be preserved
without expanding formatting attributes into direct ones. However, in this case the actual colors
of the imported shapes can differ from the ones they had in the original document. The reason for
this is the different theme colors in the source and destination documents. Setting this option
to ``true`` forces to resolve source shape theme colors and hence to preserve the actual
color of the shapes they have in the source document.





### See Also

* module [Aspose.Words](../../)
* class [ImportFormatOptions](../)

