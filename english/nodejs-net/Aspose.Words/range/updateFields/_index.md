---
title: Range.updateFields method
linktitle: updateFields method
articleTitle: updateFields method
second_title: Aspose.Words for Node.js
description: "Range.updateFields method. Updates the values of document fields in this range."
type: docs
weight: 130
url: /nodejs-net/aspose.words/range/updateFields/
---

## updateFields() {#default}

Updates the values of document fields in this range.


```js
updateFields()
```

### Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.updatePageLayout()](../../document/updatePageLayout/#default).

To update fields in the whole document use [Document.updateFields()](../../document/updateFields/#default).




### Examples

Shows how to update all the fields in a range.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertField(" DOCPROPERTY Category");
builder.insertBreak(aw.BreakType.SectionBreakEvenPage);
builder.insertField(" DOCPROPERTY Category");

// The above DOCPROPERTY fields will display the value of this built-in document property.
doc.builtInDocumentProperties.category = "MyCategory";

// If we update the value of a document property, we will need to update all the DOCPROPERTY fields to display it.
expect(doc.range.fields.at(0).result).toEqual('');
expect(doc.range.fields.at(1).result).toEqual('');

// Update all the fields that are in the range of the first section.
doc.firstSection.range.updateFields();

expect(doc.range.fields.at(0).result).toEqual("MyCategory");
expect(doc.range.fields.at(1).result).toEqual('');
```

### See Also

* module [Aspose.Words](../../)
* class [Range](../)

