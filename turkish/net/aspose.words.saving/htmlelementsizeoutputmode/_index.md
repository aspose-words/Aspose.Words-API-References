---
title: HtmlElementSizeOutputMode Enum
linktitle: HtmlElementSizeOutputMode
articleTitle: HtmlElementSizeOutputMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.HtmlElementSizeOutputMode Sıralama. Aspose.Wordsün öğe genişliklerini ve yüksekliklerini HTML MHTML ve EPUBa nasıl aktardığını belirtir C#'da.
type: docs
weight: 5060
url: /tr/net/aspose.words.saving/htmlelementsizeoutputmode/
---
## HtmlElementSizeOutputMode enumeration

Aspose.Words'ün öğe genişliklerini ve yüksekliklerini HTML, MHTML ve EPUB'a nasıl aktardığını belirtir.

```csharp
public enum HtmlElementSizeOutputMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| All | `0` | Belgede belirtilen hem mutlak hem de göreli birimlerdeki tüm öğe boyutları dışa aktarılır. |
| RelativeOnly | `1` | Öğe boyutları yalnızca belgede ilgili birimler halinde belirtilmişse dışa aktarılır. Sabit boyutlar bu modda dışa aktarılmaz. Görsel aracılar, belge düzenini daha doğal hale getirmek için eksik boyutları hesaplayacak. |
| None | `2` | Öğe boyutları dışa aktarılmaz. Görsel aracılar, öğeler arasındaki ilişkiye göre düzeni otomatik olarak oluşturacaktır. |

## Örnekler

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

* property [TableWidthOutputMode](../htmlsaveoptions/tablewidthoutputmode/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
