---
title: Font.NameOther
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. 128 ile 255 arasında karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar.
type: docs
weight: 270
url: /tr/net/aspose.words/font/nameother/
---
## Font.NameOther property

128 ile 255 arasında karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar.

```csharp
public string NameOther { get; set; }
```

### Örnekler

Microsoft Word'ün iki farklı yazı tipini tek bir çalıştırmada nasıl birleştirebileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu yazı tipi yapılandırmasını kullanırken eklemek için oluşturucuyu kullandığımız bir çalıştırmayı varsayalım
// ASCII karakter aralığı içindeki karakterleri içerir. Bu durumda,
// bu yazı tipini kullanarak bu karakterleri gösterecektir.
builder.Font.NameAscii = "Calibri";

// Başka bir yazı tipi belirtilmediğinde, oluşturucu bu yazı tipini eklediği tüm karakterlere de uygular.
Assert.AreEqual("Calibri", builder.Font.Name);

// ASCII aralığının dışındaki tüm karakterler için kullanılacak bir yazı tipi belirtin.
// İdeal olarak, bu yazı tipinin gerekli her ASCII olmayan karakter kodu için bir glifi olmalıdır.
builder.Font.NameOther = "Courier New";

// ASCII karakterlerinden oluşan bir sözcük ve bu aralığın dışındaki tüm karakterleri içeren bir sözcük içeren bir çalıştırma ekleyin.
// Her karakter, bağlı olarak yazı tiplerinden biri kullanılarak görüntülenecektir.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Ayrıca bakınız

* property [Name](../name/)
* class [Font](../)
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


