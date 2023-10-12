---
title: CompositeNode.CreateNavigator
second_title: Aspose.Words per .NET API Reference
description: CompositeNode metodo. Crea un navigatore che può essere utilizzato per attraversare e leggere i nodi.
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

### Esempi

Mostra come creare un XPathNavigator e quindi usarlo per attraversare e leggere i nodi.

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

        // L'albero del documento ha il documento, prima sezione,
        // corpo e primo paragrafo come nodi, ciascuno dei quali è figlio unico del precedente.
        // Possiamo aggiungerne altri per dare all'albero alcuni rami che il navigatore possa attraversare.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Usa il nostro navigatore per stampare sulla console una mappa di tutti i nodi nel documento.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Attraversa tutti i figli di un nodo composito e mappa la struttura nello stile di un albero di directory.
/// La quantità di rientro dello spazio indica la profondità relativa al nodo iniziale.
/// Stampa il contenuto testuale del nodo corrente solo se è un Run.
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
* spazio dei nomi [Aspose.Words](../../compositenode/)
* assemblea [Aspose.Words](../../../)


