---
title: Range.NormalizeFieldTypes
linktitle: NormalizeFieldTypes
articleTitle: NormalizeFieldTypes
second_title: Aspose.Words for .NET
description: Range NormalizeFieldTypes method. Changes field type values FieldType of FieldStart FieldSeparator FieldEnd in this range so that they correspond to the field types contained in the field codes in C#.
type: docs
weight: 80
url: /net/aspose.words/range/normalizefieldtypes/
---
## Range.NormalizeFieldTypes method

Changes field type values [`FieldType`](../../../aspose.words.fields/fieldchar/fieldtype/) of [`FieldStart`](../../../aspose.words.fields/fieldstart/), [`FieldSeparator`](../../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes.

```csharp
public void NormalizeFieldTypes()
```

## Remarks

Use this method after document changes that affect field types.

To change field type values in the whole document use [`NormalizeFieldTypes`](../../document/normalizefieldtypes/).

## Examples

Shows how to get the keep a field's type up to date with its field code.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE", null);

// Aspose.Words automatically detects field types based on field codes.
Assert.AreEqual(FieldType.FieldDate, field.Type);

// Manually change the raw text of the field, which determines the field code.
Run fieldText = (Run)doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Run, true)[0];
fieldText.Text = "PAGE";

// Changing the field code has changed this field to one of a different type,
// but the field's type properties still display the old type.
Assert.AreEqual("PAGE", field.GetFieldCode());
Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual(FieldType.FieldDate, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldDate, field.End.FieldType);

// Update those properties with this method to display current value.
doc.NormalizeFieldTypes();

Assert.AreEqual(FieldType.FieldPage, field.Type);
Assert.AreEqual(FieldType.FieldPage, field.Start.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.Separator.FieldType);
Assert.AreEqual(FieldType.FieldPage, field.End.FieldType);
```

### See Also

* class [Range](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
