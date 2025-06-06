---
title: NodeList.ToArray
linktitle: ToArray
articleTitle: ToArray
second_title: Aspose.Words per .NET
description: Converti senza sforzo NodeList in un array con il metodo ToArray, semplificando la manipolazione dei nodi e migliorando il flusso di lavoro di sviluppo web.
type: docs
weight: 40
url: /it/net/aspose.words/nodelist/toarray/
---
## NodeList.ToArray method

Copia tutti i nodi dalla raccolta in un nuovo array di nodi.

```csharp
public Node[] ToArray()
```

### Valore di ritorno

Una serie di nodi.

## Osservazioni

Non dovresti aggiungere/rimuovere nodi durante l'iterazione su una raccolta di nodi perché ciò invalida l'iteratore e richiede aggiornamenti per le raccolte attive.

Per poter aggiungere/rimuovere nodi durante l'iterazione, utilizzare questo metodo per copiare nodi in un array di dimensione fissa e quindi iterare sull'array.

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
* class [NodeList](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
