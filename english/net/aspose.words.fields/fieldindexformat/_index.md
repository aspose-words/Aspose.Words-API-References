---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words for .NET
description: Aspose.Words.Fields.FieldIndexFormat enum. Specifies the formatting for the FieldIndex fields in a document in C#.
type: docs
weight: 2420
url: /net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Specifies the formatting for the [`FieldIndex`](../fieldindex/) fields in a document.

```csharp
public enum FieldIndexFormat
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Template | `0` | From template. |
| Classic | `1` | Classic. |
| Fancy | `2` | Fancy. |
| Modern | `3` | Modern. |
| Bulleted | `4` | Bulleted. |
| Formal | `5` | Formal. |
| Simple | `6` | Simple. |

## Examples

Shows how to formatting FieldIndex fields.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
