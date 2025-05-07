---
title: BuiltInDocumentProperties.sharedDocument property
linktitle: sharedDocument property
articleTitle: sharedDocument property
second_title: Aspose.Words for Node.js
description: "BuiltInDocumentProperties.sharedDocument property. Indicates whether the document is a shared document."
type: docs
weight: 260
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/sharedDocument/
---

## BuiltInDocumentProperties.sharedDocument property

Indicates whether the document is a shared document.


```js
get sharedDocument(): boolean
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

