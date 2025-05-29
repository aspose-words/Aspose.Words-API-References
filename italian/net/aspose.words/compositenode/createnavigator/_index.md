---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words per .NET
description: Scopri il metodo CompositeNode CreateNavigator per attraversare e leggere i nodi senza sforzo, migliorando la tua esperienza di navigazione dei dati.
type: docs
weight: 90
url: /it/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Esempi

Mostra come creare un XPathNavigator e poi utilizzarlo per attraversare e leggere i nodi.

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // L'albero del documento contiene il documento, prima sezione,
        // corpo e primo paragrafo come nodi, ognuno dei quali è figlio unico del precedente.
        // Possiamo aggiungerne altri per dare all'albero qualche ramo che il navigatore possa attraversare.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Utilizziamo il nostro navigatore per stampare sulla console una mappa di tutti i nodi del documento.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Attraversa tutti i figli di un nodo composito e mappa la struttura nello stile di un albero di directory.
/// La quantità di rientro dello spazio indica la profondità relativa al nodo iniziale.
/// Stampa il contenuto di testo del nodo corrente solo se è un Run.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### Guarda anche

* class [CompositeNode](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
