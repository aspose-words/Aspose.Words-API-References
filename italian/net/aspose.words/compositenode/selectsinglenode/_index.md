---
title: CompositeNode.SelectSingleNode
linktitle: SelectSingleNode
articleTitle: SelectSingleNode
second_title: Aspose.Words per .NET
description: Scopri come il metodo SelectSingleNode di CompositeNode recupera in modo efficiente il primo nodo che corrisponde alla tua espressione XPath per una gestione semplificata dei dati.
type: docs
weight: 220
url: /it/net/aspose.words/compositenode/selectsinglenode/
---
## CompositeNode.SelectSingleNode method

Seleziona il primo[`Node`](../../node/) che corrisponde all'espressione XPath.

```csharp
public Node SelectSingleNode(string xpath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xpath | String | L'espressione XPath. |

### Valore di ritorno

Il primo[`Node`](../../node/) che corrisponde alla query XPath o`null` se non viene trovato alcun nodo corrispondente.

## Osservazioni

Al momento sono supportate solo le espressioni con nomi di elementi. Le espressioni che utilizzano nomi di attributi non sono supportate.

## Esempi

Mostra come selezionare determinati nodi utilizzando un'espressione XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Questa espressione estrarrà tutti i nodi del paragrafo,
// che sono discendenti di qualsiasi nodo della tabella nel documento.
NodeList nodeList = doc.SelectNodes("//Tabella//Paragrafo");

// Scorrere l'elenco con un enumeratore e stampare il contenuto di ogni paragrafo in ogni cella della tabella.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Questa espressione selezionerà tutti i paragrafi che sono figli diretti di qualsiasi nodo Corpo nel documento.
nodeList = doc.SelectNodes("//Corpo/Paragrafo");

// Possiamo trattare l'elenco come un array.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilizzare SelectSingleNode per selezionare il primo risultato della stessa espressione di cui sopra.
Node node = doc.SelectSingleNode("//Corpo/Paragrafo");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Guarda anche

* class [Node](../../node/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
