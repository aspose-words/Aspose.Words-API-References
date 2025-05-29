---
title: HtmlSaveOptions.ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
articleTitle: ExportHeadersFootersMode
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ExportHeadersFootersMode özelliğinin HTML, MHTML ve EPUB biçimleri için başlık ve altbilgi çıktısını nasıl optimize ettiğini keşfedin. Belgenizin sunumunu en üst düzeye çıkarın!
type: docs
weight: 160
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/
---
## HtmlSaveOptions.ExportHeadersFootersMode property

Başlıkların ve altbilgilerin HTML, MHTML veya EPUB'a nasıl çıktılanacağını belirtir. Varsayılan değerPerSection HTML/MHTML ve içinNone EPUB için.

```csharp
public ExportHeadersFootersMode ExportHeadersFootersMode { get; set; }
```

## Notlar

HTML'de sayfalandırma olmadığından, başlıkları ve alt bilgileri anlamlı bir şekilde HTML'e aktarmak zordur.

Bu özellik ne zamanPerSection, Aspose.Words yalnızca her bölümün başında ve sonunda birincil üstbilgileri ve altbilgileri dışa aktarır.

Ne zamanFirstSectionHeaderLastSectionFooter yalnızca ilk birincil başlık ve son birincil altbilgi (öncekilere bağlı olanlar dahil) dışa aktarılır.

Bu property değerini ayarlayarak başlık ve altbilgilerin dışa aktarılmasını tamamen devre dışı bırakabilirsiniz.None.

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

* enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
