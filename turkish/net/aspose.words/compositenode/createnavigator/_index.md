---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: Aspose.Words for .NET
description: CompositeNode CreateNavigator yöntem. Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Düğümlerin arasında geçiş yapmak ve düğümleri okumak için kullanılabilecek gezgini oluşturur.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Örnekler

Bir XPathNavigator'ın nasıl oluşturulacağını ve ardından düğümlerin arasında geçiş yapmak ve düğümleri okumak için nasıl kullanılacağını gösterir.

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

        // Belge ağacında belgenin ilk bölümü bulunur,
        // gövde ve ilk paragraf düğüm olarak; her biri bir öncekinin tek çocuğu olacak.
        // Ağaca, gezginin geçebileceği birkaç dal vermek için birkaç tane daha ekleyebiliriz.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Belgedeki tüm düğümlerin haritasını konsola yazdırmak için gezginimizi kullanın.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Bileşik bir düğümün tüm alt öğelerini çaprazlar ve yapıyı bir dizin ağacı tarzında eşler.
/// Boşluk girintisinin miktarı, ilk düğüme göre derinliği belirtir.
/// Geçerli düğümün metin içeriğini yalnızca Çalıştırma olması durumunda yazdırır.
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

### Ayrıca bakınız

* class [CompositeNode](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
