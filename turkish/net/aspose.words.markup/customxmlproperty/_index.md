---
title: CustomXmlProperty Class
linktitle: CustomXmlProperty
articleTitle: CustomXmlProperty
second_title: .NET için Aspose.Words
description: Gelişmiş belge denetimi için özel XML niteliklerini ve akıllı etiket özelliklerini yönetmeyi basitleştirmek üzere tasarlanmış Aspose.Words.Markup.CustomXmlProperty sınıfını keşfedin.
type: docs
weight: 4630
url: /tr/net/aspose.words.markup/customxmlproperty/
---
## CustomXmlProperty class

Tek bir özel XML niteliğini veya akıllı etiket özelliğini temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yapılandırılmış Belge Etiketleri veya İçerik Denetimi](https://docs.aspose.com/words/net/working-with-content-control-sdt/) belgeleme makalesi.

```csharp
public class CustomXmlProperty
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [CustomXmlProperty](customxmlproperty/)(*string, string, string*) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Name](../../aspose.words.markup/customxmlproperty/name/) { get; } | Özel XML niteliğinin veya akıllı etiket özelliğinin adını belirtir. |
| [Uri](../../aspose.words.markup/customxmlproperty/uri/) { get; set; } | Özel XML niteliğinin veya akıllı etiket özelliğinin ad alanı URI'sini alır veya ayarlar. |
| [Value](../../aspose.words.markup/customxmlproperty/value/) { get; set; } | Özel XML niteliğinin veya akıllı etiket özelliğinin değerini alır veya ayarlar. |

## Notlar

Bir eşyanın parçası olarak kullanıldı[`CustomXmlPropertyCollection`](../customxmlpropertycollection/) koleksiyon.

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

* ad alanı [Aspose.Words.Markup](../../aspose.words.markup/)
* toplantı [Aspose.Words](../../)
