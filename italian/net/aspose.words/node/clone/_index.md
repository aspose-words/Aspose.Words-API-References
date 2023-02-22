---
title: Node.Clone
second_title: Aspose.Words per .NET API Reference
description: Node metodo. Crea un duplicato del nodo.
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
| isCloneChildren | Boolean | True per clonare ricorsivamente il sottoalbero nel nodo specificato; false per clonare solo il nodo stesso. |

### Valore di ritorno

Il nodo clonato.

### Osservazioni

Questo metodo funge da costruttore di copie per i nodi. Il nodo clonato non ha padre, ma appartiene allo stesso documento del nodo originale.

Questo metodo esegue sempre una copia completa del nodo. IlisCloneChildren parametro specifica se eseguire la copia anche di tutti i nodi figlio.

### Esempi

Mostra come clonare un nodo composito.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Di seguito sono riportati due modi per clonare un nodo composito.
// 1 - Crea un clone di un nodo e crea anche un clone di ciascuno dei suoi nodi figlio.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Crea un clone di un nodo da solo senza figli.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Guarda anche

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../node/)
* assemblea [Aspose.Words](../../../)


