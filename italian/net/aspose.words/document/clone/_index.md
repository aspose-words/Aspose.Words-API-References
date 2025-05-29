---
title: Document.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: Duplica senza sforzo i tuoi documenti con il nostro metodo "Document Clone". Ottieni copie precise e approfondite per un editing fluido e un flusso di lavoro efficiente.
type: docs
weight: 590
url: /it/net/aspose.words/document/clone/
---
## Document.Clone method

Esegue una copia profonda del[`Document`](../) .

```csharp
public Document Clone()
```

### Valore di ritorno

Il documento clonato.

## Esempi

Mostra come clonare in modo approfondito un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

// La clonazione produrrà un nuovo documento con lo stesso contenuto dell'originale,
// ma con una copia univoca di ciascuno dei nodi del documento originale.
Document clone = doc.Clone();

Assert.AreEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetText(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].Text);
Assert.AreNotEqual(doc.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode(),
    clone.FirstSection.Body.FirstParagraph.Runs[0].GetHashCode());
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
