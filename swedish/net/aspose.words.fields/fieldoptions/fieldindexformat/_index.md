---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words för .NET
description: FieldOptions FieldIndexFormat fast egendom. Hämtar eller sätter enFieldIndexFormat som representerar formateringen förFieldIndex fält i dokumentet i C#.
type: docs
weight: 90
url: /sv/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Hämtar eller sätter en`FieldIndexFormat` som representerar formateringen för[`FieldIndex`](../../fieldindex/) fält i dokumentet.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## Exempel

Visar hur man formaterar FieldIndex-fält.

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

### Se även

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
