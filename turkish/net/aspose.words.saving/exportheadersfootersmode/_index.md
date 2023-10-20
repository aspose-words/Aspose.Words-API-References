---
title: ExportHeadersFootersMode Enum
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.ExportHeadersFootersMode Sıralama. Üstbilgilerin ve altbilgilerin HTML MHTML veya EPUBa nasıl aktarılacağını belirtir C#'da.
type: docs
weight: 5000
url: /tr/net/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enumeration

Üstbilgilerin ve altbilgilerin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir.

```csharp
public enum ExportHeadersFootersMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Üstbilgiler ve altbilgiler dışa aktarılmaz. |
| PerSection | `1` | Birincil üstbilgiler ve altbilgiler her bölümün başında ve sonunda dışa aktarılır. |
| FirstSectionHeaderLastSectionFooter | `2` | İlk bölümün birincil başlığı belgenin başına aktarılır ve birincil altbilgi belgenin sonundadır. |
| FirstPageHeaderFooterPerSection | `3` | İlk sayfa üst bilgisi ve alt bilgisi her bölümün başında ve sonunda dışa aktarılır. |

## Örnekler

Bir belgeyi HTML'ye kaydederken üstbilgilerin/altbilgilerin nasıl atlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Bu belge üstbilgi ve altbilgileri içerir. Bunlara "HeadersFooters" koleksiyonu aracılığıyla erişebiliriz.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// .html gibi formatlar belgeyi sayfalara bölmez, dolayısıyla üstbilgiler/altbilgiler aynı şekilde çalışmaz
// belgeyi Microsoft Word kullanarak .docx olarak açtığımızda bunu yaparlar.
// Üstbilgileri/altbilgileri olan bir belgeyi html'ye dönüştürürsek, dönüşüm üstbilgileri/altbilgileri gövde metnine asimile edecektir.
// HTML'ye dönüştürürken üstbilgileri/altbilgileri atlamak için SaveOptions nesnesini kullanabiliriz.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Kaydedilen belgemizi açın ve başlık metnini içermediğini doğrulayın
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Ayrıca bakınız

* property [ExportHeadersFootersMode](../htmlsaveoptions/exportheadersfootersmode/)
* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
