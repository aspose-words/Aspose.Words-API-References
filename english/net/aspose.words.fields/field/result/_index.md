---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words for .NET
description: Field Result property. Gets or sets text that is between the field separator and field end in C#.
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

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// This overload of the InsertField method automatically updates inserted fields.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### See Also

* class [Field](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
