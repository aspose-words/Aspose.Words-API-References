---
title: SaveOptions.UpdateFields
linktitle: UpdateFields
articleTitle: UpdateFields
second_title: .NET için Aspose.Words
description: SaveOptions UpdateFields özelliğinin, sabit biçimlere dönüştürmeden önce belirli alan türlerini güncelleyerek belge kaydetmeyi nasıl optimize ettiğini keşfedin. Varsayılan, true.
type: docs
weight: 170
url: /tr/net/aspose.words.saving/saveoptions/updatefields/
---
## SaveOptions.UpdateFields property

Belgeyi sabit bir sayfa biçimine kaydetmeden önce belirli türdeki alanların güncellenip güncellenmeyeceğini belirleyen bir değeri alır veya ayarlar. Bu özelliğin varsayılan değeri`doğru` .

```csharp
public bool UpdateFields { get; set; }
```

## Notlar

MS Word davranışının taklit edilip edilmeyeceğini belirtmeye izin verir.

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

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
