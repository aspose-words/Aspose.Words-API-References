---
title: BuiltInDocumentProperties.scaleCrop property
linktitle: scaleCrop property
articleTitle: scaleCrop property
second_title: Aspose.Words for Node.js
description: "BuiltInDocumentProperties.scaleCrop property. Indicates whether document thumbnail is cropped or scaled to fit the display."
type: docs
weight: 240
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/scaleCrop/
---

## BuiltInDocumentProperties.scaleCrop property

Indicates whether document thumbnail is cropped or scaled to fit the display.


```js
get scaleCrop(): boolean
```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to get extended properties.

```js
let doc = new aw.Document(base.myDir + "Extended properties.docx");
expect(doc.builtInDocumentProperties.scaleCrop).toEqual(true);
expect(doc.builtInDocumentProperties.sharedDocument).toEqual(true);
expect(doc.builtInDocumentProperties.hyperlinksChanged).toEqual(true);
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

