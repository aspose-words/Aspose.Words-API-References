---
title: HeaderFooterCollection.LinkToPrevious
second_title: Aspose.Words for .NET API Referansı
description: HeaderFooterCollection yöntem. Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgilerine ve altbilgilerine bağlar veya bağlantısını kaldırır.
type: docs
weight: 20
url: /tr/net/aspose.words/headerfootercollection/linktoprevious/
---
## LinkToPrevious(bool) {#linktoprevious_1}

Tüm üstbilgileri ve altbilgileri önceki bölümdeki karşılık gelen üstbilgilerine ve altbilgilerine bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| isLinkToPrevious | Boolean | `doğru` üstbilgileri ve altbilgileri önceki bölüme bağlamak için; `YANLIŞ` bunların bağlantısını kaldırmak için. |

### Notlar

Üstbilgi veya altbilgilerden herhangi biri mevcut değilse bunları otomatik olarak oluşturur.

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

// İlk bölüme geçin ve bir üstbilgi ve altbilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecektir.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgilerini/altbilgilerini önceki bölümün üstbilgilerine/altbilgilerine bağlayabiliriz
// bağlantı bölümünün bağlantılı bölümün üstbilgilerini/altbilgilerini görüntülemesine izin vermek için.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Her bölümün yine kendi üstbilgi/altbilgi nesneleri olacaktır. Bölümleri birbirine bağladığımızda,
// bağlantı bölümü, kendisine ait olanı korurken, bağlantılı bölümün üstbilgisini/altbilgilerini görüntüleyecektir.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Üçüncü bölümün üstbilgilerini/altbilgilerini ikinci bölümün üstbilgilerine/altbilgilerine bağlayın.
// İkinci bölüm zaten ilk bölümün üstbilgisine/altbilgilerine bağlantı veriyor,
// yani ikinci bölüme bağlanmak bir bağlantı zinciri oluşturacaktır.
// Birinci, ikinci ve şimdi de üçüncü bölümlerin tümü, birinci bölümün başlıklarını görüntüleyecektir.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// LinkToPrecious yöntemini çağırırken "false" ileterek önceki bölümün üstbilgi/altbilgilerinin bağlantısını kaldırabiliriz.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Bu yöntemi kullanarak bağlantı vermek için yalnızca belirli bir üstbilgi/altbilgi türünü de seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// İlk bölümün üstbilgi/altbilgileri, önceki bölüm olmadığından kendilerini hiçbir şeye bağlayamaz.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// İkinci bölümün tüm üstbilgileri/altbilgileri, ilk bölümün üstbilgileri/altbilgilerine bağlanır.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Üçüncü bölümde, ikinci bölüm aracılığıyla yalnızca alt bilgi birinci bölümün alt bilgisine bağlanır.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ayrıca bakınız

* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../headerfootercollection/)
* toplantı [Aspose.Words](../../../)

---

## LinkToPrevious(HeaderFooterType, bool) {#linktoprevious}

Belirtilen üstbilgiyi veya altbilgiyi önceki bölümdeki ilgili üstbilgiye veya altbilgiye bağlar veya bağlantısını kaldırır.

```csharp
public void LinkToPrevious(HeaderFooterType headerFooterType, bool isLinkToPrevious)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| headerFooterType | HeaderFooterType | A[`HeaderFooterType`](../../headerfootertype/) Bağlanacak/bağlantıyı kaldıracak üstbilgiyi veya altbilgiyi belirten value . |
| isLinkToPrevious | Boolean | `doğru`üstbilgiyi veya altbilgiyi önceki bölüme bağlamak için; `YANLIŞ` bağlantıyı kaldırmak için. |

### Notlar

Belirtilen türde üstbilgi veya altbilgi yoksa otomatik olarak oluşturur.

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

// İlk bölüme geçin ve bir üstbilgi ve altbilgi oluşturun. Varsayılan olarak,
// üstbilgi ve altbilgi yalnızca onları içeren bölümdeki sayfalarda görünecektir.
builder.MoveToSection(0);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("This is the header, which will be displayed in sections 1 and 2.");

builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("This is the footer, which will be displayed in sections 1, 2 and 3.");

// Bir bölümün üstbilgilerini/altbilgilerini önceki bölümün üstbilgilerine/altbilgilerine bağlayabiliriz
// bağlantı bölümünün bağlantılı bölümün üstbilgilerini/altbilgilerini görüntülemesine izin vermek için.
doc.Sections[1].HeadersFooters.LinkToPrevious(true);

// Her bölümün yine kendi üstbilgi/altbilgi nesneleri olacaktır. Bölümleri birbirine bağladığımızda,
// bağlantı bölümü, kendisine ait olanı korurken, bağlantılı bölümün üstbilgisini/altbilgilerini görüntüleyecektir.
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0], doc.Sections[1].HeadersFooters[0]);
Assert.AreNotEqual(doc.Sections[0].HeadersFooters[0].ParentSection, doc.Sections[1].HeadersFooters[0].ParentSection);

// Üçüncü bölümün üstbilgilerini/altbilgilerini ikinci bölümün üstbilgilerine/altbilgilerine bağlayın.
// İkinci bölüm zaten ilk bölümün üstbilgisine/altbilgilerine bağlantı veriyor,
// yani ikinci bölüme bağlanmak bir bağlantı zinciri oluşturacaktır.
// Birinci, ikinci ve şimdi de üçüncü bölümlerin tümü, birinci bölümün başlıklarını görüntüleyecektir.
doc.Sections[2].HeadersFooters.LinkToPrevious(true);

// LinkToPrecious yöntemini çağırırken "false" ileterek önceki bölümün üstbilgi/altbilgilerinin bağlantısını kaldırabiliriz.
doc.Sections[2].HeadersFooters.LinkToPrevious(false);

// Bu yöntemi kullanarak bağlantı vermek için yalnızca belirli bir üstbilgi/altbilgi türünü de seçebiliriz.
// Üçüncü bölüm artık ikinci ve birinci bölümlerle aynı altbilgiye sahip olacak, ancak üstbilgiye sahip olmayacak.
doc.Sections[2].HeadersFooters.LinkToPrevious(HeaderFooterType.FooterPrimary, true);

// İlk bölümün üstbilgi/altbilgileri, önceki bölüm olmadığından kendilerini hiçbir şeye bağlayamaz.
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count);
Assert.AreEqual(2, doc.Sections[0].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));

// İkinci bölümün tüm üstbilgileri/altbilgileri, ilk bölümün üstbilgileri/altbilgilerine bağlanır.
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count);
Assert.AreEqual(6, doc.Sections[1].HeadersFooters.Count(hf => ((HeaderFooter)hf).IsLinkedToPrevious));

// Üçüncü bölümde, ikinci bölüm aracılığıyla yalnızca alt bilgi birinci bölümün alt bilgisine bağlanır.
Assert.AreEqual(6, doc.Sections[2].HeadersFooters.Count);
Assert.AreEqual(5, doc.Sections[2].HeadersFooters.Count(hf => !((HeaderFooter)hf).IsLinkedToPrevious));
Assert.True(doc.Sections[2].HeadersFooters[3].IsLinkedToPrevious);

doc.Save(ArtifactsDir + "HeaderFooter.Link.docx");
```

### Ayrıca bakınız

* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../headerfootercollection/)
* toplantı [Aspose.Words](../../../)


