---
title: HtmlSaveOptions.ExportHeadersFootersMode
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Üstbilgilerin ve altbilgilerin HTML MHTML veya EPUBa nasıl aktarılacağını belirtir. Varsayılan değerPerSection HTML/MHTML için veNone EPUB. için
type: docs
weight: 160
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Üstbilgilerin ve altbilgilerin HTML, MHTML veya EPUB'a nasıl aktarılacağını belirtir. Varsayılan değer:PerSection HTML/MHTML için veNone EPUB. için

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

### Notlar

HTML sayfalara ayrılmadığından üstbilgileri ve altbilgileri anlamlı bir şekilde HTML'ye çıkarmak zordur.

Bu özellik olduğundaPerSection, Aspose.Words Export her bölümün başında ve sonunda yalnızca birincil üstbilgiler ve altbilgiler bulunur.

Ne zamanFirstSectionHeaderLastSectionFooter yalnızca ilk birincil üstbilgi ve son birincil altbilgi (öncekiyle bağlantılı olanlar dahil) dışa aktarılır.

Bu özelliği olarak ayarlayarak üstbilgilerin ve altbilgilerin dışa aktarılmasını tamamen devre dışı bırakabilirsiniz.None.

### Örnekler

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

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


