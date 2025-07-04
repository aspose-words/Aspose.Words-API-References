---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words for .NET
description: Discover how the FieldChar IsDirty property helps maintain document accuracy by tracking changes, ensuring your fields always reflect the latest updates.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.

```csharp
public bool IsDirty { get; set; }
```

## Examples

Shows how to work with a FieldStart node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.That(fieldStart.FieldType, Is.EqualTo(FieldType.FieldDate));
Assert.That(fieldStart.IsDirty, Is.EqualTo(false));
Assert.That(fieldStart.IsLocked, Is.EqualTo(false));

// Retrieve the facade object which represents the field in the document.
field = (FieldDate)fieldStart.GetField();

Assert.That(field.IsLocked, Is.EqualTo(false));
Assert.That(field.GetFieldCode(), Is.EqualTo(" DATE  \\@ \"dddd, MMMM dd, yyyy\""));

// Update the field to show the current date.
field.Update();
```

### See Also

* class [FieldChar](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
