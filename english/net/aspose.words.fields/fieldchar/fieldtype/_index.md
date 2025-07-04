---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words for .NET
description: Discover the FieldChar FieldType property, which reveals the field's type, enhancing your data management and programming efficiency. Learn more now!
type: docs
weight: 10
url: /net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

Returns the type of the field.

```csharp
public FieldType FieldType { get; }
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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
