---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: HeaderFooterCollection Item mülk. Bir öğeyi alırHeaderFooter verilen dizinde C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Bir öğeyi alır[`HeaderFooter`](../../headerfooter/) verilen dizinde.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyona bir dizin. |

## Notlar

Endeks sıfır bazlıdır.

Negatif dizinlere izin verilir ve koleksiyonun arkasından erişimi belirtir. Örneğin -1 son öğe anlamına gelir, -2 sondan önceki ikinci öğe anlamına gelir ve bu şekilde devam eder.

Dizin listedeki öğe sayısından büyük veya ona eşitse bu, boş bir başvuru döndürür.

Dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse bu, boş bir başvuru döndürür.

## Örnekler

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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Bir öğeyi alır[`HeaderFooter`](../../headerfooter/) belirtilen türden.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parametre | Tanım |
| --- | --- |
| headerFooterType | A[`HeaderFooterType`](../../headerfootertype/) alınacak üstbilgi/altbilginin türünü belirten value . |

## Notlar

İadeler`hükümsüz` belirtilen türdeki üstbilgi/altbilgi bulunamazsa.

## Örnekler

Belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

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

Bir belgedeki tüm altbilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü yineleyin ve her türden altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    // Üç çeşit altbilgi ve başlık türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Çift" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

### Ayrıca bakınız

* class [HeaderFooter](../../headerfooter/)
* enum [HeaderFooterType](../../headerfootertype/)
* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
