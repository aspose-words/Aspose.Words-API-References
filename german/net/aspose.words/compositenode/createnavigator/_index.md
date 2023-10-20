---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words für .NET
description: CompositeNode CreateNavigator methode. Erstellt einen Navigator der zum Durchlaufen und Lesen von Knoten verwendet werden kann in C#.
type: docs
weight: 70
url: /de/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Erstellt einen Navigator, der zum Durchlaufen und Lesen von Knoten verwendet werden kann.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Beispiele

Zeigt, wie Sie einen XPathNavigator erstellen und ihn dann zum Durchlaufen und Lesen von Knoten verwenden.

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

        // Der Dokumentenbaum enthält das Dokument, den ersten Abschnitt,
        // Hauptteil und erster Absatz als Knoten, wobei jeder ein einziges untergeordnetes Element des vorherigen ist.
        // Wir können noch ein paar weitere hinzufügen, um dem Baum einige Zweige zu geben, die der Navigator durchqueren kann.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Verwenden Sie unseren Navigator, um eine Karte aller Knoten im Dokument auf der Konsole zu drucken.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Durchläuft alle untergeordneten Knoten eines zusammengesetzten Knotens und bildet die Struktur im Stil eines Verzeichnisbaums ab.
/// Die Größe der Leerzeicheneinrückung gibt die Tiefe relativ zum Anfangsknoten an.
/// Gibt den Textinhalt des aktuellen Knotens nur aus, wenn es sich um einen Run handelt.
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

### Siehe auch

* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
