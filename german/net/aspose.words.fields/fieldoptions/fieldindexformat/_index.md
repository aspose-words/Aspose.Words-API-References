---
title: FieldIndexFormat
second_title: Aspose.Words für .NET-API-Referenz
description: Holt oder setzt aFieldIndexFormataspose.words.fields/fieldoptions/fieldindexformat das repräsentiert die Formatierung für dieFieldIndexaspose.words.fields/fieldindexFelder im Dokument.
type: docs
weight: 80
url: /de/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Holt oder setzt a`FieldIndexFormat` das repräsentiert die Formatierung für die[`FieldIndex`](../../fieldindex)Felder im Dokument.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### Beispiele

Zeigt, wie FieldIndex-Felder formatiert werden.

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

### Siehe auch

* enum [FieldIndexFormat](../../fieldindexformat)
* class [FieldOptions](../../fieldoptions)
* namensraum [Aspose.Words.Fields](../../fieldoptions)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->