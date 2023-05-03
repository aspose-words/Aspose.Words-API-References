---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET API Reference
description: Field Type property. Gets the Microsoft Word field type in C#.
type: docs
weight: 100
url: /net/aspose.words.fields/field/type/
---
## Field.Type property

Gets the Microsoft Word field type.

```csharp
public virtual FieldType Type { get; }
```

## Examples

Shows how to insert a field into a document using a field code.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namespace [Aspose.Words.Fields](../../field/)
* assembly [Aspose.Words](../../../)
