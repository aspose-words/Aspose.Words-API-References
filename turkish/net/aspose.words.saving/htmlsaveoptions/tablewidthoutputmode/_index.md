---
title: HtmlSaveOptions.TableWidthOutputMode
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Tablo satır ve hücre genişliklerinin HTML MHTML veya EPUBa nasıl aktarıldığını kontrol eder. Varsayılan değerAll .
type: docs
weight: 460
url: /tr/net/aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/
---
## HtmlSaveOptions.TableWidthOutputMode property

Tablo, satır ve hücre genişliklerinin HTML, MHTML veya EPUB'a nasıl aktarıldığını kontrol eder. Varsayılan değer:All .

```csharp
public HtmlElementSizeOutputMode TableWidthOutputMode { get; set; }
```

### Notlar

HTML formatında tablo, satır ve hücre elemanları ( **&lt;tablo&gt;** , **&lt;tr&gt;** , **&lt;th&gt;** , **&lt;td&gt;**) 'nin genişlikleri bağıl (yüzde) veya mutlak birimlerle belirtilebilir. Aspose.Words'teki bir belgede tabloların, satırların ve hücrelerin genişlikleri göreceli veya mutlak birimler kullanılarak olarak belirtilebilir.

Aspose.Words kullanarak bir belgeyi HTML'ye dönüştürdüğünüzde, ortaya çıkan belgenin görsel aracıda (örneğin bir tarayıcı veya görüntüleyici) nasıl görüntüleneceğini etkilemek için nasıl tablo, satır ve hücre genişliklerinin dışa aktarıldığını kontrol etmek isteyebilirsiniz.

Hedef belgeye hangi tablo genişliği değerlerinin aktarılacağını belirtmek için bu özelliği filtre olarak kullanın. Örneğin, bir belgeyi EPUB'a dönüştürüyorsanız ve belgeyi mobil bir okuma cihazında görüntülemeyi düşünüyorsanız, muhtemelen bundan kaçınmak istersiniz mutlak genişlik değerlerini dışa aktarma. Bunu yapmak için çıkış modunu belirtmeniz gerekirRelativeOnly veyaNone böylece mobil cihazdaki izleyici, tabloyu ekranın genişliğine mümkün olan en iyi şekilde uyacak şekilde düzenleyebilir.

### Örnekler

.html çıktısında negatif girintilerin nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Negatif girintili bir tablo ekleyin, bu tabloyu sol sayfa sınırının ötesine itecek.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = -36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

builder.InsertBreak(BreakType.ParagraphBreak);

// Tabloyu sağa itecek pozitif girintili bir tablo ekleyin.
table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, Cell 1");
builder.InsertCell();
builder.Write("Row 1, Cell 2");
builder.EndTable();
table.LeftIndent = 36;
table.PreferredWidth = PreferredWidth.FromPoints(144);

// Bir belgeyi HTML'ye kaydettiğimizde Aspose.Words yalnızca negatif girintileri korur
// "AllowNegativeIndent" bayrağını ayarlarsak ilk tabloya uyguladığımız gibi
// SaveOptions nesnesinde "true" değerine geçeceğiz.
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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


