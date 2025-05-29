---
title: PageSetup.DifferentFirstPageHeaderFooter
linktitle: DifferentFirstPageHeaderFooter
articleTitle: DifferentFirstPageHeaderFooter
second_title: .NET için Aspose.Words
description: Belgenizin ilk sayfasını profesyonel bir dokunuş için benzersiz üstbilgiler ve altbilgilerle özelleştirmek üzere PageSetup DifferentFirstPageHeaderFooter özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words/pagesetup/differentfirstpageheaderfooter/
---
## PageSetup.DifferentFirstPageHeaderFooter property

İlk sayfada farklı bir üstbilgi veya altbilgi kullanılıyorsa doğrudur.

```csharp
public bool DifferentFirstPageHeaderFooter { get; set; }
```

## Örnekler

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Birincil üstbilgilerin/altbilgilerin nasıl etkinleştirileceğini veya devre dışı bırakılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda iki tip başlık/altbilgi bulunmaktadır.
// 1 - Bölümün ilk sayfasında görünen "İlk" başlık/altbilgi.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Writeln("First page header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterFirst);
builder.Writeln("First page footer.");

// 2 - Bölümün her sayfasında görünen "Birincil" üstbilgi/altbilgi.
// Birincil üstbilgi/altbilgiyi birinci ve çift sayfa üstbilgi/altbilgisiyle geçersiz kılabiliriz.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("Primary header.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("Primary footer.");

builder.MoveToSection(0);
builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Her bölümün, sayfa görünümüyle ilgili özellikleri belirten bir "PageSetup" nesnesi vardır
// Yönlendirme, boyut ve kenarlıklar gibi.
// İlk üstbilgi/altbilgiyi ilk sayfaya uygulamak için "DifferentFirstPageHeaderFooter" özelliğini "true" olarak ayarlayın.
// "DifferentFirstPageHeaderFooter" özelliğini "false" olarak ayarlayın
// ilk sayfanın birincil üstbilgi/altbilgiyi görüntülemesini sağlamak için.
builder.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;

doc.Save(ArtifactsDir + "PageSetup.DifferentFirstPageHeaderFooter.docx");
```

Bir metin değiştirme işleminin düğümleri hangi sırayla geçtiğinin nasıl izleneceğini gösterir.

```csharp
public void Order(bool differentFirstPageHeaderFooter)
{
    Document doc = new Document(MyDir + "Header and footer types.docx");

    Section firstPageSection = doc.FirstSection;

    ReplaceLog logger = new ReplaceLog();
    FindReplaceOptions options = new FindReplaceOptions(logger);

    // İlk sayfa için farklı bir üstbilgi/altbilgi kullanılması arama sırasını etkileyecektir.
    firstPageSection.PageSetup.DifferentFirstPageHeaderFooter = differentFirstPageHeaderFooter;
    doc.Range.Replace(new Regex("(header|footer)"), "", options);

    if (differentFirstPageHeaderFooter)
        Assert.AreEqual("First header\nFirst footer\nSecond header\nSecond footer\nThird header\nThird footer\n", 
            logger.Text.Replace("\r", ""));
    else
        Assert.AreEqual("Third header\nFirst header\nThird footer\nFirst footer\nSecond header\nSecond footer\n", 
            logger.Text.Replace("\r", ""));
}

/// <summary>
/// Bir bul-değiştir işlemi sırasında, işlemin 'bulduğu' metni içeren her düğümün içeriğini kaydeder,
/// değiştirme gerçekleşmeden önceki hali.
/// Bu, metin değiştirme işleminin düğümleri hangi sırayla dolaşacağını görüntüler.
/// </summary>
private class ReplaceLog : IReplacingCallback
{
    public ReplaceAction Replacing(ReplacingArgs args)
    {
        mTextBuilder.AppendLine(args.MatchNode.GetText());
        return ReplaceAction.Skip;
    }

    internal string Text => mTextBuilder.ToString();

    private readonly StringBuilder mTextBuilder = new StringBuilder();
}
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
