---
title: IStructuredDocumentTag.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words per .NET
description: Scopri il metodo IStructuredDocumentTag GetChildNodes e accedi a una raccolta dinamica di nodi figlio personalizzati in base ai tipi specificati per una gestione avanzata dei documenti.
type: docs
weight: 170
url: /it/net/aspose.words.markup/istructureddocumenttag/getchildnodes/
---
## IStructuredDocumentTag.GetChildNodes method

Restituisce una raccolta live di nodi figlio che corrispondono ai tipi specificati.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
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

* class [NodeCollection](../../../aspose.words/nodecollection/)
* enum [NodeType](../../../aspose.words/nodetype/)
* interface [IStructuredDocumentTag](../)
* spazio dei nomi [Aspose.Words.Markup](../../../aspose.words.markup/)
* assemblea [Aspose.Words](../../../)
