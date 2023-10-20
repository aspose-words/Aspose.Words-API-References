---
title: NodeCollection.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words pour .NET
description: NodeCollection Clear méthode. Supprime tous les nœuds de cette collection et du document en C#.
type: docs
weight: 40
url: /fr/net/aspose.words/nodecollection/clear/
---
## NodeCollection.Clear method

Supprime tous les nœuds de cette collection et du document.

```csharp
public void Clear()
```

## Exemples

Montre comment supprimer toutes les sections d’un document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Ce document comporte une section avec quelques nœuds enfants contenant et affichant tout le contenu du document.
Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual(17, doc.Sections[0].GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual("Hello World!\r\rHello Word!\r\r\rHello World!", doc.GetText().Trim());

// Efface la collection de sections, ce qui supprimera tous les enfants du document.
doc.Sections.Clear();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Any, true).Count);
Assert.AreEqual(string.Empty, doc.GetText().Trim());
```

### Voir également

* class [NodeCollection](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
