---
title: FieldBuilder.FieldBuilder
second_title: Aspose.Words for .NET API Reference
description: FieldBuilder constructor. Initializes an instance of the FieldBuilder class in C#.
type: docs
weight: 10
url: /net/aspose.words.fields/fieldbuilder/fieldbuilder/
---
## FieldBuilder constructor

Initializes an instance of the [`FieldBuilder`](../) class.

```csharp
public FieldBuilder(FieldType fieldType)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fieldType | FieldType | The type of the field to build. |

## Examples

Shows how to create and insert a field using a field builder.

```csharp
Document doc = new Document();

// A convenient way of adding text content to a document is with a document builder.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write(" Hello world! This text is one Run, which is an inline node.");

// Fields have their builder, which we can use to construct a field code piece by piece.
// In this case, we will construct a BARCODE field representing a US postal code,
// and then insert it in front of a Run.
FieldBuilder fieldBuilder = new FieldBuilder(FieldType.FieldBarcode);
fieldBuilder.AddArgument("90210");
fieldBuilder.AddSwitch("\\f", "A");
fieldBuilder.AddSwitch("\\u");

fieldBuilder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph.Runs[0]);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CreateWithFieldBuilder.docx");
```

### See Also

* enum [FieldType](../../fieldtype/)
* class [FieldBuilder](../)
* namespace [Aspose.Words.Fields](../../fieldbuilder/)
* assembly [Aspose.Words](../../../)
