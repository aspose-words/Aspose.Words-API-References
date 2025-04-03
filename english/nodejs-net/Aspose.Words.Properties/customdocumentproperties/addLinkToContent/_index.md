---
title: CustomDocumentProperties.addLinkToContent method
linktitle: addLinkToContent method
articleTitle: addLinkToContent method
second_title: Aspose.Words for NodeJs
description: "CustomDocumentProperties.addLinkToContent method. Creates a new linked to content custom document property."
type: docs
weight: 20
url: /nodejs-net/aspose.words.properties/customdocumentproperties/addLinkToContent/
---

## addLinkToContent(name, linkSource) {#string_string}

Creates a new linked to content custom document property.


```js
addLinkToContent(name: stringlinkSource: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the property. |
| linkSource | string | The source of the property. |

### Returns

The newly created property object or ``null`` when the *linkSource* is invalid.


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
* class [CustomDocumentProperties](../)

