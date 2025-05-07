---
title: ListCollection.addSingleLevelList method
linktitle: addSingleLevelList method
articleTitle: addSingleLevelList method
second_title: Aspose.Words for Node.js
description: "ListCollection.addSingleLevelList method. Creates a new single level list based on the predefined template and adds it to the list collection in the document."
type: docs
weight: 60
url: /nodejs-net/aspose.words.lists/listcollection/addSingleLevelList/
---

## addSingleLevelList(listTemplate) {#listtemplate}

Creates a new single level list based on the predefined template and adds it to the list collection in the document.


```js
addSingleLevelList(listTemplate: Aspose.Words.Lists.ListTemplate)
```

| Parameter | Type | Description |
| --- | --- | --- |
| listTemplate | [ListTemplate](../../listtemplate/) |  |

### Examples

Shows how to create a new single level list based on the predefined template.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let listCollection = doc.lists;

// Creates the bulleted list from BulletCircle template.
let bulletedList = listCollection.addSingleLevelList(aw.Lists.ListTemplate.BulletCircle);

// Writes the bulleted list to the resulting document.
builder.writeln("Bulleted list starts below:");
builder.listFormat.list = bulletedList;
builder.writeln("Item 1");
builder.writeln("Item 2");
builder.listFormat.removeNumbers();

// Creates the numbered list from NumberUppercaseLetterDot template.
let numberedList = listCollection.addSingleLevelList(aw.Lists.ListTemplate.NumberUppercaseLetterDot);

// Writes the numbered list to the resulting document.
builder.writeln("Numbered list starts below:");
builder.listFormat.list = numberedList;
builder.writeln("Item 1");
builder.writeln("Item 2");

doc.save(base.artifactsDir + "Lists.addSingleLevelList.docx");
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListCollection](../)

