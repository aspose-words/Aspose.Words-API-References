---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words per .NET
description: Cancella senza sforzo la tua NodeCollection con il nostro metodo Clear, rimuovendo tutti i nodi sia dalla raccolta che dal documento per prestazioni ottimali.
type: docs
weight: 40
url: /it/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Rimuove tutti i nodi da questa raccolta e dal documento.

```csharp
public void Clear()
```

## Esempi

Mostra come rimuovere tutte le sezioni da un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Questo documento ha una sezione con alcuni nodi figlio che contengono e visualizzano tutto il contenuto del documento.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Cancella la raccolta di sezioni, rimuovendo così tutti gli elementi figlio del documento.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Guarda anche

* class [NodeCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
