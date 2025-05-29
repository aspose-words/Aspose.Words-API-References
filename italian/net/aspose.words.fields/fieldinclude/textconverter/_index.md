---
title: FieldInclude.TextConverter
linktitle: TextConverter
articleTitle: TextConverter
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldInclude TextConverter: gestisci facilmente le conversioni dei formati di file con nomi di convertitori di testo personalizzabili per una maggiore efficienza del flusso di lavoro.
type: docs
weight: 50
url: /it/net/aspose.words.fields/fieldinclude/textconverter/
---
## FieldInclude.TextConverter property

Ottiene o imposta il nome del convertitore di testo per il formato del file incluso.

```csharp
public string TextConverter { get; set; }
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
