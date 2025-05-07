---
title: TxtLoadOptions.autoNumberingDetection property
linktitle: autoNumberingDetection property
articleTitle: autoNumberingDetection property
second_title: Aspose.Words for Node.js
description: "TxtLoadOptions.autoNumberingDetection property. Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document"
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/txtloadoptions/autoNumberingDetection/
---

## TxtLoadOptions.autoNumberingDetection property

Gets or sets a boolean value indicating either automatic numbering detection
will be performed while loading a document.
The default value is ``true``.



```js
get autoNumberingDetection(): boolean
```

### Examples

Shows how to disable automatic numbering detection.

```js
let options = new aw.Loading.TxtLoadOptions();
options.autoNumberingDetection = false;
let doc = new aw.Document(base.myDir + "Number detection.txt", options);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [TxtLoadOptions](../)

