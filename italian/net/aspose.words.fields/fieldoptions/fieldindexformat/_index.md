---
title: FieldOptions.FieldIndexFormat
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words per .NET
description: FieldOptions FieldIndexFormat proprietà. Ottiene o imposta aFieldIndexFormat che rappresenta la formattazione per ilFieldIndex campi nel documento in C#.
type: docs
weight: 90
url: /it/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Ottiene o imposta a`FieldIndexFormat` che rappresenta la formattazione per il[`FieldIndex`](../../fieldindex/) campi nel documento.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

## Esempi

Mostra come formattare i campi FieldIndex.

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

### Guarda anche

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
