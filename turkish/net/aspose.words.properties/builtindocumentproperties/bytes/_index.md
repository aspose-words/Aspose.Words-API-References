---
title: BuiltInDocumentProperties.Bytes
linktitle: Bytes
articleTitle: Bytes
second_title: Aspose.Words for .NET
description: BuiltInDocumentProperties Bytes mülk. Belgedeki bayt sayısına ilişkin bir tahmindir C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.properties/builtindocumentproperties/bytes/
---
## BuiltInDocumentProperties.Bytes property

Belgedeki bayt sayısına ilişkin bir tahmindir.

```csharp
public int Bytes { get; set; }
```

## Notlar

Microsoft Word her zaman bu özelliği ayarlamaz.

Aspose.Words bu özelliği güncellemez.

## Örnekler

"İçerik" kategorisinde belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Yerleşik özellikleri kullanarak,
    // kelime/sayfa/karakter sayıları gibi belge istatistiklerini, belgeyi açmadan bakılabilecek meta veriler olarak ele alabiliriz
    // Bu özelliklere Windows Gezgini'nde dosyaya sağ tıklayarak ve Özellikler > Ayrıntılar > İçerik
    // Bu verileri belge içerisinde görüntülemek istiyorsak NUMPAGES, NUMWORDS, NUMCHARS vb. alanları kullanabiliriz.
    // Ayrıca bu değerler Microsoft Word'de Dosya > Özellikler > Gelişmiş Özellikler > İstatistik
    // Sayfa sayısı: PageCount özelliği sayfa sayısını gerçek zamanlı olarak gösterir ve değeri Pages özelliğine atanabilir

     // "Sayfalar" özelliği belgenin sayfa sayısını saklar.
    Assert.AreEqual(6, properties.Pages);

    // "Words", "Characters" ve "CharactersWithSpaces" yerleşik özellikleri ayrıca çeşitli belge istatistiklerini de görüntüler,
    // ancak bunların doğru değerler içermesini beklemeden önce tüm belgede "UpdateWordCount" yöntemini çağırmamız gerekiyor.
    doc.UpdateWordCount();

    Assert.AreEqual(1035, properties.Words);
    Assert.AreEqual(6026, properties.Characters);
    Assert.AreEqual(7041, properties.CharactersWithSpaces);

    // Belgedeki satır sayısını sayın ve ardından sonucu "Satırlar" yerleşik özelliğine atayın.
    LineCounter lineCounter = new LineCounter(doc);
    properties.Lines = lineCounter.GetLineCount();

    Assert.AreEqual(142, properties.Lines);

    // Belgedeki Paragraf düğümlerinin sayısını "Paragraflar" yerleşik özelliğine atayın.
    properties.Paragraphs = doc.GetChildNodes(NodeType.Paragraph, true).Count;
    Assert.AreEqual(29, properties.Paragraphs);

    // "Bayt" yerleşik özelliği aracılığıyla belgemizin dosya boyutuna ilişkin bir tahmin alın.
    Assert.AreEqual(20310, properties.Bytes);

    // Belgemiz için farklı bir şablon ayarlayın ve ardından bu değişikliği yansıtacak şekilde "Şablon" yerleşik özelliğini manuel olarak güncelleyin.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);    

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" açıklayıcı bir yerleşik özelliktir.
    properties.ContentStatus = "Draft";

    // Kaydedildikten sonra "ContentType" yerleşik özelliği, çıktı kaydetme biçiminin MIME türünü içerecektir.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Belgede bağlantılar varsa ve hepsi güncelse "LinksUpToDate" özelliğini "true" olarak ayarlayabiliriz.
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Bir belgedeki satırları sayar.
/// Oluşturma sonrasında belgenin düzen varlıkları ağacını geçer,
/// aynı zamanda gerçek metin de içeren "Çizgi" türündeki varlıkları sayma.
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
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
