---
title: TxtExportHeadersFootersMode Enum
linktitle: TxtExportHeadersFootersMode
articleTitle: TxtExportHeadersFootersMode
second_title: .NET için Aspose.Words
description: Aspose.Words'ün TxtExportHeadersFootersMode enumunun, en iyi sonuçlar için başlık ve altbilgi işlemeyi özelleştirerek düz metin dışa aktarımlarını nasıl geliştirdiğini keşfedin.
type: docs
weight: 6440
url: /tr/net/aspose.words.saving/txtexportheadersfootersmode/
---
## TxtExportHeadersFootersMode enumeration

Başlıkların ve altbilgilerin düz metin biçimine aktarılma şeklini belirtir.

```csharp
public enum TxtExportHeadersFootersMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Hiçbir başlık ve altbilgi dışa aktarılmaz. |
| PrimaryOnly | `1` | Her bölümün başında ve sonunda yalnızca birincil başlıklar ve altbilgiler dışa aktarılır. |
| AllAtEnd | `2` | Tüm başlıklar ve altbilgiler, belgenin en sonundaki tüm bölüm gövdelerinden sonra yerleştirilir. |

## Örnekler

Üstbilgi ve altbilgilerin düz metin biçimine nasıl aktarılacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();

// Belgeye eşit ve birincil üstbilgiler/altbilgiler ekleyin.
// Birincil üstbilgi/altbilgiler, çift üstbilgi/altbilgileri geçersiz kılacaktır.
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderEven].AppendParagraph("Even header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterEven));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterEven].AppendParagraph("Even footer");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.HeaderPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].AppendParagraph("Primary header");
doc.FirstSection.HeadersFooters.Add(new HeaderFooter(doc, HeaderFooterType.FooterPrimary));
doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].AppendParagraph("Primary footer");

// Bu üstbilgi ve altbilgileri görüntülemek için sayfalar ekleyin.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak); 
builder.Write("Page 3");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.None" olarak ayarlayın
// hiçbir başlık/altbilginin dışa aktarılmaması.
// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.PrimaryOnly" olarak ayarlayın
// yalnızca birincil başlıkları/altbilgileri dışa aktarmak için.
// "ExportHeadersFootersMode" özelliğini "TxtExportHeadersFootersMode.AllAtEnd" olarak ayarlayın
// tüm bölüm gövdeleri için tüm üstbilgi ve altbilgileri belgenin sonuna yerleştirmek için.
saveOptions.ExportHeadersFootersMode = txtExportHeadersFootersMode;

doc.Save(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt", saveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ExportHeadersFooters.txt");

string newLine = Environment.NewLine;
switch (txtExportHeadersFootersMode)
{
    case TxtExportHeadersFootersMode.AllAtEnd:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Even header{newLine}{newLine}" +
                        $"Primary header{newLine}{newLine}" +
                        $"Even footer{newLine}{newLine}" +
                        $"Primary footer{newLine}{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.PrimaryOnly:
        Assert.AreEqual($"Primary header{newLine}" +
                        $"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}" +
                        $"Primary footer{newLine}", docText);
        break;
    case TxtExportHeadersFootersMode.None:
        Assert.AreEqual($"Page 1{newLine}" +
                        $"Page 2{newLine}" +
                        $"Page 3{newLine}", docText);
        break;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
