---
title: CompositeNode.CreateNavigator
second_title: Aspose.Words for .NET API Referansı
description: CompositeNode yöntem. Sistem kullanımı için ayrılmıştır. IXPathNavigable.
type: docs
weight: 80
url: /tr/net/aspose.words/compositenode/createnavigator/
---
## CompositeNode.CreateNavigator method

Sistem kullanımı için ayrılmıştır. IXPathNavigable.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

### Örnekler

Bir XPathNavigator'ın nasıl oluşturulacağını ve ardından düğümleri geçmek ve okumak için nasıl kullanılacağını gösterir.

```csharp
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // Belge ağacında belge, ilk bölüm,
        // gövde ve düğümler olarak ilk paragraf, her biri bir öncekinin tek çocuğu.
        // Gezginin geçmesi için ağaca bazı dallar vermek için birkaç tane daha ekleyebiliriz.
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

/// <summary>
/// Bileşik düğümün tüm alt öğelerini çaprazlar ve yapıyı bir dizin ağacı stilinde eşler.
/// Boşluk girintisi miktarı, ilk düğüme göre derinliği gösterir.
/// Geçerli düğümün metin içeriğini yalnızca bir Run ise yazdırır.
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
* ad alanı [Aspose.Words](../../compositenode/)
* toplantı [Aspose.Words](../../../)


