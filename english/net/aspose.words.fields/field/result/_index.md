---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: Manage Field Result properties effortlessly. Access or modify text between field separators for streamlined data handling and enhanced efficiency.
type: docs
weight: 70
url: /net/aspose.words.fields/field/result/
---
## Field.Result property

Gets or sets text that is between the field separator and field end.

```csharp
public string Result { get; set; }
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

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
