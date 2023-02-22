---
title: IsDirty
second_title: Aspose.Words for .NET API Reference
description: FieldChar property. Gets or sets whether the current result of the field is no longer correct stale due to other modifications made to the document in C#.
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

* class [FieldChar](../)
* namespace [Aspose.Words.Fields](../../fieldchar/)
* assembly [Aspose.Words](../../../)
