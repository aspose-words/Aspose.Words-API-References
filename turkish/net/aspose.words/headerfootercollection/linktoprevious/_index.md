---
title: LinkToPrevious
second_title: Aspose.Words for .NET API Referansı
description: Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgi ve altbilgilere bağlar veya bağlantısını kaldırır.
type: docs
weight: 20
url: /tr/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(bool) {#linktoprevious_1}

Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgi ve altbilgilere bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| isLinkToPrevious | Boolean | Üstbilgileri ve altbilgileri önceki bölüme bağlamak için true; false bağlantılarını kaldırmak için. |

### Notlar

Üstbilgi veya altbilgilerden herhangi biri yoksa, bunları otomatik olarak oluşturur.

### Örnekler

Bölümler arasında üstbilgilerin ve altbilgilerin nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// İlk bölüme gidin ve bir üst bilgi ve bir alt bilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünür.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgilerini/altbilgilerini önceki bölümün üstbilgilerine/altbilgilerine bağlayabiliriz
// bağlama bölümünün, bağlantılı bölümün üstbilgilerini/altbilgilerini görüntülemesine izin vermek için.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Her bölümün hala kendi üstbilgi/altbilgi nesneleri olacaktır. Bölümleri bağladığımızda,
// bağlama bölümü, kendi bölümünü korurken bağlantılı bölümün üstbilgisini/altbilgilerini görüntüler.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Üçüncü bölümün üstbilgilerini/altbilgilerini ikinci bölümün üstbilgilerini/altbilgilerini bağlayın.
// İkinci bölüm, birinci bölümün üstbilgi/altbilgilerine zaten bağlantı veriyor,
// böylece ikinci bölüme bağlantı bir bağlantı zinciri oluşturacaktır.
// Birinci, ikinci ve şimdi üçüncü bölümlerin tümü ilk bölümün başlıklarını gösterecek.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// LinkToPrevious yöntemini çağırırken "false" ileterek önceki bölümün üstbilgi/altbilgilerinin bağlantısını kaldırabiliriz.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Ayrıca, bu yöntemi kullanarak yalnızca belirli bir üstbilgi/altbilgi türü seçebiliriz.
// Üçüncü bölüm şimdi ikinci ve ilk bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// İlk bölümün üstbilgi/altbilgileri, önceki bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// İkinci bölümün tüm üstbilgileri/altbilgileri, ilk bölümün üstbilgileri/altbilgileri ile bağlantılıdır.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Üçüncü bölümde, sadece altbilgi, ikinci bölüm aracılığıyla birinci bölümün altbilgisine bağlanır.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ayrıca bakınız

* class [HeaderFooterCollection](../../headerfootercollection)
* ad alanı [Aspose.Words](../../headerfootercollection)
* toplantı [Aspose.Words](../../../)

---

## LinkToPrevious(HeaderFooterType, bool) {#linktoprevious}

Belirtilen üstbilgi veya altbilgiyi önceki bölümdeki karşılık gelen üstbilgi veya altbilgiye bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype) Bağlanacak/bağlantıyı kaldıracak üstbilgiyi veya altbilgiyi belirten value . |
| isLinkToPrevious | Boolean | Üstbilgiyi veya altbilgiyi önceki bölüme bağlamak için true;bağlantıyı kaldırmak için false. |

### Notlar

Belirtilen türde üstbilgi veya altbilgi yoksa, otomatik olarak oluşturur.

### Örnekler

Bölümler arasında üstbilgilerin ve altbilgilerin nasıl bağlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

// İlk bölüme gidin ve bir üst bilgi ve bir alt bilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünür.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgilerini/altbilgilerini önceki bölümün üstbilgilerine/altbilgilerine bağlayabiliriz
// bağlama bölümünün, bağlantılı bölümün üstbilgilerini/altbilgilerini görüntülemesine izin vermek için.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Her bölümün hala kendi üstbilgi/altbilgi nesneleri olacaktır. Bölümleri bağladığımızda,
// bağlama bölümü, kendi bölümünü korurken bağlantılı bölümün üstbilgisini/altbilgilerini görüntüler.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Üçüncü bölümün üstbilgilerini/altbilgilerini ikinci bölümün üstbilgilerini/altbilgilerini bağlayın.
// İkinci bölüm, birinci bölümün üstbilgi/altbilgilerine zaten bağlantı veriyor,
// böylece ikinci bölüme bağlantı bir bağlantı zinciri oluşturacaktır.
// Birinci, ikinci ve şimdi üçüncü bölümlerin tümü ilk bölümün başlıklarını gösterecek.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// LinkToPrevious yöntemini çağırırken "false" ileterek önceki bölümün üstbilgi/altbilgilerinin bağlantısını kaldırabiliriz.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Ayrıca, bu yöntemi kullanarak yalnızca belirli bir üstbilgi/altbilgi türü seçebiliriz.
// Üçüncü bölüm şimdi ikinci ve ilk bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// İlk bölümün üstbilgi/altbilgileri, önceki bölüm olmadığı için kendilerini hiçbir şeye bağlayamaz.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// İkinci bölümün tüm üstbilgileri/altbilgileri, ilk bölümün üstbilgileri/altbilgileri ile bağlantılıdır.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Üçüncü bölümde, sadece altbilgi, ikinci bölüm aracılığıyla birinci bölümün altbilgisine bağlanır.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ayrıca bakınız

* enum [HeaderFooterType](../../headerfootertype)
* class [HeaderFooterCollection](../../headerfootercollection)
* ad alanı [Aspose.Words](../../headerfootercollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
