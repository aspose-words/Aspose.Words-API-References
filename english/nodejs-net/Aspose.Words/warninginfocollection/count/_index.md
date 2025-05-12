---
title: WarningInfoCollection.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Node.js
description: "WarningInfoCollection.count property. Gets the number of elements contained in the collection."
type: docs
weight: 20
url: /nodejs-net/aspose.words/warninginfocollection/count/
---

## WarningInfoCollection.count property

Gets the number of elements contained in the collection.


```js
get count(): number
```

### Examples

Shows how to get warnings about unsupported formats.

```js
let warnings = new aw.WarningInfoCollection();
let lo = new aw.Loading.LoadOptions();
lo.warningCallback = warnings;
let doc = new aw.Document(base.myDir + "FB2 document.fb2", lo);

expect(warnings.at(0).description).toEqual("The original file load format is FB2, which is not supported by Aspose.words. The file is loaded as an XML document.");
expect(warnings.count).toEqual(1);
```

### See Also

* module [Aspose.Words](../../)
* class [WarningInfoCollection](../)

