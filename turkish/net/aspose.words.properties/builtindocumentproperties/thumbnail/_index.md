---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words for .NET
description: BuiltInDocumentProperties Thumbnail mülk. Belgenin küçük resmini alır veya ayarlar C#'da.
type: docs
weight: 280
url: /tr/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Belgenin küçük resmini alır veya ayarlar.

```csharp
public byte[] Thumbnail { get; set; }
```

## Notlar

Şimdilik bu özellik yalnızca bir belge ePub'a aktarılırken kullanılıyor, diğer belge biçimlerinden okunmuyor ve diğer belge biçimlerine yazılmıyor.

İsteğe bağlı formattaki resim bu özelliğe ayarlanabilir, ancak format dışa aktarma sırasında kontrol edilir. InvalidOperationException görüntü geçersizse veya biçimi, belgenin biçimi için desteklenmiyorsa atılır.

ePub yayını için yalnızca gif, jpeg ve png görselleri kullanılabilir.

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

* class [BuiltInDocumentProperties](../)
* ad alanı [Aspose.Words.Properties](../../../aspose.words.properties/)
* toplantı [Aspose.Words](../../../)
