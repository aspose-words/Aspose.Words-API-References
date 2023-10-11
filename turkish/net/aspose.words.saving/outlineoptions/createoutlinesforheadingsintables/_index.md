---
title: OutlineOptions.CreateOutlinesForHeadingsInTables
second_title: Aspose.Words for .NET API Referansı
description: OutlineOptions mülk. Tabloların içindeki başlıklar Başlık stilleriyle biçimlendirilmiş paragraflar için ana hatlar oluşturulup oluşturulmayacağını belirtir.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/
---
## OutlineOptions.CreateOutlinesForHeadingsInTables property

Tabloların içindeki başlıklar (Başlık stilleriyle biçimlendirilmiş paragraflar) için ana hatlar oluşturulup oluşturulmayacağını belirtir.

```csharp
public bool CreateOutlinesForHeadingsInTables { get; set; }
```

### Notlar

Varsayılan değer:`YANLIŞ`.

### Örnekler

Tabloların içindeki başlıklar için PDF belgesi anahat girişlerinin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üç satırlı bir tablo oluşturuyoruz. İlk sıra,
// metnini başlık tipi tarzında formatlayacağımız sütun başlığı görevi görecek.
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

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

// Çıktı PDF belgesi, belge gövdesindeki başlıkları listeleyen bir içindekiler tablosu olan bir taslak içerecektir.
// Bu taslaktaki bir girişe tıklamak bizi ilgili başlığın konumuna götürecektir.
// Ana hatları elde etmek için "HeadingsOutlineLevels" özelliğini "1" olarak ayarlayın
// yalnızca 1'den büyük olmayan başlık düzeylerine sahip başlıkları kaydetmek için.
pdfSaveOptions.OutlineOptions.HeadingsOutlineLevels = 1;

// Tablolardaki tüm başlıkları hariç tutmak için "CreateOutlinesForHeadingsInTables" özelliğini "false" olarak ayarlayın,
// yukarıda taslaktan oluşturduğumuz gibi.
// Tablolardaki tüm başlıkları dahil etmek için "CreateOutlinesForHeadingsInTables" özelliğini "true" olarak ayarlayın
// anahatta, "HeadingsOutlineLevels" özelliğinin değerinden daha büyük olmayan bir başlık düzeyine sahip olmaları koşuluyla.
pdfSaveOptions.OutlineOptions.CreateOutlinesForHeadingsInTables = createOutlinesForHeadingsInTables;

doc.Save(ArtifactsDir + "PdfSaveOptions.TableHeadingOutlines.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [OutlineOptions](../)
* ad alanı [Aspose.Words.Saving](../../outlineoptions/)
* toplantı [Aspose.Words](../../../)


