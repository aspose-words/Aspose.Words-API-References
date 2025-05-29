---
title: FieldInclude.SourceFullName
linktitle: SourceFullName
articleTitle: SourceFullName
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà FieldInclude SourceFullName per gestire in modo efficiente le posizioni dei documenti. Migliora il tuo flusso di lavoro oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldinclude/sourcefullname/
---
## FieldInclude.SourceFullName property

Ottiene o imposta la posizione del documento.

```csharp
public string SourceFullName { get; set; }
```

## Esempi

Mostra come creare un campo INCLUDE e impostarne le proprietà.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Possiamo utilizzare un campo INCLUDE per importare una porzione di un altro documento nel file system locale.
// Il segnalibro dell'altro documento a cui facciamo riferimento con questo campo contiene questa parte importata.
FieldInclude field = (FieldInclude)builder.InsertField(FieldType.FieldInclude, true);
field.SourceFullName = MyDir + "Bookmarks.docx";
field.BookmarkName = "MyBookmark1";
field.LockFields = false;
field.TextConverter = "Microsoft Word";

Assert.True(Regex.Match(field.GetFieldCode(), " INCLUDE .* MyBookmark1 \\\\c \"Microsoft Word\"").Success);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INCLUDE.docx");
```

### Guarda anche

* class [FieldInclude](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
