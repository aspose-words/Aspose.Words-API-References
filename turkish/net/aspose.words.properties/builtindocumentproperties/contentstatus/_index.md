---
title: BuiltInDocumentProperties.ContentStatus
second_title: Aspose.Words for .NET API Referansı
description: BuiltInDocumentProperties mülk. Belgenin ContentStatusunu alır veya ayarlar.
type: docs
weight: 80
url: /tr/net/aspose.words.properties/builtindocumentproperties/contentstatus/
---
## BuiltInDocumentProperties.ContentStatus property

Belgenin ContentStatus'unu alır veya ayarlar.

```csharp
public string ContentStatus { get; set; }
```

### Örnekler

"İçerik" kategorisindeki belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Yerleşik özellikleri kullanarak,
    // kelime/sayfa/karakter sayıları gibi belge istatistiklerini, belgeyi açmadan bakılabilen meta veriler olarak değerlendirebiliriz
    // Bu özelliklere, Windows Gezgini'nde dosyaya sağ tıklanarak ve Özellikler > Ayrıntılar > İçerik
    // Bu veriyi belge içinde görüntülemek istiyorsak NUMPAGES, NUMWORDS, NUMCHARS vb. alanları kullanabiliriz.
    // Ayrıca, bu değerler Microsoft Word'de Dosya > Özellikler > Gelişmiş Özellikler > İstatistik
    // Sayfa sayısı: PageCount özelliği sayfa sayısını gerçek zamanlı olarak gösterir ve değeri Pages özelliğine atanabilir

    // "Sayfalar" özelliği, belgenin sayfa sayısını saklar. 
    Assert.AreEqual(6, properties.Pages);

    // "Words", "Characters" ve "CharactersWithSpaces" yerleşik özellikleri ayrıca çeşitli belge istatistiklerini görüntüler,
    // ancak doğru değerler içermelerini beklemeden önce tüm belgede "UpdateWordCount" yöntemini çağırmamız gerekiyor.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Belgedeki satır sayısını sayın ve sonucu "Satırlar" yerleşik özelliğine atayın.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Belgedeki Paragraf düğümlerinin sayısını yerleşik "Paragraflar" özelliğine atayın.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // "Bytes" yerleşik özelliği aracılığıyla belgemizin dosya boyutunun bir tahminini alın.
    Assert.AreEqual(20310, properties.Bytes);

    // Belgemiz için farklı bir şablon ayarlayın ve ardından bu değişikliği yansıtmak için "Şablon" yerleşik özelliğini manuel olarak güncelleyin.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus", açıklayıcı yerleşik bir özelliktir.
    properties.ContentStatus = "Draft";

    // Kaydettikten sonra, "ContentType" yerleşik özelliği, çıktı kaydetme biçiminin MIME türünü içerecektir.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Belge bağlantılar içeriyorsa ve hepsi güncelse, "LinksUpToDate" özelliğini "true" olarak ayarlayabiliriz.
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Bir belgedeki satırları sayar.
/// Oluşturma sırasında belgenin yerleşim varlıkları ağacında çapraz geçiş yapar,
/// aynı zamanda gerçek metin de içeren "Satır" türündeki varlıkları sayma.
/// </summary>
private class LineCounter
{
    public LineCounter(Document doc)
    {
        mLayoutEnumerator = new LayoutEnumerator(doc);

        CountLines();
    }

    public int GetLineCount()
    {
        return mLineCount;
    }

    private void CountLines()
    {
        do
        {
            if (mLayoutEnumerator.Type == LayoutEntityType.Line)
            {
                mScanningLineForRealText = true;
            }

            if (mLayoutEnumerator.MoveFirstChild())
            {
                if (mScanningLineForRealText && mLayoutEnumerator.Kind.StartsWith("TEXT"))
                {
                    mLineCount++;
                    mScanningLineForRealText = false;
                }
                CountLines();
                mLayoutEnumerator.MoveParent();
            }
        } while (mLayoutEnumerator.MoveNext());
    }

    private readonly LayoutEnumerator mLayoutEnumerator;
    private int mLineCount;
    private bool mScanningLineForRealText;
}
```

### Ayrıca bakınız

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../builtindocumentproperties/)
* toplantı [Aspose.Words](../../../)


