---
title: SmartTag.Accept
second_title: Aspose.Words for .NET API Referansı
description: SmartTag yöntem. Bir ziyaretçiyi kabul eder.
type: docs
weight: 60
url: /tr/net/aspose.words.markup/smarttag/accept/
---
## SmartTag.Accept method

Bir ziyaretçiyi kabul eder.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| visitor | DocumentVisitor | Düğümleri ziyaret edecek ziyaretçi. |

### Geri dönüş değeri

Tüm düğümler ziyaret edildiyse doğrudur; DocumentVisitor tüm düğümleri ziyaret etmeden önce işlemi durdurduysa false.

### Notlar

Bu düğüm ve tüm alt öğeleri üzerinde numaralandırır. Her düğüm, DocumentVisitor'da karşılık gelen bir yöntemi çağırır.

Daha fazla bilgi için Ziyaretçi tasarım modeline bakın.

Çağrılar[`VisitSmartTagStart`](../../../aspose.words/documentvisitor/visitsmarttagstart/) , sonra arar[`Accept`](../../../aspose.words/node/accept/)akıllı etiketin ve çağrıların all alt düğümleri için[`VisitSmartTagEnd`](../../../aspose.words/documentvisitor/visitsmarttagend/) sonunda.

### Örnekler

Akıllı etiketlerin nasıl oluşturulacağını gösterir.

```csharp
public void Create()
{
    Document doc = new Document();

    // Microsoft Word ile bir belgede bir akıllı etiket görünür, metninin bir bölümünü bir tür veri olarak tanır,
    // ad, tarih veya adres gibi ve onu mor noktalı alt çizgi görüntüleyen bir köprüye dönüştürür.
    SmartTag smartTag = new SmartTag(doc);

    // Akıllı etiketler, tanınan metinlerini bütünüyle içeren bileşik düğümlerdir.
    // Bu akıllı etikete manuel olarak içerik ekleyin.
    smartTag.AppendChild(new Run(doc, "May 29, 2019"));

    // Microsoft Word, yukarıdaki içeriği bir tarih olarak tanıyabilir.
    // Akıllı etiketler, içerdikleri veri türünü yansıtmak için "Element" özelliğini kullanır.
    smartTag.Element = "date";

    // Bazı akıllı etiket türleri, içeriklerini daha fazla özel XML özelliklerine işler.
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

    // Bir belge ziyaretçisi kullanarak belgemizdeki tüm akıllı etiketleri yazdırın.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [SmartTag](../)
* ad alanı [Aspose.Words.Markup](../../smarttag/)
* toplantı [Aspose.Words](../../../)


