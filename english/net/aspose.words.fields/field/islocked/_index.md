---
title: Field.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words for .NET
description: Field IsLocked property. Gets or sets whether the field is locked should not recalculate its result in C#.
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

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// Retrieve the facade object which represents the field in the document.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Update the field to show the current date.
field.Update();
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../field/)
* assembly [Aspose.Words](../../../)
