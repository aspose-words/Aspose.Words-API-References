---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words for .NET
description: Discover the IsLocked property for fields—control recalculation and enhance data integrity. Unlock efficient management of your data results today!
type: docs
weight: 50
url: /net/aspose.words.fields/field/islocked/
---
## Field.IsLocked property

Gets or sets whether the field is locked (should not recalculate its result).

```csharp
public bool IsLocked { get; set; }
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

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
