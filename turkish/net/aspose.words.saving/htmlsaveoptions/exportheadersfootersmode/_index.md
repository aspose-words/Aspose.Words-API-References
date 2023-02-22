---
title: HtmlSaveOptions.ExportHeadersFootersMode
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Üstbilgilerin ve altbilgilerin HTML MHTML veya EPUBa nasıl çıkarılacağını belirtir. Varsayılan değerPerSection HTML/MHTML için veNone EPUB için.
type: docs
weight: 170
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Üstbilgilerin ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıkarılacağını belirtir. Varsayılan değerPerSection HTML/MHTML için veNone EPUB için.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### Notlar

HTML sayfalandırılmadığından, üstbilgileri ve altbilgileri anlamlı bir şekilde HTML'ye çıkarmak zordur.

Bu özellik ne zamanPerSection, Aspose.Words her bölümün başında ve sonunda yalnızca birincil üstbilgileri ve altbilgileri dışa aktarır.

Ne zamanFirstSectionHeaderLastSectionFooter yalnızca ilk birincil üstbilgi ve son birincil altbilgi (öncekiyle bağlantılı olanlar dahil) dışa aktarılır.

Bu özelliği olarak ayarlayarak üstbilgilerin ve altbilgilerin dışa aktarılmasını tamamen devre dışı bırakabilirsiniz.None.

### Örnekler

Bir belgeyi HTML'ye kaydederken üstbilgilerin/altbilgilerin nasıl atlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Bu belge üstbilgi ve altbilgi içerir. Onlara "HeadersFooters" koleksiyonu aracılığıyla erişebiliriz.
Assert.AreEqual("First header", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());

// .html gibi biçimler belgeyi sayfalara bölmez, bu nedenle üstbilgiler/altbilgiler aynı şekilde çalışmaz
// Microsoft Word kullanarak belgeyi .docx olarak açtığımızda yaparlar.
// Üstbilgileri/altbilgileri olan bir belgeyi html'ye dönüştürürsek, dönüştürme, üstbilgileri/altbilgileri gövde metnine dönüştürür.
// Html'ye dönüştürürken üstbilgileri/altbilgileri atlamak için SaveOptions nesnesini kullanabiliriz.
HtmlSaveOptions saveOptions =
    new HtmlSaveOptions(SaveFormat.Html) { ExportHeadersFootersMode = ExportHeadersFootersMode.None };

doc.Save(ArtifactsDir + "HeaderFooter.ExportMode.html", saveOptions);

// Kaydedilmiş belgemizi açın ve başlığın metnini içermediğini doğrulayın
doc = new Document(ArtifactsDir + "HeaderFooter.ExportMode.html");

Assert.IsFalse(doc.Range.Text.Contains("First header"));
```

### Ayrıca bakınız

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


