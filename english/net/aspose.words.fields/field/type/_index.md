---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the Microsoft Word field type with our Field Type property. Enhance your documents with precise formatting and dynamic content capabilities.
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

Assert.That(field.Type, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.GetFieldCode(), Is.EqualTo("DATE \\@ \"dddd, MMMM dd, yyyy\""));

// This overload of the InsertField method automatically updates inserted fields.
Assert.That((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1, Is.True);
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
