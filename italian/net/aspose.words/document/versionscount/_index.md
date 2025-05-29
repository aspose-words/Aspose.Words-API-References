---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words per .NET
description: Scopri la proprietà Document VersionsCount per tenere facilmente traccia del numero di versioni dei documenti archiviate nei tuoi file DOC, per una migliore gestione e organizzazione.
type: docs
weight: 480
url: /it/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Ottiene il numero di versioni del documento memorizzate nel documento DOC.

```csharp
public int VersionsCount { get; }
```

## Osservazioni

Le versioni in Microsoft Word sono accessibili tramite il menu File/Versioni. Microsoft Word supporta le versioni solo per i file DOC.

Questa proprietà consente di rilevare se erano presenti versioni del documento memorizzate in questo documento prima che venisse aperto in Aspose.Words. Aspose.Words non fornisce altro supporto per le versioni del documento. Se si salva questo documento utilizzando Aspose.Words, il documento verrà salvato senza versioni.

## Esempi

Mostra come utilizzare la funzionalità di conteggio delle versioni dei vecchi documenti Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Possiamo leggere questa proprietà di un documento, ma non possiamo conservarla durante il salvataggio.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
