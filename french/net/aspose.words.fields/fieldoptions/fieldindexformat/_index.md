---
title: FieldIndexFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: Obtient ou définit unFieldIndexFormataspose.words.fields/fieldoptions/fieldindexformat qui représente la mise en forme duFieldIndexaspose.words.fields/fieldindexchamps dans le document.
type: docs
weight: 80
url: /fr/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Obtient ou définit un`FieldIndexFormat` qui représente la mise en forme du[`FieldIndex`](../../fieldindex)champs dans le document.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### Exemples

Montre comment formater les champs FieldIndex.

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

### Voir également

* enum [FieldIndexFormat](../../fieldindexformat)
* class [FieldOptions](../../fieldoptions)
* espace de noms [Aspose.Words.Fields](../../fieldoptions)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->