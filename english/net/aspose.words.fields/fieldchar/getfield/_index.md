---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: Aspose.Words for .NET
description: Discover the GetField method in FieldChar, effortlessly retrieve fields for optimal data management and enhanced performance in your applications.
type: docs
weight: 40
url: /net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

Returns a field for the field char.

```csharp
public Field GetField()
```

### Return Value

A field for the field char.

## Remarks

A new [`Field`](../../field/) object is created each time the method is called.

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

* class [Field](../../field/)
* class [FieldChar](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
