---
title: DocumentProperty.isLinkToContent property
linktitle: isLinkToContent property
articleTitle: isLinkToContent property
second_title: Aspose.Words for NodeJs
description: "DocumentProperty.isLinkToContent property. Shows whether this property is linked to content or not."
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Properties/documentproperty/isLinkToContent/
---

## DocumentProperty.isLinkToContent property

Shows whether this property is linked to content or not.


```js
get isLinkToContent(): boolean
```

### Examples

Shows how to link a custom document property to a bookmark.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.startBookmark("MyBookmark");
builder.write("Hello world!");
builder.endBookmark("MyBookmark");

// Link a new custom property to a bookmark. The value of this property
// will be the contents of the bookmark that it references in the "LinkSource" member.
let customProperties = doc.customDocumentProperties;
let customProperty = customProperties.addLinkToContent("Bookmark", "MyBookmark");

expect(customProperty.isLinkToContent).toEqual(true);
expect(customProperty.linkSource).toEqual("MyBookmark");
expect(customProperty.toString()).toEqual("Hello world!");

doc.save(base.artifactsDir + "DocumentProperties.LinkCustomDocumentPropertiesToBookmark.docx");
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [DocumentProperty](../)

