---
title: NodeCollection.Clear
second_title: Aspose.Words per .NET API Reference
description: NodeCollection metodo. Rimuove tutti i nodi da questa raccolta e dal documento.
type: docs
weight: 40
url: /it/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Rimuove tutti i nodi da questa raccolta e dal documento.

```csharp
public void Clear()
```

### Esempi

Mostra come rimuovere tutte le sezioni da un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Questo documento ha una sezione con alcuni nodi figli che contengono e visualizzano tutti i contenuti del documento.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Cancella la raccolta di sezioni, rimuovendo così tutti i figli del documento.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Guarda anche

* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../nodecollection/)
* assemblea [Aspose.Words](../../../)


