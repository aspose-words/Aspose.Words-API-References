---
title: LoadOptions.UpdateDirtyFields
linktitle: UpdateDirtyFields
articleTitle: UpdateDirtyFields
second_title: Aspose.Words for .NET
description: Discover how the LoadOptions UpdateDirtyFields property enhances data integrity by selectively updating fields marked as dirty for optimal performance.
type: docs
weight: 170
url: /net/aspose.words.loading/loadoptions/updatedirtyfields/
---
## LoadOptions.UpdateDirtyFields property

Specifies whether to update the fields with the `dirty` attribute.

```csharp
public bool UpdateDirtyFields { get; set; }
```

## Examples

Shows how to use special property for updating field result.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Give the document's built-in "Author" property value, and then display it with a field.
doc.BuiltInDocumentProperties.Author = "John Doe";
FieldAuthor field = (FieldAuthor)builder.InsertField(FieldType.FieldAuthor, true);

Assert.That(field.IsDirty, Is.False);
Assert.That(field.Result, Is.EqualTo("John Doe"));

// Update the property. The field still displays the old value.
doc.BuiltInDocumentProperties.Author = "John & Jane Doe";

Assert.That(field.Result, Is.EqualTo("John Doe"));

// Since the field's value is out of date, we can mark it as "dirty".
// This value will stay out of date until we update the field manually with the Field.Update() method.
field.IsDirty = true;

using (MemoryStream docStream = new MemoryStream())
{
    // If we save without calling an update method,
    // the field will keep displaying the out of date value in the output document.
    doc.Save(docStream, SaveFormat.Docx);

    // The LoadOptions object has an option to update all fields
    // marked as "dirty" when loading the document.
    LoadOptions options = new LoadOptions();
    options.UpdateDirtyFields = updateDirtyFields;
    doc = new Document(docStream, options);

    Assert.That(doc.BuiltInDocumentProperties.Author, Is.EqualTo("John & Jane Doe"));

    field = (FieldAuthor)doc.Range.Fields[0];

    // Updating dirty fields like this automatically set their "IsDirty" flag to false.
    if (updateDirtyFields)
    {
        Assert.That(field.Result, Is.EqualTo("John & Jane Doe"));
        Assert.That(field.IsDirty, Is.False);
    }
    else
    {
        Assert.That(field.Result, Is.EqualTo("John Doe"));
        Assert.That(field.IsDirty, Is.True);
    }
}
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
