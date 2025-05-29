---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà OriginalLoadFormat per accedere facilmente al formato del documento originale caricato nel tuo oggetto, migliorando la gestione dei documenti.
type: docs
weight: 310
url: /it/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Ottiene il formato del documento originale caricato in questo oggetto.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Osservazioni

Se hai creato un nuovo documento vuoto, restituisce ilDoc valore.

## Esempi

Mostra come recuperare i dettagli dell'operazione di caricamento di un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Guarda anche

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
