---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words per .NET
description: Scopri il metodo Node Remove per staccare senza sforzo i nodi dal loro elemento padre, migliorando l'efficienza e la struttura del tuo codice.
type: docs
weight: 150
url: /it/net/aspose.words/node/remove/
---
## Node.Remove method

Si rimuove dal genitore.

```csharp
public void Remove()
```

## Esempi

Mostra come eliminare tutte le forme con immagini da un documento.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Mostra come rimuovere tutti i nodi figlio di un tipo specifico da un nodo composito.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Salva il nodo fratello successivo come variabile nel caso in cui volessimo spostarci su di esso dopo aver eliminato questo nodo.
    Node nextNode = curNode.NextSibling;

    // Il corpo di una sezione può contenere nodi Paragrafo e Tabella.
    // Se il nodo è una tabella, rimuoverla dal padre.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
```

### Guarda anche

* class [Node](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
