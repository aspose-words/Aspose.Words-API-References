---
title: PdfSaveOptions.Clone
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions yöntem. Bu nesnenin derin bir kopyasını oluşturur.
type: docs
weight: 340
url: /tr/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Bu nesnenin derin bir kopyasını oluşturur.

```csharp
public PdfSaveOptions Clone()
```

### Örnekler

Bir belgedeki tüm alanların PDF'ye kaydedilmeden hemen önce nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// PAGE ve NUMPAGES alanlarıyla metin ekleyin. Bu alanlar gerçek zamanlı olarak doğru değeri göstermez.
// "Field.Update()" ve "Document.UpdateFields()" gibi güncelleme yöntemlerini kullanarak bunları manuel olarak güncellememiz gerekecek.
// her seferinde doğru değerleri göstermelerine ihtiyacımız var.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Bir belgedeki tüm alanların kaydetme işleminden hemen önce güncellenmemesi için "UpdateFields" özelliğini "false" olarak ayarlayın.
// Kaydetmeden önce tüm alanlarımızın güncel olacağını biliyorsak bu tercih edilen seçenektir.
// Tüm belgeyi yinelemek için "UpdateFields" özelliğini "true" olarak ayarlayın
// alanlar ve PDF olarak kaydetmeden önce bunları güncelleyin. Bu, tüm alanların görüntülenmesini sağlayacaktır
// PDF'deki en doğru değerler.
options.UpdateFields = updateFields;

// PdfSaveOptions nesnelerini klonlayabiliriz.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


