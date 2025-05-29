---
title: HeaderFooterCollection.LinkToPrevious
linktitle: LinkToPrevious
articleTitle: LinkToPrevious
second_title: .NET için Aspose.Words
description: Sorunsuz biçimlendirme için belge bölümleriniz arasında üstbilgileri ve altbilgileri kolayca bağlamak veya bağlantısını kesmek üzere HeaderFooterCollection'daki LinkToPrevious yöntemini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(*bool*) {#linktoprevious_1}

Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgilere ve altbilgilere bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `doğru` Başlıkları ve altbilgileri önceki bölüme bağlamak için; `YANLIŞ` onları birbirinden ayırmak için. |

## Notlar

Başlık veya altbilgilerden herhangi biri mevcut değilse, bunları otomatik olarak oluşturur.

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

* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## LinkToPrevious(*[HeaderFooterType](../../headerfootertype/), bool*) {#linktoprevious}

Belirtilen üstbilgi veya altbilgiyi önceki bölümdeki karşılık gelen üstbilgi veya altbilgiye bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype/) Bağlanacak/bağlantısı kaldırılacak üstbilgi veya altbilgiyi belirten value . |
| isLinkToPrevious | Boolean | `doğru` üstbilgiyi veya altbilgiyi önceki bölüme bağlamak için; `YANLIŞ` bağlantısını kesmek. |

## Notlar

Belirtilen türün üstbilgisi veya altbilgisi yoksa otomatik olarak oluşturur.

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

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
