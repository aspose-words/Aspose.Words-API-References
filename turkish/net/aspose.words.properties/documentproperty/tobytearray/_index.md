---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words for .NET
description: DocumentProperty ToByteArray yöntem. Özellik değerini bayt dizisi olarak döndürür C#'da.
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

Özellik türü değilse bir istisna atarByteArray.

## Örnekler

Epub olarak kaydettiğimiz bir belgeye nasıl küçük resim ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// "Thumbnail" özelliği eklediğimiz görsel verilerini içeren bir dokümanı Epub olarak kaydedersek,
// o belgeyi açan okuyucu, görüntüyü ilk sayfadan önce görüntüleyebilir.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Bir belgenin küçük resmini çıkartıp yerel dosya sistemine kaydedebiliriz.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Ayrıca bakınız

* class [DocumentProperty](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
