---
title: CompositeNode.SelectNodes
linktitle: SelectNodes
articleTitle: SelectNodes
second_title: Aspose.Words per .NET
description: CompositeNode SelectNodes metodo. Seleziona un elenco di nodi che corrispondono allespressione XPath in C#.
type: docs
weight: 190
url: /it/net/aspose.words/compositenode/selectnodes/
---
## CompositeNode.SelectNodes method

Seleziona un elenco di nodi che corrispondono all'espressione XPath.

```csharp
public NodeList SelectNodes(string xpath)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| xpath | String | L'espressione XPath. |

### Valore di ritorno

Un elenco di nodi che corrispondono alla query XPath.

## Osservazioni

Al momento sono supportate solo le espressioni con nomi di elementi. Le espressioni che utilizzano nomi di attributi non sono supportate.

## Esempi

Mostra come utilizzare un'espressione XPath per verificare se un nodo si trova all'interno di un campo.

```csharp
Document doc = new Document(MyDir + "Mail merge destination - Northwind employees.docx");

// La NodeList risultante da questa espressione XPath conterrà tutti i nodi che troviamo all'interno di un campo.
// Tuttavia, i nodi FieldStart e FieldEnd possono essere presenti nell'elenco se sono presenti campi nidificati nel percorso.
// Attualmente non trova i campi rari in cui FieldCode o FieldResult si estendono su più paragrafi.
NodeList resultList =
    doc.SelectNodes("//FieldStart/following-sibling::node()[following-sibling::FieldEnd]");

// Controlla se l'esecuzione specificata è uno dei nodi all'interno del campo.
Console.WriteLine($"Contents of the first Run node that's part of a field: {resultList.First(n => n.NodeType == NodeType.Run).GetText().Trim()}");
```

Mostra come selezionare determinati nodi utilizzando un'espressione XPath.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Questa espressione estrarrà tutti i nodi del paragrafo,
// che sono discendenti di qualsiasi nodo della tabella nel documento.
NodeList nodeList = doc.SelectNodes("//Tabella//Paragrafo");

// Scorre l'elenco con un enumeratore e stampa il contenuto di ogni paragrafo in ogni cella della tabella.
int index = 0;

using (IEnumerator<Node> e = nodeList.GetEnumerator())
    while (e.MoveNext())
        Console.WriteLine($"Table paragraph index {index++}, contents: \"{e.Current.GetText().Trim()}\"");

// Questa espressione selezionerà tutti i paragrafi che sono figli diretti di qualsiasi nodo Body nel documento.
nodeList = doc.SelectNodes("//Corpo/Paragrafo");

// Possiamo trattare la lista come un array.
Assert.AreEqual(4, nodeList.ToArray().Length);

// Utilizza SelectSingleNode per selezionare il primo risultato della stessa espressione di cui sopra.
Node node = doc.SelectSingleNode("//Corpo/Paragrafo");

Assert.AreEqual(typeof(Paragraph), node.GetType());
```

### Guarda anche

* class [NodeList](../../nodelist/)
* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
