---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: Duplica i nodi senza sforzo con il metodo Node Clone. Migliora il tuo processo di sviluppo e ottimizza l'efficienza dei progetti oggi stesso!
type: docs
weight: 100
url: /it/net/aspose.words/node/clone/
---
## Node.Clone method

Crea un duplicato del nodo.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| isCloneChildren | Boolean | True per clonare ricorsivamente il sottoalbero sotto il nodo specificato; false per clonare solo il nodo stesso. |

### Valore di ritorno

Il nodo clonato.

## Osservazioni

Questo metodo funge da costruttore di copie per i nodi. Il nodo clonato non ha un elemento padre, ma appartiene allo stesso documento del nodo originale.

Questo metodo esegue sempre una copia profonda del nodo.*isCloneChildren* parameter specifica se eseguire anche la copia di tutti i nodi figlio.

## Esempi

Mostra come clonare un nodo composito.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Di seguito sono riportati due metodi per clonare un nodo composito.
// 1 - Crea un clone di un nodo e crea anche un clone di ciascuno dei suoi nodi figlio.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Crea un clone di un nodo senza alcun elemento figlio.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Guarda anche

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
