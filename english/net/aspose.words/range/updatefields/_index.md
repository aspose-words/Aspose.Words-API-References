---
title: Range.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: Aspose.Words for .NET
description: Enhance your documents effortlessly with the Range UpdateFields method, updating field values quickly and efficiently for improved accuracy.
type: docs
weight: 130
url: /net/aspose.words/range/updatefields/
---
## Range.UpdateFields method

Updates the values of document fields in this range.

```csharp
public void UpdateFields()
```

## Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [`UpdatePageLayout`](../../document/updatepagelayout/).

To update fields in the whole document use [`UpdateFields`](../../document/updatefields/).

## Examples

Shows how to update all the fields in a range.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" DOCPROPERTY Category");
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.InsertField(" DOCPROPERTY Category");

// The above DOCPROPERTY fields will display the value of this built-in document property.
doc.BuiltInDocumentProperties.Category = "MyCategory";

// If we update the value of a document property, we will need to update all the DOCPROPERTY fields to display it.
Assert.That(doc.Range.Fields[0].Result, Is.EqualTo(string.Empty));
Assert.That(doc.Range.Fields[1].Result, Is.EqualTo(string.Empty));

// Update all the fields that are in the range of the first section.
doc.FirstSection.Range.UpdateFields();

Assert.That(doc.Range.Fields[0].Result, Is.EqualTo("MyCategory"));
Assert.That(doc.Range.Fields[1].Result, Is.EqualTo(string.Empty));
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
