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

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
