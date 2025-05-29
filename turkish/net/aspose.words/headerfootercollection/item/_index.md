---
title: HeaderFooterCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: Öğe özelliğiyle HeaderFooters'a zahmetsizce erişin. Kolaylaştırılmış belge yönetimi için dizine göre belirli başlıkları veya altbilgileri alın.
type: docs
weight: 10
url: /tr/net/aspose.words/headerfootercollection/item/
---
## HeaderFooterCollection indexer (1 of 2)

Birini alır[`HeaderFooter`](../../headerfooter/) verilen indekste.

```csharp
public HeaderFooter this[int index] { get; }
```

| Parametre | Tanım |
| --- | --- |
| index | Koleksiyonun indeksi. |

## Notlar

Endeks sıfır bazlıdır.

Negatif indekslere izin verilir ve koleksiyonun sonundan erişimi belirtir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi vb. ifade eder.

Eğer indeks listedeki öğe sayısından büyük veya eşitse, bu boş bir referans döndürür.

Eğer indeks negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu durum boş bir referans döndürür.

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

* class [HeaderFooter](../../headerfooter/)
* class [HeaderFooterCollection](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## HeaderFooterCollection indexer (2 of 2)

Birini alır[`HeaderFooter`](../../headerfooter/) belirtilen türde.

```csharp
public HeaderFooter this[HeaderFooterType headerFooterType] { get; }
```

| Parametre | Tanım |
| --- | --- |
| headerFooterType | A[`HeaderFooterType`](../../headerfootertype/) Alınacak başlık/altbilginin türünü belirten value . |

## Notlar

Geri Döndürür`hükümsüz`Belirtilen türün üstbilgisi/altbilgisi bulunamazsa.

## Örnekler

Bir belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

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

Bir belgeden tüm altbilgilerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Her bölümü inceleyin ve her türlü altbilgiyi kaldırın.
foreach (Section section in doc.OfType<Section>())
{
    // Üç çeşit altbilgi ve üstbilgi türü vardır.
    // 1 - Bir bölümün yalnızca ilk sayfasında görünen "İlk" üstbilgi/altbilgi.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 - Tek sayfalarda görünen "Birincil" üstbilgi/altbilgi.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - Çift sayfalarda görünen "Çift" üstbilgisi/altbilgisi.
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
