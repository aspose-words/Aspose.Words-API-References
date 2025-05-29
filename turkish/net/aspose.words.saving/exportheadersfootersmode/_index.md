---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: .NET için Aspose.Words
description: Sorunsuz HTML, MHTML veya EPUB başlık ve altbilgi dışa aktarımları için Aspose.Words ExportHeadersFootersMode enum'unu keşfedin. Belge dönüşümünüzü bugün optimize edin!
type: docs
weight: 5750
url: /tr/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Başlıkların ve altbilgilerin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir.

```csharp
public enum ExportHeadersFootersMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Başlıklar ve altbilgiler dışa aktarılmaz. |
| PerSection | `1` | Birincil üstbilgiler ve altbilgiler her bölümün başında ve sonunda dışa aktarılır. |
| FirstSectionHeaderLastSectionFooter | `2` | Birinci bölümün birincil başlığı belgenin başına, birincil altbilgi ise sonuna aktarılır. |
| FirstPageHeaderFooterPerSection | `3` | İlk sayfa üstbilgisi ve altbilgisi her bölümün başına ve sonuna aktarılır. |

## Örnekler

Bir belgeyi HTML'e kaydederken üstbilgilerin/altbilgilerin nasıl atlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Bu belge başlıklar ve altbilgiler içerir. Bunlara "HeadersFooters" koleksiyonu aracılığıyla erişebiliriz.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// .html gibi formatlar belgeyi sayfalara bölmez, bu nedenle üstbilgiler/altbilgiler aynı şekilde çalışmaz
// Microsoft Word kullanarak belgeyi .docx olarak açtığımızda olur.
// Başlık/altbilgi içeren bir dokümanı HTML'e dönüştürürsek, dönüşüm başlık/altbilgileri gövde metnine asimile edecektir.
// HTML'e dönüştürürken başlıkları/altbilgileri atlamak için SaveOptions nesnesini kullanabiliriz.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Kaydedilen belgemizi açın ve başlığın metnini içermediğini doğrulayın
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Ayrıca bakınız

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
