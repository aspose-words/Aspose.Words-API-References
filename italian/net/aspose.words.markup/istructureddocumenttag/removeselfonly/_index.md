---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words per .NET
description: Scopri il metodo RemoveSelfOnly di IStructuredDocumentTag per rimuovere senza sforzo un nodo SDT, preservandone il contenuto nell'albero dei documenti.
type: docs
weight: 180
url: /it/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Rimuove solo questo nodo SDT, ma ne mantiene il contenuto all'interno dell'albero del documento.

```csharp
public void RemoveSelfOnly()
```

## Esempi

Mostra come rimuovere il tag del documento strutturato, mantenendone però il contenuto al suo interno.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Questa raccolta fornisce un'interfaccia unificata per accedere ai tag strutturati con e senza intervallo.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Qui possiamo ottenere i nodi figlio dall'interfaccia comune dei tag strutturati con e senza intervallo.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Guarda anche

* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
