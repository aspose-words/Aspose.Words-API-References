---
title: FieldInclude.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri come utilizzare la proprietà FieldInclude BookmarkName per gestire facilmente i segnalibri nei tuoi documenti, migliorando l'organizzazione e l'efficienza.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldinclude/bookmarkname/
---
## FieldInclude.BookmarkName property

Ottiene o imposta il nome del segnalibro nel documento da includere.

```csharp
public string BookmarkName { get; set; }
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
