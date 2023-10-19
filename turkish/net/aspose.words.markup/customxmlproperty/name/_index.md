---
title: CustomXmlProperty.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words for .NET
description: CustomXmlProperty Name mülk. Özel XML niteliğinin veya akıllı etiket özelliğinin adını belirtir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.markup/customxmlproperty/name/
---
## CustomXmlProperty.Name property

Özel XML niteliğinin veya akıllı etiket özelliğinin adını belirtir.

```csharp
public string Name { get; }
```

## Notlar

Olamaz`hükümsüz`.

Varsayılan boş dizedir.

## Örnekler

Akıllı etiketlerin nasıl oluşturulacağını gösterir.

```csharp
public void Create()
{
    Document doc = new Document();

    // Microsoft Word'ün metnin bir bölümünü bir tür veri olarak tanıdığı bir belgede akıllı etiket görünür,
    // ad, tarih veya adres gibi ve onu mor noktalı alt çizgi görüntüleyen bir köprüye dönüştürür.
    SmartTag smartTag = new SmartTag(doc);

    // Akıllı etiketler, tanınan metnin tamamını içeren bileşik düğümlerdir.
    // İçeriği bu akıllı etikete manuel olarak ekleyin.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word yukarıdaki içerikleri tarih olarak tanıyabilir.
    // Akıllı etiketler içerdikleri veri türünü yansıtmak için "Element" özelliğini kullanır.
    smartTag.Element = "date";

    // Bazı akıllı etiket türleri, içeriklerini özel XML özelliklerine göre işler.
    smartTag.Properties.Add(new CustomXmlProperty("Day", string.Empty, "29"));
    smartTag.Properties.Add(new CustomXmlProperty("Month", string.Empty, "5"));
    smartTag.Properties.Add(new CustomXmlProperty("Year", string.Empty, "2019"));

    // Akıllı etiketin URI'sini varsayılan değere ayarlayın.
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a date. "));

    // Hisse senedi takip cihazı için başka bir akıllı etiket oluşturun.
    smartTag = new SmartTag(doc);
    smartTag.Element = "stockticker";
    smartTag.Uri = "urn:schemas-microsoft-com:office:smarttags";

    smartTag.AppendChild(new Run(doc, "MSFT"));

    doc.FirstSection.Body.FirstParagraph.AppendChild(smartTag);
    doc.FirstSection.Body.FirstParagraph.AppendChild(new Run(doc, " is a stock ticker."));

    // Bir belge ziyaretçisi kullanarak belgemizdeki tüm akıllı etiketleri yazdırın.
    doc.Accept(new SmartTagPrinter());

    // Microsoft Word'ün eski sürümleri akıllı etiketleri destekler.
    doc.Save(ArtifactsDir + "SmartTag.Create.doc");

    // Bir belgedeki tüm akıllı etiketleri kaldırmak için "RemoveSmartTags" yöntemini kullanın.
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
    /// SmartTag düğümünün ziyareti sonlandırıldığında çağrılır.
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

* class [CustomXmlProperty](../)
* ad alanı [Aspose.Words.Markup](../../../aspose.words.markup/)
* toplantı [Aspose.Words](../../../)
