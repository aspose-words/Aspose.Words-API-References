---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words for .NET
description: Discover how to utilize the FieldIndexFormat property in FieldOptions to customize FieldIndex formatting for enhanced document clarity and organization.
type: docs
weight: 90
url: /net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Gets or sets a `FieldIndexFormat` that represents the formatting for the [`FieldIndex`](../../fieldindex/) fields in the document.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

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

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
