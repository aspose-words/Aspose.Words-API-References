---
title: Item
second_title: Aspose.Words for .NET API Referansı
description: Bir Üstbilgi Altbilgi verilen dizinde.
type: docs
weight: 10
url: /tr/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Bir **Üstbilgi Altbilgi** verilen dizinde.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyona bir dizin. |

### Notlar

Endeks sıfır tabanlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi gösterir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki saniye anlamına gelir vb.

Dizin, listedeki öğe sayısından büyük veya ona eşitse, bu, boş bir başvuru döndürür.

İndeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu bir boş başvuru döndürür.

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

* class [HeaderFooter](../../headerfooter)
* class [HeaderFooterCollection](../../headerfootercollection)
* ad alanı [Aspose.Words](../../headerfootercollection)
* toplantı [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Bir **Üstbilgi Altbilgi** belirtilen türden.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parametre | Tanım |
| --- | --- |
| headerFooterType | A[`HeaderFooterType`](../../headerfootertype) alınacak üstbilgi/altbilginin türünü belirten value . |

### Notlar

Belirtilen türün üstbilgisi/altbilgisi bulunamazsa null değerini döndürür.

### Örnekler

Belgenin alt bilgisindeki metnin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Bir belgeden tüm alt bilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü yineleyin ve her türden altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    //Üç çeşit altbilgi ve üstbilgi türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Eşit" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Ayrıca bakınız

* class [HeaderFooter](../../headerfooter)
* enum [HeaderFooterType](../../headerfootertype)
* class [HeaderFooterCollection](../../headerfootercollection)
* ad alanı [Aspose.Words](../../headerfootercollection)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
