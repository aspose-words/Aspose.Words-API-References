---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: Aspose.Words for .NET
description: Font NameOther mülk. 128den 255e kadar karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar C#'da.
type: docs
weight: 270
url: /tr/net/aspose.words/font/nameother/
---
## Font.NameOther property

128'den 255'e kadar karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar.

```csharp
public string NameOther { get; set; }
```

## Örnekler

Microsoft Word'ün iki farklı yazı tipini tek seferde nasıl birleştirebileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu yazı tipi yapılandırmasını kullanırken oluşturucuyu eklemek için kullandığımız bir çalıştırmayı varsayalım
// ASCII karakterleri aralığındaki karakterleri içerir. Bu durumda,
// bu karakterleri bu yazı tipini kullanarak görüntüleyecektir.
builder.Font.NameAscii = "Calibri";

// Başka bir yazı tipi belirtilmediğinde, oluşturucu bu yazı tipini eklediği tüm karakterlere de uygulayacaktır.
Assert.AreEqual("Calibri", builder.Font.Name);

// ASCII aralığının dışındaki tüm karakterler için kullanılacak bir yazı tipi belirtin.
// İdeal olarak, bu yazı tipinin gerekli her ASCII olmayan karakter kodu için bir glifi olmalıdır.
builder.Font.NameOther = "Courier New";

// ASCII karakterlerinden oluşan bir kelime ve bu aralığın dışındaki tüm karakterleri içeren bir kelime içeren bir çalıştırma ekleyin.
// Her karakter, bağlı olarak yazı tiplerinden biri kullanılarak görüntülenecektir.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Ayrıca bakınız

* property [Name](../name/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
