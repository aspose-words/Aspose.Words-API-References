---
title: Document.OriginalLoadFormat
second_title: Aspose.Words per .NET API Reference
description: Document proprietà. Ottiene il formato del documento originale che è stato caricato in questo oggetto.
type: docs
weight: 280
url: /it/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Ottiene il formato del documento originale che è stato caricato in questo oggetto.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

### Osservazioni

Se hai creato un nuovo documento vuoto, restituisce ilDoc valore.

### Esempi

Mostra come recuperare i dettagli dell'operazione di caricamento di un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Guarda anche

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


