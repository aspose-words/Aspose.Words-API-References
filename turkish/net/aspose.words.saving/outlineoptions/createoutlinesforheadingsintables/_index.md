---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
linktitle: CreateOutlinesForHeadingsInTables
articleTitle: CreateOutlinesForHeadingsInTables
second_title: .NET için Aspose.Words
description: CreateOutlinesForHeadingsInTables özelliğinin başlık stilleri için ana hatları etkinleştirerek ve belge netliğini iyileştirerek tablo organizasyonunu nasıl geliştirdiğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Tabloların içindeki başlıklar (Başlık stilleri ile biçimlendirilen paragraflar) için ana hatların oluşturulup oluşturulmayacağını belirtir.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

## Notlar

Varsayılan değer`YANLIŞ`.

## Örnekler

Tabloların içindeki başlıklar için PDF belge anahat girişlerinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üç satırdan oluşan bir tablo oluşturun. İlk satır,
// metnini başlık türü stilinde biçimlendireceğimiz metin, sütun başlığı olarak kullanılacaktır.
builder.StartTable();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Write("Customers");
builder.EndRow();
builder.InsertCell();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Normal;
builder.Write("John Doe");
builder.EndRow();
builder.InsertCell();
builder.Write("Jane Doe");
builder.EndTable();

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içerik tablosu olan bir ana hat içerecektir.
// Bu taslaktaki bir girdiye tıkladığımızda ilgili başlığın bulunduğu yere gideceğiz.
// Anahattı almak için "HeadingsOutlineLevels" özelliğini "1" olarak ayarlayın
// yalnızca 1'den büyük olmayan başlık düzeylerine sahip başlıkları kaydetmek için.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Tablolardaki tüm başlıkları hariç tutmak için "CreateOutlinesForHeadingsInTables" özelliğini "false" olarak ayarlayın.
// yukarıda taslağı oluşturduğumuz gibi.
// Tablolardaki tüm başlıkları dahil etmek için "CreateOutlinesForHeadingsInTables" özelliğini "true" olarak ayarlayın
// anahatta, "HeadingsOutlineLevels" özelliğinin değerinden büyük olmayan bir başlık düzeyine sahip olmaları koşuluyla.
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
