---
title: Document.Clone
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Esegue una copia approfondita del fileDocument .
type: docs
weight: 570
url: /it/net/aspose.words/document/clone/
---
## Document.Clone method

Esegue una copia approfondita del file[`Document`](../) .

```csharp
public Document Clone()
```

### Valore di ritorno

Il documento clonato.

### Esempi

Mostra come clonare in profondità un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// La clonazione produrrà un nuovo documento con lo stesso contenuto dell'originale,
// ma con una copia unica di ciascuno dei nodi del documento originale.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(), 
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


