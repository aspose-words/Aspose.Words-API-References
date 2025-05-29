---
title: SmartTag
linktitle: SmartTag
articleTitle: SmartTag
second_title: .NET için Aspose.Words
description: Oluşturucumuzla dinamik SmartTag'leri zahmetsizce oluşturun. Projelerinizi özelleştirilebilir özellikler ve optimum performans için kusursuz entegrasyonla geliştirin.
type: docs
weight: 10
url: /tr/net/aspose.words.markup/smarttag/smarttag/
---
## SmartTag constructor

Yeni bir örneğini başlatır[`SmartTag`](../) sınıf.

```csharp
public SmartTag(DocumentBase doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |

## Notlar

Yeni bir düğüm oluşturduğunuzda, düğümün ait olduğu bir belge belirtmeniz gerekir. Bir düğüm, listeler ve stiller gibi belge çapındaki yapılara bağlı olduğundan belge olmadan var olamaz. Bir düğüm her zaman bir belgeye ait olsa da, bir düğüm belge ağacının bir parçası olabilir veya olmayabilir .

Bir düğüm oluşturulduğunda, bir belgeye aittir ancak henüz belge tree 'nin bir parçası değildir ve[`ParentNode`](../../../aspose.words/node/parentnode/) null'dır. Belgeye bir düğüm eklemek için the kullanın[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) veya[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/)Üst düğümdeki yöntemleri.

## Örnekler

Akıllı etiketlerin nasıl oluşturulacağını gösterir.

```csharp
public void Create()
{
    Document doc = new Document();

    // Microsoft Word'de bir belgede görünen akıllı etiket, metnin bir kısmını bir tür veri olarak tanır,
    // isim, tarih veya adres gibi bir bilgiyi alıp mor noktalı alt çizgi gösteren bir köprü metnine dönüştürür.
    SmartTag smartTag = new SmartTag(doc);

    // Akıllı etiketler, tanınan metinlerini bütünüyle içeren bileşik düğümlerdir.
    // Bu akıllı etikete içerikleri manuel olarak ekleyin.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word yukarıdaki içeriği bir tarih olarak tanıyabilir.
    // Akıllı etiketler, içerdikleri veri türünü yansıtmak için "Element" özelliğini kullanır.
    smartTag.Element = "date";

    // Bazı akıllı etiket türleri içeriklerini daha sonra özel XML özelliklerine işler.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Akıllı etiketin URI'sini varsayılan değere ayarlayın.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Bir hisse senedi için başka bir akıllı etiket oluşturun.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Belge ziyaretçisini kullanarak belgemizdeki tüm akıllı etiketleri yazdır.
    doc.Accept(new SmartTagPrinter());

    // Microsoft Word'ün eski sürümleri akıllı etiketleri destekler.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Bir belgeden tüm akıllı etiketleri kaldırmak için "RemoveSmartTags" yöntemini kullanın.
    Assert.AreEqual(2, doc.GetChildNodes(NodeType.SmartTag, true).Count);

    doc.RemoveSmartTags();

    Assert.AreEqual(0, doc.GetChildNodes(NodeType.SmartTag, true).Count);
}

/// <summary>
/// Ziyaret edilen akıllı etiketleri ve içeriklerini yazdırır.
/// </summary>
private class SmartTagPrinter : DocumentVisitor
{
    /// <summary>
    /// Belgede bir SmartTag düğümüyle karşılaşıldığında çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagStart(SmartTag smartTag)
    {
        Console.WriteLine($"Smart tag type: {smartTag.Element}");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Bir SmartTag düğümünün ziyareti sona erdiğinde çağrılır.
    /// </summary>
    public override VisitorAction VisitSmartTagEnd(SmartTag smartTag)
    {
        Console.WriteLine($"\tContents: \"{smartTag.ToString(SaveFormat.Text)}\"");

        if (smartTag.Properties.Count == 0)
        {
            Console.WriteLine("\tContains no properties");
        }
        else
        {
            Console.Write("\tProperties: ");
            string[] properties = new string[smartTag.Properties.Count];
            int index = 0;

            foreach (CustomXmlProperty cxp in smartTag.Properties)
                properties[index++] = $"\"{cxp.Name}\" = \"{cxp.Value}\"";

            Console.WriteLine(string.Join(", ", properties));
        }

        return VisitorAction.Continue;
    }
}
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [SmartTag](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
