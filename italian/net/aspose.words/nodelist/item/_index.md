---
title: NodeList.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words per .NET
description: Accedi facilmente a nodi specifici con la proprietà NodeList Item. Recupera i nodi per indice per una manipolazione dei dati semplificata e una codifica efficiente.
type: docs
weight: 20
url: /it/net/aspose.words/nodelist/item/
---
## NodeList indexer

Recupera un nodo all'indice specificato.

```csharp
public Node this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nell'elenco dei nodi. |

## Osservazioni

L'indice è basato sullo zero.

Sono consentiti indici negativi che indicano l'accesso dalla parte posteriore della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, viene restituito un riferimento null.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, viene restituito un riferimento null.

## Esempi

Mostra come utilizzare gli XPath per navigare in un NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire alcuni nodi con un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

builder.InsertImage(ImageDir + "Logo.jpg");

// Il nostro documento contiene tre nodi Run.
NodeList nodeList = doc.SelectNodes("//Correre");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Utilizzare una doppia barra per selezionare tutti i nodi Esegui
// che sono discendenti indiretti di un nodo Tabella, che sarebbero le esecuzioni all'interno delle due celle che abbiamo inserito.
nodeList = doc.SelectNodes("//Table//Correre");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Le barre singole specificano relazioni dirette discendenti,
// che abbiamo saltato quando abbiamo utilizzato le doppie barre.
Assert.AreEqual(doc.SelectNodes(" //Tabella//Esegui"),
    doc.SelectNodes("//Tabella/Riga/Cella/Paragrafo/Esegui"));

// Accedi alla forma che contiene l'immagine che abbiamo inserito.
nodeList = doc.SelectNodes("//Forma");

Assert.AreEqual(1, nodeList.Count);

Shape shape = (Shape)nodeList[0];
Assert.True(shape.HasImage);
```

### Guarda anche

* class [Node](../../node/)
* class [NodeList](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
