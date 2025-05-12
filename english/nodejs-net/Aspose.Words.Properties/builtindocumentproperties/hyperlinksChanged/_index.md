---
title: BuiltInDocumentProperties.hyperlinksChanged property
linktitle: hyperlinksChanged property
articleTitle: hyperlinksChanged property
second_title: Aspose.Words for Node.js
description: "BuiltInDocumentProperties.hyperlinksChanged property. Indicates whether hyperlinks in a document were changed."
type: docs
weight: 120
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/hyperlinksChanged/
---

## BuiltInDocumentProperties.hyperlinksChanged property

Indicates whether hyperlinks in a document were changed.


```js
get hyperlinksChanged(): boolean
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

