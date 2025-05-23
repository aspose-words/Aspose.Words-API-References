﻿---
title: FieldOptions.toaCategories property
linktitle: toaCategories property
articleTitle: toaCategories property
second_title: Aspose.Words for Node.js
description: "FieldOptions.toaCategories property. Gets or sets the table of authorities categories."
type: docs
weight: 180
url: /nodejs-net/aspose.words.fields/fieldoptions/toaCategories/
---

## FieldOptions.toaCategories property

Gets or sets the table of authorities categories.


```js
get toaCategories(): Aspose.Words.Fields.ToaCategories
```

### Examples

Shows how to specify a set of categories for TOA fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// TOA fields can filter their entries by categories defined in this collection.
let toaCategories = new aw.Fields.ToaCategories();
doc.fieldOptions.toaCategories = toaCategories;

// This collection of categories comes with default values, which we can overwrite with custom values.
expect(toaCategories.at(1)).toEqual("Cases");
expect(toaCategories.at(2)).toEqual("Statutes");

toaCategories.setAt(1, "My Category 1");
toaCategories.setAt(2, "My Category 2");

// We can always access the default values via this collection.
expect(aw.Fields.ToaCategories.defaultCategories.at(1)).toEqual("Cases");
expect(aw.Fields.ToaCategories.defaultCategories.at(2)).toEqual("Statutes");

// Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
// Use the "\c" switch to select the index of a category from our collection.
//  With this switch, a TOA field will only pick up entries from TA fields that
// also have a "\c" switch with a matching category index. Each TOA field will also display
// the name of the category that its "\c" switch points to.
builder.insertField("TOA \\c 1 \\h", null);
builder.insertField("TOA \\c 2 \\h", null);
builder.insertBreak(aw.BreakType.PageBreak);

// Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
// from the second TA field whose "\c" switch also points to the first category.
// The second TOA field will have two entries from the other two TA fields.
builder.insertField("TA \\c 2 \\l \"entry 1\"");
builder.insertBreak(aw.BreakType.PageBreak);
builder.insertField("TA \\c 1 \\l \"entry 2\"");
builder.insertBreak(aw.BreakType.PageBreak);
builder.insertField("TA \\c 2 \\l \"entry 3\"");

doc.updateFields();
doc.save(base.artifactsDir + "FieldOptions.TOA.categories.docx");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FieldOptions](../)

