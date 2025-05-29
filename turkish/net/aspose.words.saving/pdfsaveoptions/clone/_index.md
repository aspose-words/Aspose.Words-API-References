---
title: PdfSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: .NET için Aspose.Words
description: Nesnelerinizin derin bir klonunu zahmetsizce oluşturmak ve PDF yönetim yeteneklerinizi geliştirmek için PdfSaveOptions Clone yöntemini keşfedin.
type: docs
weight: 370
url: /tr/net/aspose.words.saving/pdfsaveoptions/clone/
---
## PdfSaveOptions.Clone method

Bu nesnenin derin bir klonunu oluşturur.

```csharp
public PdfSaveOptions Clone()
```

## Örnekler

Bir belgeyi PDF'e kaydetmeden hemen önce içindeki tüm alanların nasıl güncelleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// PAGE ve NUMPAGES alanlarını içeren metni ekleyin. Bu alanlar gerçek zamanlı olarak doğru değeri göstermez.
// "Field.Update()" ve "Document.UpdateFields()" gibi güncelleme yöntemlerini kullanarak bunları manuel olarak güncellememiz gerekecek
// her seferinde doğru değerleri göstermelerine ihtiyacımız var.
builder.Write("Page ");
builder.InsertField("PAGE", "");
builder.Write(" of ");
builder.InsertField("NUMPAGES", "");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Hello World!");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Bir kaydetme işleminden hemen önce belgedeki tüm alanları güncellememek için "UpdateFields" özelliğini "false" olarak ayarlayın.
// Kaydetmeden önce tüm alanlarımızın güncel olacağını biliyorsak bu tercih edilen seçenektir.
// Tüm belgede yineleme yapmak için "UpdateFields" özelliğini "true" olarak ayarlayın
// alanları ve PDF olarak kaydetmeden önce bunları güncelleyin. Bu, tüm alanların görüntülenmesini sağlayacaktır
// PDF'deki en doğru değerler.
options.UpdateFields = updateFields;

// PdfSaveOptions nesnelerini klonlayabiliriz.
Assert.AreNotSame(options, options.Clone());

doc.Save(ArtifactsDir + "PdfSaveOptions.UpdateFields.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
