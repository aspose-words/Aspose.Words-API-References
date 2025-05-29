---
title: HtmlSaveOptions.TableWidthOutputMode
linktitle: TableWidthOutputMode
articleTitle: TableWidthOutputMode
second_title: .NET için Aspose.Words
description: HtmlSaveOptions TableWidthOutputMode ile HTML dışa aktarımlarınızı optimize edin. Sorunsuz MHTML ve EPUB biçimlendirmesi için tablo satır ve hücre genişliklerini kontrol edin.
type: docs
weight: 480
url: /tr/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl aktarılacağını kontrol eder. Varsayılan değerAll .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

## Notlar

HTML biçiminde tablo, satır ve hücre elements (**&lt;tablo&gt;** ,**&lt;tr&gt;** ,**&lt;inci&gt;** ,**&lt;td&gt;**) genişlikleri ya bağıl (yüzde) ya da mutlak birimlerle belirtilebilir. Aspose'daki bir belgede, kelimeler, tablolar, satırlar ve hücrelerin genişlikleri de bağıl ya da mutlak birimler kullanılarak belirtilebilir.

Bir belgeyi Aspose.Words kullanarak HTML'e dönüştürdüğünüzde, ortaya çıkan belgenin görsel aracıda (örneğin bir tarayıcı veya görüntüleyici) nasıl görüntüleneceğini etkilemek için tablo, satır ve hücre genişliklerinin nasıl dışa aktarılacağını kontrol etmek isteyebilirsiniz.

Bu özelliği, hedef belgeye hangi tablo genişlikleri değerlerinin aktarılacağını belirtmek için bir filtre olarak kullanın. Örneğin, bir belgeyi EPUB'a dönüştürüyorsanız ve belgeyi mobil bir okuma aygıtında görüntülemeyi düşünüyorsanız, o zaman muhtemelen mutlak genişlik değerlerini dışa aktarmaktan kaçınmak istersiniz. Bunu yapmak için, çıktı modunu belirtmeniz gerekirRelativeOnly veyaNone böylece mobil cihazdaki izleyici tabloyu ekran genişliğine olabildiğince uygun şekilde yerleştirebilir.

## Örnekler

Çıktı .html'de negatif girintilerin nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Negatif girintili bir tablo ekle, bu tabloyu sol sayfa sınırının ötesine itecektir.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Tabloyu sağa itecek pozitif girintili bir tablo ekle.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Bir belgeyi HTML'e kaydettiğimizde, Aspose.Words yalnızca negatif girintileri koruyacaktır
// "AllowNegativeIndent" bayrağını ayarlarsak ilk tabloya uyguladığımız gibi
// "true"ya geçireceğimiz SaveOptions nesnesinde.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    AllowNegativeIndent = allowNegativeIndent,
    TableWidthOutputMode = HtmlElementSizeOutputMode.RelativeOnly
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.NegativeIndent.html");

if (allowNegativeIndent)
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:-41.65pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
    Assert.True(outDocContents.Contains(
        "<table cellspacing=\"0\" cellpadding=\"0\" style=\"margin-left:30.35pt; border:0.75pt solid #000000; -aw-border:0.5pt single; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
}
```

### Ayrıca bakınız

* enum [HtmlElementSizeOutputMode](../../htmlelementsizeoutputmode/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
