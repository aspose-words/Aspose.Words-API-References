---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words per .NET
description: Document VersionsCount proprietà. Ottiene il numero di versioni del documento archiviate nel documento DOC in C#.
type: docs
weight: 460
url: /it/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Ottiene il numero di versioni del documento archiviate nel documento DOC.

```csharp
public int VersionsCount { get; }
```

## Osservazioni

È possibile accedere alle versioni in Microsoft Word tramite il menu File/Versioni. Microsoft Word supporta le versioni solo per i file DOC.

Questa proprietà consente di rilevare se esistevano versioni di documenti archiviate in questo document prima che fosse aperto in Aspose.Words. Aspose.Words non fornisce altro supporto per le versioni del documento. Se salvi questo documento utilizzando Aspose.Words, il documento verrà salvato senza versioni.

## Esempi

Mostra come utilizzare la funzionalità di conteggio delle versioni dei documenti Microsoft Word precedenti.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Possiamo leggere questa proprietà di un documento, ma non possiamo preservarla durante il salvataggio.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
