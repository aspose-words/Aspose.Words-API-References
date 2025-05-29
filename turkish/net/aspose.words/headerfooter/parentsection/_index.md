---
title: HeaderFooter.ParentSection
linktitle: ParentSection
articleTitle: ParentSection
second_title: .NET için Aspose.Words
description: Hikayenizin üst bölümüne kolayca erişmek, belgenizin yapısını ve organizasyonunu geliştirmek için HeaderFooter ParentSection özelliğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words/headerfooter/parentsection/
---
## HeaderFooter.ParentSection property

Bu hikayenin üst bölümünü alır.

```csharp
public Section ParentSection { get; }
```

## Notlar

`ParentSection` eşdeğerdir[`ParentNode`](../../node/parentnode/) atıldı[`Section`](../../section/).

## Örnekler

Bölümler arasında üstbilgi ve altbilgilerin nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// İlk bölüme geçin ve bir üstbilgi ve altbilgi oluşturun. Varsayılan olarak,
// Başlık ve altbilgi yalnızca bunları içeren bölümdeki sayfalarda görünecektir.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün başlıklarını/altbilgilerini önceki bölümün başlık/altbilgilerine bağlayabiliriz
// Bağlantılı bölümün, bağlantılı bölümün başlıklarını/altbilgilerini görüntülemesine izin vermek için.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Her bölümün hala kendi başlık/altbilgi nesneleri olacak. Bölümleri birbirine bağladığımızda,
// Bağlantı bölümü, kendi başlık/altbilgilerini koruyarak bağlantılı bölümün başlık/altbilgilerini görüntüler.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Üçüncü bölümün başlıklarını/altbilgilerini ikinci bölümün başlık/altbilgilerine bağlayın.
// İkinci bölüm zaten birinci bölümün üstbilgi/altbilgilerine bağlantı veriyor,
// yani ikinci bölüme bağlantı yapıldığında bir bağlantı zinciri oluşacaktır.
// Birinci, ikinci ve şimdi üçüncü bölümlerin hepsinde birinci bölümün başlıkları görüntülenecektir.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// LinkToPrevious metodunu çağırırken "false" değerini geçirerek önceki bir bölümün başlık/altbilgilerinin bağlantısını kaldırabiliriz.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Bu yöntemi kullanarak bağlantı verilecek sadece belirli bir başlık/altbilgi türünü de seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı alt bilgiye sahip olacak, ancak üst bilgiye sahip olmayacak.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// İlk bölümün üstbilgi/altbilgileri kendilerini hiçbir şeye bağlayamaz çünkü önceki bir bölüm yoktur.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// İkinci bölümün tüm üstbilgileri/altbilgileri birinci bölümün üstbilgilerine/altbilgilerine bağlıdır.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Üçüncü bölümde sadece altbilgi, ikinci bölüm aracılığıyla birinci bölümün altbilgisine bağlanıyor.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ayrıca bakınız

* class [Section](../../section/)
* class [HeaderFooter](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
