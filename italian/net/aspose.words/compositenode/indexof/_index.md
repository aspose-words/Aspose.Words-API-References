---
title: CompositeNode.IndexOf
linktitle: IndexOf
articleTitle: IndexOf
second_title: Aspose.Words per .NET
description: Scopri come il metodo CompositeNode IndexOf individua in modo efficiente l'indice di un nodo figlio specificato nell'array, migliorando la tua esperienza di codifica.
type: docs
weight: 140
url: /it/net/aspose.words/compositenode/indexof/
---
## CompositeNode.IndexOf method

Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio.

```csharp
public int IndexOf(Node child)
```

## Osservazioni

Restituisce -1 se il nodo non viene trovato nei nodi figlio.

## Esempi

Mostra come ottenere l'indice di un dato nodo figlio dal suo padre.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

Body body = doc.FirstSection.Body;

// Recupera l'indice dell'ultimo paragrafo nel corpo della prima sezione.
Assert.AreEqual(24, body.GetChildNodes(NodeType.Any, false).IndexOf(body.LastParagraph));
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
