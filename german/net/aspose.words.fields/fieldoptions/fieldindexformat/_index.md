---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie die FieldIndexFormat-Eigenschaft in FieldOptions nutzen können, um die FieldIndex-Formatierung anzupassen und so die Übersichtlichkeit und Organisation von Dokumenten zu verbessern.
type: docs
weight: 90
url: /de/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Ruft ab oder setzt einen`FieldIndexFormat` das stellt die Formatierung für die[`FieldIndex`](../../fieldindex/) Felder im Dokument.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## Beispiele

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

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
