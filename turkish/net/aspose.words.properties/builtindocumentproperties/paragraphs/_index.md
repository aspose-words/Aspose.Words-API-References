---
title: BuiltInDocumentProperties.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: .NET için Aspose.Words
description: Belgenizdeki paragraf sayısının doğru bir tahminini sunarak daha iyi içerik yönetimi sağlayan BuiltInDocumentProperties Paragraphs özelliğini keşfedin.
type: docs
weight: 240
url: /tr/net/aspose.words.properties/builtindocumentproperties/paragraphs/
---
## BuiltInDocumentProperties.Paragraphs property

Belgedeki paragraf sayısının bir tahminini temsil eder.

```csharp
public int Paragraphs { get; set; }
```

## Notlar

Aspose.Words, çağırdığınızda bu özelliği günceller[`UpdateWordCount`](../../../aspose.words/document/updatewordcount/).

## Örnekler

Bir belgedeki tüm liste etiketlerinin nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.Write("Ut enim ad minim veniam, " +
                "quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Aspose.Words bu tür belge ölçümlerini gerçek zamanlı olarak izlemez.
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(0, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Paragraphs);
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

// Bu özelliklerden üçünün doğru değerlerini elde etmek için bunları manuel olarak güncellememiz gerekecek.
doc.UpdateWordCount();

Assert.AreEqual(196, doc.BuiltInDocumentProperties.Characters);
Assert.AreEqual(36, doc.BuiltInDocumentProperties.Words);
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Paragraphs);

// Satır sayısı için güncelleme metodunun belirli bir aşırı yüklemesini çağırmamız gerekecek.
Assert.AreEqual(1, doc.BuiltInDocumentProperties.Lines);

doc.UpdateWordCount(true);

Assert.AreEqual(4, doc.BuiltInDocumentProperties.Lines);
```

"İçerik" kategorisindeki belge özellikleriyle nasıl çalışılacağını gösterir.

```csharp
public void Content()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");
    BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

    // Dahili özellikleri kullanarak,
    // Kelime/sayfa/karakter sayıları gibi belge istatistiklerini, belgeyi açmadan göz atılabilecek meta veri olarak ele alabiliriz
    // Bu özelliklere Windows Gezgini'nde dosyaya sağ tıklanarak ve Özellikler > Ayrıntılar > İçerik'e gidilerek erişilebilir
    // Eğer bu verileri doküman içerisinde göstermek istiyorsak NUMPAGES, NUMWORDS, NUMCHARS vb. alanları kullanabiliriz.
    // Ayrıca, bu değerler Microsoft Word'de Dosya > Özellikler > Gelişmiş Özellikler > İstatistikler'e gidilerek de görüntülenebilir
    // Sayfa sayısı: PageCount özelliği, sayfa sayısını gerçek zamanlı olarak gösterir ve değeri Pages özelliğine atanabilir

     // "Sayfalar" özelliği belgenin sayfa sayısını saklar.
    Assert.AreEqual(6, properties.Pages);

    // "Words", "Characters" ve "CharactersWithSpaces" yerleşik özellikleri ayrıca çeşitli belge istatistiklerini görüntüler.
    // ancak bunların doğru değerler içermesini beklemeden önce, tüm belge üzerinde "UpdateWordCount" metodunu çağırmamız gerekir.
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

    // "Bayt" yerleşik özelliği aracılığıyla belgemizin dosya boyutunun bir tahminini alın.
    Assert.AreEqual(20310, properties.Bytes);

    // Belgemiz için farklı bir şablon belirleyelim ve ardından bu değişikliği yansıtmak için yerleşik "Şablon" özelliğini manuel olarak güncelleyelim.
    doc.AttachedTemplate = MyDir + "Business brochure.dotx";

    Assert.AreEqual("Normal", properties.Template);

    properties.Template = doc.AttachedTemplate;

    // "ContentStatus" tanımlayıcı bir yerleşik özelliktir.
    properties.ContentStatus = "Draft";

    // Kaydetme sırasında, "ContentType" yerleşik özelliği, çıktı kaydetme biçiminin MIME türünü içerecektir.
    Assert.AreEqual(string.Empty, properties.ContentType);

    // Belgede bağlantılar varsa ve hepsi güncelse, "LinksUpToDate" özelliğini "true" olarak ayarlayabiliriz.
    Assert.False(properties.LinksUpToDate);

    doc.Save(ArtifactsDir + "DocumentProperties.Content.docx");
}

/// <summary>
/// Bir belgedeki satırları sayar.
/// Oluşturma sırasında belgenin düzen varlıkları ağacını dolaşır,
/// Gerçek metin içeren "Çizgi" türündeki varlıkların sayılması.
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
