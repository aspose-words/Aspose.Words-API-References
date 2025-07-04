---
title: Document.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words for .NET
description: Optimize your document with the NormalizeFieldTypes method, ensuring all field type values align with field codes for enhanced consistency and accuracy.
type: docs
weight: 670
url: /net/aspose.words/document/normalizefieldtypes/
---
## Document.NormalizeFieldTypes method

Changes field type values [`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) of [`FieldStart`](../../../aspose.words.fields/fieldstart/), [`FieldSeparator`](../../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../../aspose.words.fields/fieldend/) in the whole document so that they correspond to the field types contained in the field codes.

```csharp
public void NormalizeFieldTypes()
```

## Remarks

Use this method after document changes that affect field types.

To change field type values in a specific part of the document use [`NormalizeFieldTypes`](../../range/normalizefieldtypes/).

## Examples

Shows how to get the keep a field's type up to date with its field code.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words automatically detects field types based on field codes.
Assert.That(field.Type, Is.EqualTo(FieldType.FieldDate));

// Manually change the raw text of the field, which determines the field code.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Changing the field code has changed this field to one of a different type,
// but the field's type properties still display the old type.
Assert.That(field.GetFieldCode(), Is.EqualTo("PAGE"));
Assert.That(field.Type, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.Start.FieldType, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.Separator.FieldType, Is.EqualTo(FieldType.FieldDate));
Assert.That(field.End.FieldType, Is.EqualTo(FieldType.FieldDate));

// Update those properties with this method to display current value.
doc.NormalizeFieldTypes();

Assert.That(field.Type, Is.EqualTo(FieldType.FieldPage));
Assert.That(field.Start.FieldType, Is.EqualTo(FieldType.FieldPage));
Assert.That(field.Separator.FieldType, Is.EqualTo(FieldType.FieldPage));
Assert.That(field.End.FieldType, Is.EqualTo(FieldType.FieldPage));
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
