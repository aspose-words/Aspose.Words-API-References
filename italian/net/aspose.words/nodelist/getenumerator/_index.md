---
title: NodeList.GetEnumerator
second_title: Aspose.Words per .NET API Reference
description: NodeList metodo. Fornisce una semplice iterazione di stile foreach sulla raccolta di nodi.
type: docs
weight: 30
url: /it/net/aspose.words/nodelist/getenumerator/
---
## NodeList.GetEnumerator method

Fornisce una semplice iterazione di stile "foreach" sulla raccolta di nodi.

```csharp
public IEnumerator<Node> GetEnumerator()
```

### Valore di ritorno

Un IEnumerator.

### Esempi

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

* class [Node](../../node/)
* class [NodeList](../)
* spazio dei nomi [Aspose.Words](../../nodelist/)
* assemblea [Aspose.Words](../../../)


