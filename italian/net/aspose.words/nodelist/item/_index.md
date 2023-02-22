---
title: NodeList.Item
second_title: Aspose.Words per .NET API Reference
description: NodeList proprietà. Recupera un nodo in corrispondenza dellindice specificato.
type: docs
weight: 20
url: /it/net/aspose.words/nodelist/item/
---
## NodeList indexer

Recupera un nodo in corrispondenza dell'indice specificato.

```csharp
public Node this[int index] { get; }
```

| Parametro | Descrizione |
| --- | --- |
| index | Un indice nell'elenco dei nodi. |

### Osservazioni

L'indice è a base zero.

Gli indici negativi sono consentiti e indicano l'accesso dal retro della raccolta. Ad esempio -1 indica l'ultimo elemento, -2 indica il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nell'elenco, restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nell'elenco, restituisce un riferimento nullo.

### Esempi

Mostra come usare XPath per navigare in una NodeList.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce alcuni nodi con un DocumentBuilder.
builder.Writeln("Hello world!");

builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();

#if NET48 || JAVA
builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
#elif NET5_0_OR_GREATER || __MOBILE__
using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(image);
#endif

// Il nostro documento contiene tre nodi Run.
NodeList nodeList = doc.SelectNodes("//Correre");

Assert.AreEqual(3, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Hello world!"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Usa una doppia barra per selezionare tutti i nodi Run
// che sono discendenti indiretti di un nodo Table, che sarebbero le corse all'interno delle due celle che abbiamo inserito.
nodeList = doc.SelectNodes("//Table//Correre");

Assert.AreEqual(2, nodeList.Count);
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 1"));
Assert.True(nodeList.Any(n => n.GetText().Trim() == "Cell 2"));

// Le singole barre in avanti specificano le relazioni discendenti dirette,
// che abbiamo saltato quando abbiamo usato le doppie barre.
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
* spazio dei nomi [Aspose.Words](../../nodelist/)
* assemblea [Aspose.Words](../../../)


