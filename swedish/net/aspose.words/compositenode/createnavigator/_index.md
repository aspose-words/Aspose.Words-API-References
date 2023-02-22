---
title: CompositeNode.CreateNavigator
second_title: Aspose.Words för .NET API Referens
description: CompositeNode metod. Reserverad för systemanvändning. IXPathNavigable.
type: docs
weight: 80
url: /sv/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Reserverad för systemanvändning. IXPathNavigable.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Exempel

Visar hur man skapar en XPathNavigator och sedan använder den för att korsa och läsa noder.

```csharp
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // Dokumentträdet har dokumentet, första avsnittet,
        // body, och första stycket som noder, där var och en är en enda underordnad av den föregående.
        // Vi kan lägga till några fler för att ge trädet några grenar som navigatorn kan korsa.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Använd vår navigator för att skriva ut en karta över alla noder i dokumentet till konsolen.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
}

/// <summary>
/// Går igenom alla barn i en sammansatt nod och mappar strukturen i stil med ett katalogträd.
/// Mängden rymdfördjupning anger djup i förhållande till den initiala noden.
/// Skriver ut textinnehållet i den aktuella noden endast om det är en körning.
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

### Se även

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../compositenode/)
* hopsättning [Aspose.Words](../../../)


