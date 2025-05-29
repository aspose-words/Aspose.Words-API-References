---
title: Font.NameOther
linktitle: NameOther
articleTitle: NameOther
second_title: .NET için Aspose.Words
description: Font NameOther'ı keşfedin. 128-255 karakter kodları için yazı tiplerini kolayca özelleştirin, metninizin stilini ve okunabilirliğini geliştirin. Tasarımınızı bugün yükseltin!
type: docs
weight: 270
url: /tr/net/aspose.words/font/nameother/
---
## Font.NameOther property

128 ile 255 arasındaki karakter kodlarına sahip karakterler için kullanılan yazı tipini döndürür veya ayarlar.

```csharp
public string NameOther { get; set; }
```

## Örnekler

Microsoft Word'ün iki farklı yazı tipini tek seferde nasıl birleştirebileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bu yazı tipi yapılandırmasını kullanırken oluşturucuyu kullanarak ekleme yaptığımızı varsayalım
// ASCII karakter aralığındaki karakterleri içerir. Bu durumda,
// bu yazı tipini kullanarak o karakterleri gösterecektir.
builder.Font.NameAscii = "Calibri";

// Başka bir yazı tipi belirtilmediğinde, oluşturucu eklediği tüm karakterlere bu yazı tipini uygulayacaktır.
Assert.AreEqual("Calibri", builder.Font.Name);

// ASCII aralığının dışındaki tüm karakterler için kullanılacak yazı tipini belirtin.
// İdeal olarak, bu yazı tipinde her bir gerekli ASCII olmayan karakter kodu için bir glif bulunmalıdır.
builder.Font.NameOther = "Courier New";

// ASCII karakterlerinden oluşan bir kelime ve bu aralığın dışında kalan tüm karakterlerden oluşan bir kelimeden oluşan bir koşu ekle.
// Her karakter, duruma bağlı olarak iki yazı tipinden biri kullanılarak görüntülenecektir.
builder.Writeln("Hello, Привет");

doc.Save(ArtifactsDir + "Font.NameAscii.docx");
```

### Ayrıca bakınız

* property [Name](../name/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
