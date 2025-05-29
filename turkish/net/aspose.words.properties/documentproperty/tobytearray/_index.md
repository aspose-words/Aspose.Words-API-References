---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: .NET için Aspose.Words
description: ToByteArray metoduyla DocumentProperty'yi zahmetsizce bir bayt dizisine dönüştürün. Veri işlemeyi kolaylaştırın ve kodlama verimliliğinizi artırın!
type: docs
weight: 70
url: /tr/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Özellik değerini bayt dizisi olarak döndürür.

```csharp
public byte[] ToByteArray()
```

## Notlar

Özellik türü uygun değilse bir istisna atarByteArray.

## Örnekler

Epub olarak kaydettiğimiz bir belgeye küçük resim eklemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// "Küçük Resim" özelliği eklediğimiz resim verilerini içeren bir belgeyi Epub olarak kaydedersek,
// Bu belgeyi açan bir okuyucu, ilk sayfadan önce resmi görüntüleyebilir.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Bir belgenin küçük resmini çıkarıp yerel dosya sistemine kaydedebiliriz.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Ayrıca bakınız

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
