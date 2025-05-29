---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
articleTitle: CreateNavigator
second_title: .NET için Aspose.Words
description: Düğümleri zahmetsizce dolaşmak ve okumak için CompositeNode CreateNavigator yöntemini keşfedin ve veri gezinme deneyiminizi geliştirin.
type: docs
weight: 90
url: /tr/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Düğümleri gezmek ve okumak için kullanılabilen gezgini oluşturur.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Örnekler

XPathNavigator'ın nasıl oluşturulacağını ve daha sonra düğümleri dolaşmak ve okumak için nasıl kullanılacağını gösterir.

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

        // Belge ağacında belgenin ilk bölümü vardır.
        // gövde ve ilk paragraf düğümler olarak, her biri bir öncekinin tek çocuğu olacak şekilde.
        // Gezginin geçebileceği birkaç dal daha eklemek için birkaç tane daha ekleyebiliriz.
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
/// Bileşik düğümün tüm alt düğümlerini dolaşır ve yapıyı bir dizin ağacının stilinde eşler.
/// Boşluk girintisinin miktarı, başlangıç düğümüne göre derinliği belirtir.
/// Yalnızca Çalıştır ise geçerli düğümün metin içeriğini yazdırır.
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
